<!--
Creator: <Name>
Market: SF
-->

![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

# Bubble Sort

## What are the objectives?
*After this workshop, developers will be able to:*

- Conceptualize Bubble Sort
- Physicalize Bubble Sort
- Write Bubble Sort

## Where should we be now?
*Before this workshop, developers should already be able to:*

- Write functions
- Use problem solving skills to think about algorithms

## Intro

Sorting is a common problem in interviews and in the real world. Algorithms sort books by title,  items by price, phone numbers by area code, etc.

There are many different sorting algorithms that excel in different circumstances.

The term "algorithm" is used in software development to describe a solution to a problem that will work in all or many programming languages, without going into the specifics of coding it in any particular language.

<a href="http://www.sorting-algorithms.com/" target="_blank">See a bunch of different sorting algorithms in action.</a>

## Why bubble sort?  

We'll look at a few different sorting algorithms, here's why to use bubble sort:

 - It is one of the simpler, more strait forward sorting algorithms
 - It works great on 'nearly sorted' data

## Why doesn't Obama think we should use it?

[source](https://www.youtube.com/watch?v=k4RRi_ntQc8)

- Bubble sort is exponential in its worst case speed, meaning an array of 100 items could take up to 100x as long to sort as a an array of 10 items.
- Bubble sort's worst case scenario is a reverse-sorted array.

###Sort the list using Bubble Sort: [5,4,2,3,1,6]

####Iteration 1
Look at the first two elements in the list.
	
0: [**5, 4**,2,3,1,6]  

Is 5 > 4 ? Yes! Swap!

If an element on the left (5) is greater than the element on the right (4), the two elements 'swap' locations

1: [4,**5,2**,3,1,6]  

2: [4,2,**5,3**,1,6]  

3: [4,2,3,**5,1**,6]  

4: [4,2,3,1,**5,6**]  


**Important:** We now know that the last element in the list is the largest element in the list. There's no need to do a comparison with that number ever again.


####Iteration 2

0: [**4,2**,3,1,5,~~6~~]

1:  [2,**4,3**,1,5,~~6~~]

2:  [2,3,**4,1**,5,~~6~~]

3:  [2,3,1,**4,5**,~~6~~]

Stop!

Remember: we know that last element is the largest number in the list.  There is no need to compare against that number ever again.  We also now know that the **second** to last number is the second largest number; no need to move that one ever again as well. (Detect a trend?)

###Iteration 3

0: [**2,3**,1,4,~~5,6~~]  

If an element on the left has met a larger or equal element, we look at its bigger neighbor and now compare the larger neighbor to it's neighbor on the right.  The process is continued until our established end.

1: [2,**3,1**,4,~~5,6~~]

2: [2,1,**3,4**,~~5,6~~]

Stop!

We don't stop sorting until we hit the end.  Even if we find 

###Iteration 4

0: [**2,1**,3,~~4,5,6~~]

1: [1,**2,3**,~~4,5,6~~]

Stop!

###Iteration 5
0: [**1,2**,~~3,4,5,6~~]

Stop!

When there is only one element (the first element) left in our unsorted list, it is already sorted for us as a freebie!

###List is now sorted using Bubble Sort: [1,2,3,4,5,6]

![](http://cdn2.crunchify.com/wp-content/uploads/2013/01/BubbleSort-Algorithm-Crunchify.jpg)

###Now write your own bubble sort!
####Hints:
If you want to swap two variables, a and b:

```javascript
var a, b, temp;
temp = a;
a = b;
b = temp;
```

You may use a conventional for loop.


## Visualizations

<a href="https://en.wikipedia.org/wiki/Bubble_sort#/media/File:Bubble-sort-example-300px.gif" target="_blank">From wikipedia</a>


<a href="https://www.youtube.com/watch?v=lyZQPjUT5B4&t=52" target="_blank">
From Romania</a> (you can watch on double speed).

## Drill!

* Work with a partner.

* Write on the whiteboard/tables. No computer code allowed!

* Start with pseudocode (English descriptions of what you want to do in the code).

* Test your work with the input/output pairs listed below!

**Create a `bubbleSort` function that takes in an array of numbers, uses the bubble sort algorithm on it, and returns the sorted array.**

Here are some input/output pairs you can use to test it:

| Input | Expected Output |
| :--- | :--- |
| `[0,1,2]` | `[0,1,2]` |
| `[8,5,3]` | `[3,5,8]` |
| `[]`  | `[]` |
| `[9,4,7,6]` |  `[4,6,7,9]` |

[sample solution](sample-solution.js)

## Thought Bubbles

_Because we can only make that pun once._

1. Why is it safe to stop looping through the array after you have a full pass through without swaps?  

1. How would you change your function to sort the array in the reverse order?

1. What are some basic requirements for bubble sort to work on an input array?  Would your code on the board with an input array like `["Thursday", 47, ['a','b','c']]`?

1. Bubble sort is known as a slower sorting algorithm for in many scenarios.   What is the best-case scenario for bubble sort? That is, what characteristic of an array causes bubble sort to do the least amount of swaps?  How many swaps would bubble sort do on one of these arrays?  

1. What is the worst case scenario for bubble sort?  (What kind of arrays cause it to do the most swaps?)  



[sample answers](thought-bubbles.md)

## Closing Thoughts
- Bubble sort is a decent search algorithm and learning it helps one think about algorithms and time optimization.
- Bubble sort performs great for nearly-sorted arrays, and terribly for reverse-sorted arrays.
- While it is highly unlikely that a junior developer would be asked to implement a sort algorithm from scratch, being thoughtful about sorting algorithms and practicing breaking problems down is an indispensable skill!
