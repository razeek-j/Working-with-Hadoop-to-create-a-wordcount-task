# Hadoop Word Count

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Overview

The Hadoop Word Count project demonstrates a classic example of utilizing Hadoop's MapReduce paradigm to process a pre-processed text file. This project aims to count the occurrences of each word within the provided text, displaying the frequency of each word's appearance.

## Introduction

In the world of big data, Hadoop has emerged as a powerful tool for distributed computing tasks. The Word Count program is often considered the "Hello, World!" equivalent in Hadoop, illustrating the core principles of MapReduce.

## Project Flow

### Data Preprocessing

1. **Input Text File**: Prepare a text file with pre-processed data containing paragraphs with words separated and cleaned (no punctuation). This file serves as the input data for the Word Count program.

### MapReduce Job Execution

2. **Map Task**:
   - **Mapper Class**: The Mapper reads the input text file and tokenizes it into words.
   - **Key-Value Pair Emission**: Each word is emitted as a key-value pair, with the word as the key and an initial count of 1.

3. **Shuffle and Sort Phase**:
   - **Intermediate Data**: The emitted key-value pairs are shuffled and sorted based on the word keys to prepare for the Reducer task.

4. **Reduce Task**:
   - **Reducer Class**: The Reducer task aggregates the intermediate key-value pairs, grouping identical words together.
   - **Count Aggregation**: It sums up the counts for each word, calculating the total occurrences.

### Output Generation

5. **Final Output**:
   - **Output File**: The final output file displays each unique word along with its count, showcasing the frequency of occurrence for each word in the input text file.

## Usage

### Prerequisites
- Ensure Hadoop is installed and configured properly on your system.

### Execution Steps
1. **Input Preparation**: Provide the pre-processed text file containing words without punctuation.
2. **Hadoop Command**: Run the Hadoop Word Count program using the appropriate command-line syntax, specifying the input and output paths.
3. **Result Retrieval**: Access the generated output file containing word counts for analysis and further processing.

## Project Structure

- **Mapper Class**: Handles the tokenization of words and emits key-value pairs.
- **Reducer Class**: Aggregates word counts and produces the final output.
- **Input File**: Contains pre-processed text data without punctuation.
- **Output File**: Shows each word and its count, indicating the frequency of occurrence.

## License

This project is licensed under the MIT License. For more details, refer to the [LICENSE](LICENSE) file.

## Contact

For any inquiries or additional information, feel free to contact the developers at [Your Email Address].
