# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  1. We drop the lower order terms when doing asymptotic analysis and these could have actual impact on prefomance in real practice. 
  2. In asymptotic analiysis we treat all constants at the same rate. When in practice constants can take different amounts of time. Like comparing strings takes longer then comparing integers.
  3. Input size also makes a difference. If you look that the lecture slides and see the graph for "Average case running times" you see that Timsort takes a longer amount of time to sort a list size of ≈62500 items then heap sort. Then the amount of time levels out between the two sorting types before timsort rises, timsort again take more time as the list size grows. This shows that when you take bounds for asymptotic analysis, it will not always reflect what the best algorithm is for each individuel case when using it in practice.
     Loose and tight bounds can be the difference. You can have bounds like a loose $O$ bound $f(n) \in O(n^2), f(n) \in O(n^3), f(n) \in O(2^n)$. It meets the criteria in therory but doesn't give a very good explanation so finding a tighter $O$ bound would be better in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

Having $O(log_2n)$ as the asymptotic complexity for searching for a specific element in a binary search tree of 1000 elements in 5 seconds has the same logarithmic growth for 10,000 elements. So, 5 secs / $log_2(1000)$ = x / log_2(10,000)$ = $5 * log_2(10,000) / log_2(1000)$. 5*13.29= 66.44  $log_2(1000) = 9.97. (66.44/9.97) = 6.7 secs to find the same element in the tree with 10,000 items.


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  
  1.The asymptotic anaylisis is $log_n$ for a binary tree. If we assume that the element is near the begining of the tree and alos assume good implentation then it should take less then 5 secs to find the specific element. This shows that the implentation isn't good. So if the best case is the element is near the begining of the tree take 6.7 secs then if the element was much deeper in the tree the this could account for the 100 second runtime.

  2. Computing hardware is an obvious reason this could happen. If you run the same search on two different machines with different specs then this could cause the difference in analysis because the hardware is not taken into account for the asymptotic complexity. This is becuase we assume that each comparison in the binary tree takes the exact same amount of time. 

  3.Even further into the difference in hardware is the size of the trees and memory, the computing power and memory for a 1000 element tree is going to be less then 10,000 element tree. This could cause the certain computer to switch to disk memory to store the elements vs having the elements stored in RAM could also make the difference in time.

Add your answers to this markdown file.

https://www.geeksforgeeks.org/complexity-different-operations-binary-tree-binary-search-tree-avl-tree/

https://uwyo.instructure.com/courses/593273/files/folder/slides?preview=86250260 (Slide 55)

class topics and notes

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
