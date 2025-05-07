# CS4348 Project 3 – B-Tree Index Manager

## Overview
This project implements a disk-based B-tree index system using fixed-size 512-byte blocks. It supports insertion, search, bulk loading from a CSV, printing contents in order, and extracting the index to a CSV file.

The B-tree uses a minimum degree (`t`) of 10, with each node supporting up to 19 keys and 20 children. Blocks are written and read in big-endian format.

Please note: the input.csv file has been included in submission to be used to load, but the test.idx file and output.csv must be generated through the commands.

## Commands

```bash
# Create a new index file
python project3.py create test.idx

# Insert a single key-value pair
python project3.py insert test.idx 15 100

# Search for a key
python project3.py search test.idx 15

# Load key-value pairs from a CSV file (format: key,value)
python project3.py load test.idx input.csv

# Print all key-value pairs in order
python project3.py print test.idx

# Extract key-value pairs to a CSV file
python project3.py extract test.idx output.csv
