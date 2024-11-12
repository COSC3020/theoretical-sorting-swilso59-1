# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

## Answer 

Testing: To determine if the algorithm operates in linear time. I would use a set of test cases to determine if the algorithm's runtime scales propotionally with an increasing input size. These inputs would be arrays of various input types. Some of the cases I would use would be an already sorted array, reverse sorted array, a randomly generated array, array with duplucate values, and a empty array. Each of these input types would be tested with different sizes to observe the runtime scaling as the input sizes increase. Each of these tests would be conducted multiple time to get an average runtime. 



Since our sorting algorithm is based on comparisons. I would assume that the algorithms would be subject to the same limitations as any comparison based sorting algorithms. 
- In a comparision-based sorting algorithm sorting can be visualized as a decision tree. "Each comparisons acts a choice point"
  that branches out into 2 possibilities based on the outcome of the comparison. This is whata gives us the decision tree model.
- For an input of $n$ elements. "There are $n!$ possible output orderings". The algorithm must be able to distinguish among all 
  permutations to sort correctly, so each permutation would be a path in the decision tree.
- The height of this tree is the minimum number of comparisions in the worst-case senario which is at least "$\log_{2}(n!)$".
- This height is a theoretical lower bound on the nubmer of comparisons for sorting.
- $\log_{2}(n!)$ approximates to $n\log_{2}(n)$. This means the lower bound on comparisons for any comparison-based sorting algorithm is
  $\Omega(n\log(n))$. This shows us that getting a time complexity of $O(n)$ through comparisons alone is not posibble "according to 
  Stirlings approximation".

  
  
