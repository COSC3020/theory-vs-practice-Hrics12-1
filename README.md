# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  1. We drop the lower order terms when doing asymptotic analysis and these could have actual impact on prefomance in real practice. 
  2. In asymptotic analiysis we treat all constants at the same rate. When in practice constants can take different amounts of time. Like comparing strings takes longer then comparing integers.
  3. Input size also makes a difference. If you look that the lecture slides and see the graph for "Average case running times" you see that Timsort takes a longer amount of time to sort a list size of ≈62500 items then heap sort. Then the amount of time levels out between the two sorting types before timsort rises, timsort again take more time as the list size grows. This shows that when you take bounds for asymptotic analysis, it will not always reflect what the best algorithm is for each individuel case when using it in practice. 

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.



- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.
