# Distributed MapReduce Engine with Hash Partitioning

## Project Overview

This project implements the **MapReduce programming model from scratch using Python**. It simulates the complete Hadoop MapReduce workflow, including input splitting, mapping, partitioning, shuffle & sort, and reducing. The system processes an input text file and calculates the frequency of each word using multiple mapper and reducer processes.

---

## Objective

The objective of this project is to understand the internal working of the MapReduce framework without using Hadoop. It demonstrates how distributed processing can be implemented using Python by dividing work among multiple mapper and reducer processes.

---

## Project Structure

```
Project/
│── input.txt
│── main.py
│── mapper.py
│── partition.py
│── reducer.py
│── intermediate/
│── output/
│── README.md
```

---

## Files Description

### main.py
Acts as the driver program.

Responsibilities:
- Reads the input file
- Splits the input into chunks
- Executes mapper processes
- Partitions intermediate output
- Performs shuffle and sort
- Executes reducer processes
- Stores the final output

---

### mapper.py

Reads words from standard input and emits key-value pairs.

Example:

Input

```
Arun Priya Kumar
```

Output

```
Arun    1
Priya   1
Kumar   1
```

---

### partition.py

Implements a custom hash partitioner.

Responsibilities:
- Computes hash values
- Distributes words among reducer partitions
- Ensures the same key always reaches the same reducer

---

### reducer.py

Reads sorted intermediate key-value pairs and computes the total count for each word.

Example

Input

```
Arun    1
Arun    1
Arun    1
```

Output

```
Arun    3
```

---

## MapReduce Workflow

1. Read Input File
2. Split Input Data
3. Execute Mapper Processes
4. Generate Key-Value Pairs
5. Partition Mapper Output
6. Store Intermediate Files
7. Shuffle and Sort
8. Execute Reducers
9. Generate Final Output

---

## Technologies Used

- Python 3.x
- os
- sys
- shutil
- subprocess
- hashlib

---

## Input Dataset

Example input

```
Arun Priya Kumar Arun Divya Kumar Priya Arun
Karthik Divya Arun Suresh Priya Kumar Karthik
Meena Arun Suresh Divya Karthik Priya Meena Arun
Kumar Meena Karthik Suresh Arun Divya Priya
Suresh Kumar Meena Arun Karthik Divya Suresh
Priya Arun Meena Kumar Suresh Karthik Divya
Arun Divya Priya Karthik Meena Suresh Kumar
Kumar Arun Priya Divya Meena Karthik Suresh Arun
```

---

## Expected Output

```
Arun      10
Priya      8
Divya      7
Karthik    7
Kumar      7
Suresh     7
Meena      6
```

The output is stored inside the **output** directory.

---

## How to Run

Clone the repository.

Run the driver program.

```
python main.py
```

The program automatically performs:

- Input Splitting
- Mapping
- Partitioning
- Shuffle & Sort
- Reducing

Final results are generated inside the output folder.

---

## Features

- Custom MapReduce implementation
- Multiple Mapper Processes
- Multiple Reducer Processes
- Custom Hash Partitioner
- Shuffle and Sort
- Intermediate File Generation
- Word Count Analysis
- Modular Python Code
- Easy to Extend

---

## Applications

- Big Data Processing
- Word Frequency Analysis
- Text Mining
- Log Processing
- Hadoop Streaming Concepts
- Distributed Computing
- Educational Demonstration

---

## Advantages

- Lightweight implementation
- Easy to understand
- Modular architecture
- Demonstrates Hadoop concepts
- Supports multiple mapper and reducer processes
- Custom partitioning logic

---

## Future Enhancements

- Dynamic number of reducers
- Combiner implementation
- Fault tolerance
- Multi-machine execution
- GUI dashboard
- Performance visualization
- Large dataset support

---

## Conclusion

This project successfully demonstrates the complete MapReduce workflow using Python. It simulates Hadoop's processing model by dividing input data among multiple mapper processes, partitioning intermediate key-value pairs using a custom hash function, performing shuffle and sort, and finally reducing them to produce the total word frequencies. The project provides a practical understanding of distributed data processing and the core principles behind the MapReduce programming model.

---


**SAN**

BCA Student | Python Developer | Full Stack Developer
