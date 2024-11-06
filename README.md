This project implements advanced caching techniques for improving database query performance. It uses multiple levels of cache (L1, L2, L3) to optimize data retrieval. The project benchmarks the performance of inserting and retrieving data from the database and various caching layers.
Features
•	Multi-level Caching: Implements three levels of cache:
o	L1 Cache: Local in-memory cache (LinkedHashMap).
o	L2 Cache: Guava Cache with expiration time.
o	L3 Cache: Database (MySQL).
•	Concurrency Support: Uses Java's ExecutorService for concurrent operations, simulating multiple threads performing data operations simultaneously.
•	Database: MySQL database is used to store and retrieve data.
•	Benchmarking: Measures and benchmarks the performance of database insert, retrieve, and cache operations.
Technologies Used
•	Java 8+ (for multithreading and concurrent operations)
•	MySQL (for database storage)
•	Guava (for L2 caching)
•	JDBC (for database interaction)
•	ExecutorService (for concurrent operations)
Project Structure
├── src
│   ├── main
│   │   ├── java
│   │   │   ├── com
│   │   │   │   └── example
│   │   │   │       └── AdvancedDatabaseCachingBenchmarkThread.java
│   ├── resources
│   │   ├── application.properties (optional, for configuration)
└── pom.xml (Maven project file)
Requirements
•	Java: 8 or above
•	MySQL: Database server
•	Guava: For caching (added via Maven dependency)
Setup
1.	Clone the repository:
git clone https://github.com/Udaya-raman/Advanced-caching-project.git
2.	Database Setup:
o	Create a MySQL database named testdb.
o	Run the following SQL query to create the test_table:
CREATE TABLE IF NOT EXISTS test_table (
    id INT PRIMARY KEY,
    value VARCHAR(255)
);
3.	Maven Setup:
o	Open the project in your IDE (e.g., IntelliJ IDEA, VS Code).
o	Run the following command to install dependencies:
                           mvn install
4.	Run the Project:
You can run the AdvancedDatabaseCachingBenchmarkThread.java class directly, which will execute the benchmarking tests.
5.	View Benchmark Results:
After running the program, the console will display the time taken for various operations (database insert, cache insert, retrieve from L1, L2, and multilevel caches).
Sample Output – 


