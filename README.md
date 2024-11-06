This project implements advanced caching techniques for improving database query performance. It uses multiple levels of cache (L1, L2, L3) to optimize data retrieval. The project benchmarks the performance of inserting and retrieving data from the database and various caching layers.

Features
Multi-level Caching: Implements three levels of cache:

L1 Cache: Local in-memory cache (LinkedHashMap).
L2 Cache: Guava Cache with expiration time.
L3 Cache: Database (MySQL).
Concurrency Support: Uses Java's ExecutorService for concurrent operations, simulating multiple threads performing data operations simultaneously.

Database: MySQL database is used to store and retrieve data.

Benchmarking: Measures and benchmarks the performance of database insert, retrieve, and cache operations.

Technologies Used
Java 8+ (for multithreading and concurrent operations)
MySQL (for database storage)
Guava (for L2 caching)
JDBC (for database interaction)
ExecutorService (for concurrent operations)

Setup
Clone the repository:

bash
Copy code
git clone https://github.com/Udaya-raman/Advanced-caching-project.git
Database Setup:

Create a MySQL database named testdb.

Run the following SQL query to create the test_table:

sql
Copy code
CREATE TABLE IF NOT EXISTS test_table (
    id INT PRIMARY KEY,
    value VARCHAR(255)
);
Maven Setup:

Open the project in your IDE (e.g., IntelliJ IDEA, VS Code).

Run the following command to install dependencies:

bash
Copy code
mvn install
Run the Project:

You can run the AdvancedDatabaseCachingBenchmarkThread.java class directly, which will execute the benchmarking tests.

bash
Copy code
mvn exec:java -Dexec.mainClass="com.example.AdvancedDatabaseCachingBenchmarkThread"
View Benchmark Results:

After running the program, the console will display the time taken for various operations (database insert, cache insert, retrieve from L1, L2, and multilevel caches).

Sample Output-
Database Insert Time: 224162895900 nanoseconds
Database Retrieve Time: 26760484900 nanoseconds
L1 Cache Insert Time: 148051500 nanoseconds
L1 Cache Retrieve Time: 116816700 nanoseconds
L2 Cache Insert Time: 319569600 nanoseconds
L2 Cache Retrieve Time: 141539800 nanoseconds
Multilevel Cache Retrieve Time: 515089000 nanoseconds

Process finished with exit code 0

