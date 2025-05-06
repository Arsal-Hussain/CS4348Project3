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

