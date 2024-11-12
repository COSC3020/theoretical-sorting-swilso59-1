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

Testing: 
- To determine if the algorithm operates in linear time.
- I would use a set of test cases to check if the algorithm's runtime scales proportionally with an increasing input size.
- These inputs would be arrays of various input types.
- Some of the case types I would use would be an already sorted array, reverse sorted array, a randomly generated array, array with 
  duplicate values, and an empty array.
- Each of these input types would be tested with different sizes to observe the runtime scaling as the input sizes increase.
- This would allow us to see if the runtime acts in a manner greater than $O(n)$. 

Argument: 
- Since our sorting algorithm is based on comparisons.
- I would assume that the algorithms would be subject to the same limitations as any comparison based sorting algorithms. 
- In a comparison-based sorting algorithm sorting can be visualized as a decision tree.
- "Each comparisons acts a choice point" that branches out into 2 possibilities based on the outcome of the comparison.
- This is what gives us the decision tree model.
- For an input of $n$ elements "There are $n!$ possible output orderings".
- The algorithm must be able to distinguish among all permutations to sort correctly.
- Each permutation would be a path in the decision tree.
- The height of this tree is the minimum number of comparisons in the worst-case scenario which is at least " $\log_{2}(n!)$ ".
- This height is a theoretical lower bound on the number of comparisons for sorting.
- $\log_{2}(n!)$ approximates to $n\log_{2}(n)$.
- This means the lower bound on comparisons for any comparison-based sorting algorithm is
  $\Omega(n\log(n))$.
- This shows us that getting a time complexity of $O(n)$ through comparisons alone is not possible "according to 
  Stirling's approximation".


## Plagiarism Acknowledgment

In this Assignment. For the testing I had a decent idea of how I would go about it since I had worked with testing and comparing runtimes with expected growth rates and checking against different implementations. I took the information from the question prompt and reviewed the sorting slides. These helped me understand the limitations of comparison-based sorting.

I used the lecture01-sorting.pdf on slides 40-45 for the theoretical argument portion.
and mergesort-swilso59-2 for the verification portion.

“I certify that I have listed all sources used to complete this exercise, including the use
of any Large Language Models. All of the work is my own, except where stated
otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is
suspected, charges may be filed against me without prior notice.”
 


  
  
