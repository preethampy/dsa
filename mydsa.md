## Algorithm
It is a set of well-defined instructions to solve a particular problem.

## Characteristics of Algorithm
1) Well defined inputs and outputs
2) Each step should be clear and unambiguous
3) Language independent

## Why Algorithms ?
As a developer we are going to come accross problems that we need to solve. Learning algo's means learning different techniques to efficiently solve those problems. One problem could be solved in many ways using different algo's. Every algo comes with its own tradeoffs when it comes to performance.

## Algorithm analysis
There are multiple ways to solve a problem.
Ex: There are multiple ways/algo's to sort a list of numbers.
### How do we analyse which one of them is the most efficient algorithm ?
The absolute running time of an algorithm cannot be predicted, since it depends on a number of factors like below:
1. Programming language used to implement the algorithm
2. The computer the program runs on
3. Other programs running at the same time
4. Quality of the operating system

Keeping these points in mind, we evaluate the performance of an algorithm in terms of its **input size**. The evaluation is of two types:
1. **Time complexity** - Amount of time taken by an algorithm to run, as a function of input size
2. **Space complexity** - Amount of space taken by an algorithm to run, as a function of input size

> Note: We do not consider the time taken by an algo/code to run as it is dependent on the machine, programming language etc, but the time taken when the input size changes of an algo/code.

> Ref: The Time Complexity of an algorithm/code is not equal to the actual time required to execute a particular code, but the number of times a statement executes. 

> Ref-2: Instead of measuring actual time required in executing each statement in the code, Time Complexity considers how many times each statement executes. 

### How to represent complexity ?
We use **Asymptotic notations**, which are mathematical tools to represent time and space complexities.
1. Big-O notation (O-notation) - Worst case complexity
2. Omega notation (Ω-notation) - Best case complexity
3. Theta notation (θ-notation) - Average case complexity

#### Big-O notation
It describes the complexiy of an algorithm using algebraic terms.
It has two characteristics:
1. It is expressed in terms of the input
2. It focuses on the bigger picture without getting caught up in the minute details

Let's take below example of code:
```
function summation(n){ --------> n=4
    let sum = 0; ----------> this statement executes 1 time
    for(let i=1; i<=n; i++){
        sum = sum+i; ----------> this statement executes 4 times
    }
    return sum; ----------> this statement executes 1 time
}

summation(4);
// Outputs: 10
```
- The total count of how many times all the statements get executed is 4(from for loop, which is the input "n" given to that function), plus 2 other statements
- So, we can write it as n+2, as n is the given input and other 2 are from function itself.
- For now, we have n=4, it can also be n=1000000000000000. So it doesnt make sense to add 2 to it, instead we can just say it as "n" as the value of 2 in 1000000000000002 is insignificant and we can drop it.
- Our time complexity is dependent on the input size (hence point 1)
- Hence, The time complexity of our summation algorithm above is ***O(n) - Linear (As the input size increases, time-complexity increases)***
- Anytime we see a loop in an algorith, most of the times, the time complexity is atleast O(n) Linear.

Let's consider another example:
```
function summation(n){
    return (n * (n+1)) / 2;
}
```
- Time complexity of above function is O(1) - Constant, because it always has only one statement to execute irrespective of input size.
- 
```
for(let i=0; i<10; i++){
    for(let j=0; j<10; j++){
      // Time complexity = O(n^2) - Quadratic  
    }
}

If input size reduces by half every iteration = Time complexity is O(logn) - Logarithmic
```














