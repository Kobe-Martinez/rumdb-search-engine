# RUMDb Search Engine

The RUMDb Search Engine is a Java-based project designed to function as a lightweight search engine for a database of movies. It focuses on efficient keyword-based searches within movie descriptions using a hash table to store and index the data. The hash table maps each word found in movie descriptions to the specific movies and locations where the word occurs. Noise words, such as "the" or "and," are filtered out during this process to ensure meaningful results.

The search engine allows users to query movies based on one or two keywords and ranks results based on how closely the queried words appear within the movie descriptions. It can calculate the minimum distance between the search terms and sort the results accordingly. Additionally, the search engine includes features like dynamic rehashing to maintain efficiency as the dataset grows.

This project is ideal for demonstrating concepts such as hashing, collision handling, word filtering, and data retrieval. It serves as a practical implementation of how search engines index and query data, showcasing efficient data structures and algorithms in Java.


## Table of Contents

- [Features](#features)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Requirements](#requirements)
- [File Outputs](#file-outputs)
- [License](#license)
- [Important Note](#important-note)

## Features

- **Hash Table Construction**
  
  - Maps words from movie descriptions to their occurrences in the movie database
    
  - Uses a hash function for efficient indexing and retrieval

- **Search Functionality**
  
  - Finds movies containing specified keywords in their descriptions
    
  - Ranks results based on the proximity of the search terms

- **Top Results**
  
  - Returns the top 10 most relevant movies for given keywords

- **Noise Word Filtering**
  
  - Ignores common words (e.g., "the," "and") during the indexing process

- **Dynamic Rehashing**
  
  - Automatically resizes the hash table when the load factor exceeds the threshold

## Usage

1. **Clone the Repository**
   
   ```bash
   git clone https://github.com/Kobe-Martinez/rumdb-search-engine.git
   ```

2. **Compile the Code**
   
   ```bash
   javac RUMDbSearchEngine.java
   ```

3. **Run the Program**
   
   - Initialize the search engine with a hash size, load factor threshold, and a file containing noise words
     
   - Use the insertMoviesIntoHashTable method to load movies from a data file
     
   - Perform searches with topTenSearch for relevant movie results


## Code Structure

- **RUMDbSearchEngine.java**
  
  - Core class for building the hash table and performing search operations
 
  - Contains methods for filtering words, inserting data, and searching

- **Hashing and Word Occurrences**
  
  - Implements a hash table to store words and their associated movie locations
 
  - Filters out noise words and non-alphabetic characters

- **Search and Ranking**
  
  - Supports multi-keyword searches and calculates the minimum distance between words in movie descriptions
    

## Requirements

- **Java**: Version 8 or higher


## File Outputs

- **Console Outpu**: Prints the hash table and search results, including the ranked movie titles

## License

This project is licensed under the MIT License. See the LICENSE file for details.


## Important Note

This project is designed for educational purposes to demonstrate hash table operations, search ranking, and noise word filtering in Java. It provides a practical example of building a small-scale search engine for structured data.
