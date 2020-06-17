[slide]
# Algorithmic Complexity

**Algorithm complexity** is a **measure** which evaluates the order of the **count of operations**, performed by a given algorithm as a function of the size of the input data.

In other words, **complexity** is a rough **approximation of the number of steps** necessary to execute an algorithm.

When we evaluate complexity we speak of **order of operation count**, not of their exact count.

Algorithm complexity is commonly represented with the **O(f) notation**, also known as **asymptotic notation** or **"Big O notation"**, where **f** is the function of the size of the input data.

The asymptotic computational complexity **O(f)** measures the order of the consumed resources (CPU time, memory, etc.) by certain algorithm expressed as function of the input data size.

Complexity can be **constant**, **logarithmic**, **linear**, **n*log(n)**, **quadratic**, **cubic**, **exponential**, etc.

This is respectively the order of constant, logarithmic, linear and so on, number of steps, are executed to solve a given problem.

For simplicity, sometime instead of **"algorithms complexity"** or just **"complexity"** we use the term **"running time"**.

# Typical Algorithm Complexities

This table will explain what every type of complexity (running time) means:

| **Complexity** | **Running time** | **Description** |
| --- | --- | --- |
|  constant   |    O(1)      | It takes a constant number of steps for performing a given operation (for example 1, 5, 10 or other number) and this count does not depend on the size of the input data. |
| logarithmic |  O(log(N))   | It takes the order of log(N) steps, where the base of the logarithm is most often 2, for performing a given operation on N elements. |
|   linear    |    O(N)      | It takes nearly the same amount of steps as the number of elements for performing an operation on N elements. |
|  quadratic  |    O(n^2)     | It takes the order of N^2 number of steps, where the N is the size of the input data, for performing a given operation.  For example if N = 100, it takes about 10,000 steps. |
|   cubic     |    O(n^3)     | It takes the order of N^3 steps, where N is the size of the input data, for performing an operation on N elements. For example, if we have 100 elements, it takes about 1,000,000 steps. |
|exponential|O(2^N)| It takes a number of steps, which is with an exponential dependability with the size of the input data, to perform an operation on N elements. For example, if N = 10, the exponential function 2N has a value of 1024, if N = 20, it has a value of 1 048 576, and if N = 100, it has a value of a number with about 30 digits.|





[/slide]