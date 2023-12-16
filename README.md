# CS 466 - Implementation of Global Alignment Algorithms
Final Project for CS 466 Fall 2023

**Group Members:** Rayna Patel and Sreenidhi Vijayaraghavan

## Overview
Global alignment is a crucial task in the field of bioinformatics and it allows for the comparison of sequences of DNA, RNA, or proteins to identify similarities between them. This process is used in bioinformatics for various evolutionary and functional analyses. In this project, we delve into two of the most prominent global alignment algorithms - Needleman-Wunsch and Hirschberg, and we compare the differences in performance between them.

The Needleman-Wunsch algorithm is a dynamic programming method commonly utilized for global sequence alignment. It boasts a time complexity of O(m×n) where m and n represent the lengths of the two input sequences. The space complexity is also O(m×n) due to the creation of a two-dimensional matrix designed for scoring purposes that is part of the algorithm. Needleman-Wunsch was one of the first widely used global alignment algorithms, and it serves as the baseline for this project.

The Hirschberg Algorithm is a spinoff of the Needleman-Wunsch algorithm and specializes in minimizing the space used during computation. While its time complexity mirrors that of Needleman-Wunsch i.e. O(m×n), it has an achieved space complexity of O(min(m,n)) and thus makes for a more space-efficient option. 

We found that the Needleman-Wunsch algorithm's execution time scaled quadratically with escalating input sizes, which is in line with its dynamic programming nature. Meanwhile, while Hirschberg's time complexity was identical, occasionally Hirschberg algorithm manifested quicker execution times due to its streamlined space representation, which became more  noticeable for larger input sizes. The Hirschberg algorithm also consumed considerably less memory, proving advantageous for sizeable input sequences.


### How to run the code

You can download and open the .ipynb file which contains all the code used for this project. Running all cells in the notebook will result in plots similar to the ones shown in our results below, with some differences present due to changes in the randomly generated sequences.

The main functions in our code include the following:
1. _generate_random_sequence_ - Function to generate a random sequence of strings of the four nucleotide bases—adenine (A), thymine (T), cytosine (C), and guanine (G) based on the given input length
2. _hirschberg_ - Implementation of the space-efficient Hirschberg algorithm
3. _global_align_needleman_wunsch_ - Implementation of the Needleman-Wunsch algorithm as referenced from HW1 of CS466 in the Fall 2023 semester.
4. _find_memory_and_time_ - Function to measure the peak memory usage and execution time of a specified function with given arguments. The function employs the memory_usage function from the memory_profiler module to monitor memory usage during the execution of the target function. The function also records the start and end times using the timeit library for higher accuracy in time measurements.

## Results

**Time taken for the Needleman-Wunsch and Hirschberg Algorithms**
<img width="664" alt="Screenshot 2023-12-15 at 9 42 31 PM" src="https://github.com/sreenidhi2002/Global_Alignment_Algorithms/assets/55078126/c17a5526-918c-4cfc-98a6-8262b29377ce">

**Memory used by the Needleman-Wunsch and Hirschberg Algorithms**
<img width="651" alt="Screenshot 2023-12-15 at 9 42 39 PM" src="https://github.com/sreenidhi2002/Global_Alignment_Algorithms/assets/55078126/d3c3cbd6-77f0-42e9-b9c3-a4156b9f075e">


