# Cached File I/O Library

This repository contains my implementation of a **user-level cached file I/O system**, developed as part of the **[CSCI 0300 (Fundamentals of Computer Systems)](https://csci0300.github.io)** course at Brown University. The project replaces direct system calls with a custom API that reduces disk I/O latency through software-level caching. You can find more information about the project [here](https://csci0300.github.io/assign/projects/project3.html](https://csci0300.github.io/assign/projects/project3.html).

---

## Project Overview

The caching library implements an API that mimics standard file I/O behavior while optimizing performance through a memory-resident cache. It supports:

- Reading (`io300_read`, `io300_readc`) and writing (`io300_write`, `io300_writec`) operations.
- File seeking with `io300_seek`.
- Transparent caching to reduce expensive system calls.
- Correctness and performance validation against standard `stdio`.

### Technical Highlights

- Built a fixed-size byte-level cache to buffer reads and writes.
- Tracked metadata including cache position, dirty state, and file offsets.
- Implemented lazy flushing and fetch-on-miss behavior.
- Optimized to stay within 5–10× performance of `stdio` on benchmark tests.
- Handled file edge cases like seeking past EOF and partial writes.

---

## Note
To comply with Brown’s academic code, this repository does not include the source code. If you are a potential employer and would like access to my implementation, please contact me at **mihnea_steiu@brown.edu**.
