# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  1.Dropping constants and lower order terms 2.Input size:\
  \
  We drop and disregard the lower order terms when doing asymptotic analysis and these could have actual impact on performance in real practice. So let's say we have $3n^3 + 2n^2 + 50n + 100$. When you do asymptotic analysis we are only focusing on the term with the highest growth rate. $3n^3$ has the highest growth rate. We would disregard the lower order terms and constant giving us a complexity of $O(n^3)$. This is good for large input sizes but the lower order terms and the constant could effect this with smaller input sizes. If this algorithm had a constant factor of 3 we would have $3n^3$ and we have a second algorithm that's $O(n^2)$ with a constant factor of 100.\
    1st. $3(10^3) = 3000$\
    2nd. $100(10^2) = 10,000$\
  So the first algorithm is faster with a smaller input size, if we make the first input size the same as the second n=100, then we see the $n^3$ grows much faster and becomes slower then the 2nd algorithm. This is why input size matters and why the complexity can show the scaling of an algorithm but disregarding the constant factors can be misleading. An algorithm with a lower asymptotic complexity can be slower if it has a larger constant factor.
     

2. In asymptotic analiysis we treat all constants at the same rate. When in practice constants can take different amounts of time. Like comparing strings takes longer then comparing integers.
    

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

Having $O(log_2n)$ as the asymptotic complexity for searching for a specific element in a binary search tree of 1000 elements in 5 seconds has the same logarithmic growth for 10,000 elements. So, 5 secs / $log_2(1000)$ = x / log_2(10,000)$ = $5 * log_2(10,000) / log_2(1000)$. 5*13.29= 66.44  $log_2(1000) = 9.97. (66.44/9.97) = 6.7 secs to find the same element in the tree with 10,000 items.


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  
  1.The asymptotic anaylisis is $log_n$ for a binary tree. If we assume that the element is near the begining of the tree and also assume good implentation then theoretically it should take around 6.7 secs. If the tree is not balanced, then the height of the tree could be larger then $log_2(n)$. This is a reason why it could take 100 secs.

  2. Computing hardware is an obvious reason this could happen. If you run the same search on two different machines with different specs then this could cause the difference in analysis because the hardware is not taken into account for the asymptotic complexity. This is becuase we assume that each comparison in the binary tree takes the exact same amount of time. 

  3.Even further into the difference in hardware is the size of the trees and memory, the computing power and memory for a 1000 element tree is going to be less then 10,000 element tree. This could cause the certain computer to switch to disk memory to store the elements vs having the elements stored in RAM could also make the difference in time.

Add your answers to this markdown file.

https://www.geeksforgeeks.org/complexity-different-operations-binary-tree-binary-search-tree-avl-tree/

https://uwyo.instructure.com/courses/593273/files/folder/slides?preview=86250260 (Slide 55)

class topics and notes

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
