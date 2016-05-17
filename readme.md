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

## What is it?

Here's the basic idea of the bubble sort algoritm:
  1. start at the beginning of a list (array) of items
  2. compare the item you're looking at to the next item in the list
  3. if this item is greater than the next one, swap them
  4. move on to the next item
  5. repeat steps 1-4 until you go through the whole list without doing any swaps


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
