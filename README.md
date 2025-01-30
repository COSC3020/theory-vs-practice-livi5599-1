# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

Bullet 1

1. Asymptotic analysis is theoretical, as it describes algorithm behavior with a set of unspecific inputs.  Actual performance is empirical, as it describes algorithm behavior with a specific set of inputs.  The two are different, as actual performance depends on constants and machine performance, whereas asymptotic analysis ignores those factors.


2. Actual performance is affected by hardware, software, and the characteristics of the input data, whereas asymptotic analysis is primarily affected by the input size.  Asymptotic analysis is also affected by the characteristics of the input data, but in a theoretical sense, as it often analyzes best, worst, and average cases based on predefined assumptions about input behavior that don’t always align with real-world data patterns.  In comparison, actual performance takes into account real-world input characteristics such as specific distributions, clustering, or ordering of data.  Combining these real-world factors with hardware and software, they affect actual performance much more than the effect of the theoretical sense of input data characteristics on asymptotic analysis, which is why asymptotic analysis is primarily affected by the input size.

3. In addition to ignoring constants, asymptotic analysis also ignores lower-order terms, which can be misleading when compared to actual performance since when lower-order terms are accounted for, they can have a decent effect on the runtime.

Bullet 2

The time complexity depends on if the binary search tree is balanced or not.  If it is balanced, it has a best case of O(1) and an average and worst case of O(log(n)).  If it isn’t balanced, it has a best case of O(1), and an average and worst case of O(n).  When a binary search tree is unbalanced, that means that the element being searched for is either at the beginning or end of the list.  This is because the list must be cut in half several times in order to find the element, and each time the tree branches out means the list was cut in half.  This forms uneven branches, thus making an unbalanced tree.

For a balanced binary tree, finding the same element in a tree of 10,000 elements takes about 6.65 seconds in the worst case, which comes from multiplying 5 by log2(10,000)/log2(1,000).  For an unbalanced binary tree, finding the same element in a tree of 10,000 elements takes about 50 seconds in the worst case, which comes from multiplying 5 by 10,000/1,000. 

Bullet 3

1. It could have taken much longer because the tree was very unbalanced, meaning the algorithm has to go through most, if not all of the nodes.  This causes a large difference, as with a very unbalanced tree, the search time can approach O(n) instead of O(logn).  This alone doesn’t fully account for the large jump from 5 seconds to 100 seconds.  When combined with searching an unbalanced tree of 10,000 elements, the use of poorly implemented recursive calls would cause the runtime to be considerably longer.  An example of this is the use of redundant recursive calls.  A poorly implemented search may explore both the left and right subtrees when it is only necessary to explore one subtree.  This, especially when combined with an unbalanced tree, would cause the runtime to be much longer than expected.

2. Memory or caching issues could come into play.  With a larger tree, it may no longer fit entirely in the CPU cache, causing cache misses and slower memory access time.  As the algorithm continues to access nodes stored in slower memory, this could cause a significant increase in the search time.

3. If other processes were consuming large amounts of CPU, memory, or I/O resources while the search was running, this could greatly slow down the performance.  In addition, since the larger tree requires a large amount of memory, the system could start using virtual memory, leading to much slower performance compared to when searching a smaller tree.


I received help from ChatGPT on 1.3 and 2.  For 1.3, I asked ChatGPT the question listed in the assignment.  Regarding 2, ChatGPT gave me the number of seconds it can take to find an element in a balanced binary tree of 10,000 elements.

When adjusting 1.1, I got help from Jacob in lab.  He brought up how I should go into more detail about how they are different and how asymptotic analysis ignores constants.
When adjusting 1.3, I got help from ChatGPT.  I asked it the question asked in the assignment and used one of it's responses to help me add to my original response.
For 3, I got help from ChatGPT and Ali.  I asked how I could further elaborate on/edit my answer and used their responses to help me write my answers.

When adding to 2.1, I asked ChatGPT to give me an example of a binary search tree and to give a vague answer about how the tree represents binary search.  I did this so I could have a better understanding on how binary search trees work.  This then led me to my conclusion of a tree being unbalanced when the element being searched for is at the beginning or end of the list.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models.  All of the work is my own, except where stated otherwise.  I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

-----

I submitted this assignment last semester.
