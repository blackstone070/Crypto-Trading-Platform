**Crypto-Trading-Platform: Devesh Simulation**
A high-performance C++ simulation of a cryptocurrency trading platform. This project implements a full order book system, a matching engine for bids and asks, and a wallet management system to track assets across trades.

** Features**
Order Book Management: Efficiently stores and sorts market orders using std::vector and custom sorting algorithms.

Matching Engine: Implements a price-time priority algorithm to match buyers (bids) and sellers (asks) based on compatible price points.

Wallet System: A secure asset management class using std::map<std::string, double> to handle multiple currencies and validate transaction sufficiency.

CSV Data Integration: High-speed parsing of historical market data from CSV files.

Error Handling: Robust input validation using C++ exceptions and logical flow control to prevent invalid trades or negative balances.

**Technical Implementation**
Key Components
OrderBook: The core data structure that manages all market entries.

Wallet: Handles currency insertion, removal, and balance checking.

CSVReader: A utility class designed to transform raw log data into OrderBookEntry objects.

DeveshMain: The primary controller that handles the terminal user interface and program flow.

Logic Highlights
Static vs Non-Static: Utilizes static functions for utility tasks that don't require object state and non-static functions for instance-specific operations.

Optimized Sorting: Uses a pipeline of appending new orders to the end of the collection followed by a chronological sort to ensure market integrity.

** Prerequisites**
To run this simulation, you will need:

A C++ compiler (GCC/MinGW, Clang, or MSVC)

Standard Template Library (STL) support

 **Installation & Running**
Clone the repository:

git clone https://github.com/blackstone070/Crypto-Trading-Platform.git


Navigate to the source directory:
cd Crypto-Trading-Platform/src


Compile the project:
g++ main.cpp OrderBook.cpp OrderBookEntry.cpp CSVReader.cpp Wallet.cpp DeveshMain.cpp -o DeveshSim
Run the simulation:

./DeveshSim
**Testing**
The platform was tested using:
Unit Tests: Hard-coded datasets were used to verify the Wallet and Matching Engine logic in isolation.
Edge Case Verification: Handled zero-value initializations and negative amount exceptions to ensure system stability.
