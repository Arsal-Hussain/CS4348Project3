## 2025-05-05 11:45pm

Started Project 3: B-Tree index manager.

Goal: Implement a file-based B-Tree index system that supports `create`, `insert`, and `search`. 
Initial version (`project3.py`) already supports those 3 commands without node splitting.
Plan: 
- Make a Git repo to track all changes.
- Add more commands (`print`, `extract`, `load`) later.
- Handle node splitting next.
## 2025-05-06 4:20pm

Using BTree stored in a binary file with with block based IO and strict memory limits. Going to use Python for simplicity. Planning to only load 1–3 blocks in memory at a time, as per spec.

Initial plan: 
- Set up the basic structure
- Implement the `create` command and header logic
- Make sure files initialize correctly with the header format

## 2025-05-06 4:30pm

Implementing node splitting will be tricky with limited memory. Will focus on basic root insertion today. Might create a helper class `BTreeNode`.

Session plan:
- Implement the `insert` command
- Create and write a single root node
- Prevent duplicate keys
- No splitting yet — just insert if space allows
- look into `load` command

## 2025-05-06 4:40pm

Program now supports the load feature, and has been tested with sample input.csv file which was then searched on the test.idx successfully.

Session plan:
- implement `print` command to dump current index entries to stdout

## 2025-05-06 4:50pm

Program now supports the print feature, tested after the load of the csv file and successfully shows each root and number assigned to it.

Session plan:
- implement `extract` command to write all entries into a csv file

## 2025-05-06 5:00pm

Program now supports the extract feature, tested after using test.idx file to create output.csv, with all the roots and numbers separated by comma.

Session plan:
- Check all commands and verify it is working.

## 2025-05-06 5:05pm

All commands working successfully.

Session plan:
- Doing node splitting