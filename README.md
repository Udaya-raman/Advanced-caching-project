# Advanced Caching Benchmark Project

This project demonstrates the implementation of advanced caching techniques to improve database query performance. By utilizing multiple levels of cache (L1, L2, L3), the project optimizes data retrieval processes, benchmarks performance, and simulates various caching operations.

## Features

### Multi-level Caching:
- **L1 Cache**: Local in-memory cache implemented using a `LinkedHashMap` for fast access to frequently queried data.
- **L2 Cache**: Guava Cache with automatic expiration to efficiently store data in memory with a configurable TTL (Time to Live).
- **L3 Cache**: A MySQL database serves as the fallback storage, allowing persistent storage of data when the cache layers are bypassed.

### Concurrency Support:
- Uses Java’s `ExecutorService` to simulate concurrent operations, handling multiple threads performing data operations in parallel for performance testing.

### Benchmarking:
- Measures the time taken for inserting and retrieving data from the database and cache layers (L1, L2, L3), providing insights into the effectiveness of caching in performance optimization.

## Technologies Used

- **Java 8+**: For multithreading and concurrent operations using `ExecutorService`.
- **MySQL**: Used as the database for persistent data storage.
- **Guava**: Provides L2 caching functionalities with expiration time.
- **JDBC**: Facilitates communication with MySQL for database interactions.
- **ExecutorService**: Enables concurrency by simulating multi-threaded access to the cache and database.

## Requirements

- **Java**: Version 8 or above
- **MySQL**: Database server
- **Guava**: Library for L2 caching (included as a Maven dependency)
- **Maven**: For dependency management and building the project

## Setup Instructions

### 1. Clone the repository:
Clone the repository to your local machine using the following command:

```bash
git clone https://github.com/Udaya-raman/Advanced-caching-project.git

## 2. Database Setup:
Create a MySQL database named testdb.
Run the following SQL query to create the test_table:
CREATE TABLE IF NOT EXISTS test_table (
    id INT PRIMARY KEY,
    value VARCHAR(255)
);

## 3. Maven Setup:
Open the project in your favorite IDE (e.g., IntelliJ IDEA, VS Code).
Install the project dependencies by running the following command:
mvn install

## 4. Run the Project:
You can directly run the AdvancedDatabaseCachingBenchmarkThread.java class to execute the benchmarking tests. This will initiate the caching operations and the database interactions.

## 5. View Benchmark Results:
After running the project, the console will display the time taken for various operations:
Database insert operations.
Cache insert operations (L1, L2, and L3).
Retrieval times from the L1, L2, and multi-level caches.
