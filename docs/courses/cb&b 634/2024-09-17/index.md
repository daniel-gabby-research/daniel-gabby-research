---
layout: default
parent: CB&B 634 Computational Methods in Informatics
grand_parent: Courses at Yale
title: "2024-09-17 Big Data and Parallel Algorithms"
nav_order: 23
discuss: true
math: katex
---

# Big Data and Parallel Algorithms
## 0. Learning Objectives
- Distinguish between big data analysis and traditional data analysis.
- Give examples of types of big data arising in health.
- Give examples of ethical challenges associated with big data in health care; identify strategies for preserving privacy.
Explain concepts of big data analysis, including hashing and probablistic data structures.
- Explain Amdahl's law and interpret its significance with modern HPCs with tens of thousands of processors or more.
- Implement basic parallel algorithms using Python multiprocessing.

## 1. Introduction to Big Data
### A. Key Characteristics (5 V's)
- **Volume**: Terabytes+ of data
- **Velocity**: Rapid creation rate
- **Variety**: Multiple data types (structured & unstructured)
- **Veracity**: Quality/accuracy of data
- **Value**: Actionability of insights

### B. Challenges
- Ethical considerations (Privacy, Consent, Bias, Truth)
- Storage challenges
- Data transport challenges
- Analysis challenges

## 2. Data Storage Solutions
### 2.1 Traditional Storage
- SSDs
- Tape storage

### 2.2 Database Types
#### Relational Databases
- Uses normalized tables with SQL
- Normal Forms (1NF, 2NF, BCNF)
- Multiple joins required

#### Document Databases (NoSQL)
- Denormalized structure
- Efficient for common queries
- Less efficient for non-indexed queries

### 2.3 Distribution Strategies
- Sharding: Distributes data across servers
- Replication: Creates data copies across machines
  - Reduces latency
  - Protects against data loss
  - Risk of inconsistency

## 3. Big Data Analysis Techniques
### 3.1 Hash Functions
- Maps data to numbers in known range
- Example: MD5 (not cryptographically secure)
- Universal Hashing concepts

### 3.2 Probabilistic Data Structures
#### Bloom Filters
- Approximate set membership
- Space-efficient
- Allows false positives
- No false negatives

#### Counting Bloom Filters
- Extension of regular Bloom filters
- Stores counts instead of bits
- Tracks frequency of items

### 3.3 Estimation Techniques
- Order statistics for unique items
- Flajolet-Martin algorithm
- HyperLogLog for cardinality estimation

## 4. Parallel Computing
### 4.1 Fundamentals
- Reasons for parallelization
  - Faster results
  - Larger problem solving
  - Memory distribution
  - Improved responsiveness

### 4.2 Performance Metrics
#### Amdahl's Law
- Maximum speedup: 1/(1-p + p/n)
- p: parallelizable portion
- n: number of processors

#### Scaling Types
- **Strong Scaling**: Fixed problem size
- **Weak Scaling**: Fixed work per processor

### 4.3 Python Multiprocessing
#### Basic Concepts
- Process creation and management
- Shared memory considerations
- Cache implications

#### Implementation Tools
- `multiprocessing.Process`
- `multiprocessing.Pool`
- Shared memory: `Value` and `Array`
- Manager objects for proxy objects

### 4.4 Best Practices
- Focus optimization efforts
- Ensure load balancing
- Minimize shared state
- Maintain result consistency
- Centralize output operations

## 5. Practical Considerations
- Evaluate necessity of parallel implementation
- Consider debugging complexity
- Account for setup and maintenance overhead
- Plan for scalability
- Monitor resource utilization