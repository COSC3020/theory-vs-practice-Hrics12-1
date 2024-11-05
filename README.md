# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  

  1. Input size matters becuase when doing the asymptotic analysis we focus on how the algorithm scales as the input size increases. When an algorithm takes a small input or even a medium size input the runtime can be seriously influenced by constant factors and lower order terms that have been disregarded. if I have an algorithm, $3n^3 + 2n^2 + 50n + 100$ you have a time complexity of $O(n^3)$ Then you have another algorithm with a time complexity of $O(n^2)$, $100n^2 + 50(100)+100$. If you take a small input size of $n=100$ the lower order terms in the first algorithm have a larger inpact on the operations being preformed. <br><br>
  n=100<br> Algo $A_1$: $3(100^3)+2(100^2)+50(100)+100$ = 3,025,100 <br>
  Algo $B_1$: $100(100^2)+50(100)+100$ = 1,005,100 <br><br>
  n=1,000,000<br>
  Algo $A_2$: $3(1,000,000^3)+2(1,000,000^2)+50(1,000,000)+100$ = $3.000002*10^{18}$<br>
  Algo $B_2$: $100(1,000,000^2)+50(1,000,000)+ 100$ = $1.00000005 * 10^{14}$<br><br>
  Lower order terms and constants:<br>
  n=100 <br>
  Algo $A_1$: $2(100^2)+50(100)+100$ = 25100 or .8297% of Algo $A_1$<br>
  Algo $B_1$: $50(100)+100$ = 5100 or .5074% of Algo $B_1$ <br><br>
  n=1,000,000<br>
  Algo $A_2$: $2(1,000,000^2)+50(1.000,000)+100$ = $2.00005 * 10^{12}$ or .0000667% of Algo $A_2$ <br>
  Algo $B_2$: $50(1,000,000)+100$ = $50000100$ or .00005% of Algo $B_2$<br><br>
  You can see from the percentages that as the input size grows the lower order terms and constants have a much smaller impact on the amount of operations the algorithm does. So in practice you need to know how impactuful your lower order terms and constants will be based on individual circumstances.


2. In asymptotic analiysis we treat all constants at the same rate. When in practice constants can take different amounts of time. Like comparing strings takes longer then comparing integers.


3. Hardware as an issue. Asymptotic analysis does not take into account for hardware specifics like your cache and or memory hierarchy. Running an algorithm and getting a certain Big-O bound on one machine could be significantly different on a different machine.
    

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

Having $O(log_2n)$ as the asymptotic complexity for searching for a specific element in a binary search tree of 1000 elements in 5 seconds has the same logarithmic growth for 10,000 elements. So, $ 5 secs / $log_2(1000)$ = $x / log_2(10,000)$ = $5 * log_2(10,000) / log_2(1000)$. 5*13.29= 66.44  $log_2(1000)$ = 9.97. (66.44/9.97) = 6.7 secs to find the same element in the tree with 10,000 items.


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  
  1.The asymptotic anaylisis is $log_n$ for a binary tree. If we assume that the element is near the begining of the tree and also assume good implentation then theoretically it should take around 6.7 secs. If the tree is not balanced, then the height of the tree could be larger then $log_2(n)$ and doesn't grow logarithmically. This is a reason why it could take 100 secs.

  2. Computing hardware is an obvious reason this could happen. If you run the same search on two different machines with different specs then this could cause the difference in analysis because the hardware is not taken into account for the asymptotic complexity. This is becuase we assume that each comparison in the binary tree takes the exact same amount of time. 

  3.If the tree is also not implemented correctly then it could cause it to do unnescessary rebalancing and redundant checks that would cause the significant time increase.

Add your answers to this markdown file.

https://www.geeksforgeeks.org/complexity-different-operations-binary-tree-binary-search-tree-avl-tree/

https://uwyo.instructure.com/courses/593273/files/folder/slides?preview=86250260 (Slide 55)

class topics and notes

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
