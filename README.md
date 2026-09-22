# Lab 04 - SOP/POS and KMaps

In this lab, you’ve learned how to apply KMaps, Sum Of Products and Products of
sums to simplify digital logic equations. Then, you’ve proven out that they work
using an implemented design on your Basys3 boards.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Summary

- In this lab we learned how to effectively use K-maps, Sum of Products and Product of Sums to simplify boolean equations. We started by creating a naive equation from the truth table and then used a K-map to make the simplified equations. After implementing all three equations in Verilog files we uploaded our code to Vivado and tested our logic on a circuit board utilizing 3 LED's to produce outputs for all possible inputs and checking it against the truth table. We learned how K-maps can help simplify a large boolean equation and ensure it functions the same.

## Lab Questions

### Why are the groups of 1’s (or 0’s) that we select in the KMap able to go across edges?

- Groupings in a K-map can go across edges because the map is arranged in a way so that the cells only change by one variable. The first and last rows and columns are "neighbors" so that it wraps around and lets you make groups across the edge, so long as the cells are adjacent.

### Why are the names Sum of Products and Products of Sums?

- They are named this because of how the expressions are structured, Sum of Products is multiple products (which are just variables combined with AND) and they are then summed together or "OR'd" together which is the same thing as addition. Product of Sums is reverse, having variables that are summed together (OR) and then those terms are multiplied together (AND).

### Open the test.v file – how are we able to check that the signals match using XOR?

- Since XOR has an output of 0 when two inputs are the same, and 1 when inputs are different, we can XOR the outputs from our naive table, SOP and POS equations to check if there is a difference between them all. If XOR is 0, then the signals match. If XOR is 1, then at least one of the signals does not match. If we test all input combinations, then we can verify that all three of the implementations produce the same result.
