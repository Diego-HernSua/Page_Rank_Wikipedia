# 🌐 PageRank with Apache Spark (Massive Computing)

This project focuses on the creation and implementation of the **PageRank** algorithm using **Apache Spark** within the **Databricks** environment. The objective is to efficiently compute the ranking of web pages based on the link structures derived from Wikipedia.

---

## 📚 Understanding PageRank

**PageRank** is a cornerstone algorithm developed by Larry Page, one of Google's founders, to evaluate the importance of web pages. It is widely used by search engines like Google to rank pages in their search results.

### How PageRank Works:
- **Initial Assignment**: Every web page starts with an initial rank.
- **Rank Distribution**: This rank is distributed across all the outbound links of the page.
- **Iterative Recalculation**: The ranks are recalculated iteratively, where a page's new rank depends on the ranks of the pages linking to it.
- **Convergence**: Over several iterations, the algorithm stabilizes, resulting in a final ranking that reflects the importance of each page.

### Key Concept:
The essence of PageRank lies in the idea that links from important pages (high-ranked) contribute more to the rank of the pages they link to.

---

## 💻 Implementation Overview

The implementation process is broken down into several stages to ensure efficient computation and accurate results:

### 1. **Dataset Exploration**
   - **Source**: Wikipedia dataset
   - **Key Fields**: "title," "id," and "text"
   - **Objective**: Understand the structure and content, focusing on extracting meaningful link connections between pages.

### 2. **Link Extraction**
   - **Forward Links Table**: Maps each page to its outbound links, showing where each page directs its readers.
   - **Backward Links Table**: Records all incoming links for each page, essential for calculating how influential each page is.

### 3. **PageRank Calculation**
   The core of the project involves setting up and iterating the PageRank algorithm:

   - **Initial Setup**:
     - **Damping Factor**: A value that ensures the algorithm accounts for the probability of a random jump to any page.
     - **Initial Rank Values**: All pages start with an equal rank.
     - **Maximum Iterations**: A predefined limit to control the number of recalculations.

   - **Iterative Process**:
     - Repeatedly calculate new ranks based on the ranks of linking pages until the values converge (stabilize) or reach the iteration limit.

### 4. **Output**
   - **Final Ranking**: The algorithm produces a ranked list of pages, reflecting their relative importance within the network based on link structure.

---

## 📈 Insights & Applications

The final output provides valuable insights into the web pages' relative importance, crucial for search engine optimization, web structure analysis, and various other applications in data science and web development.

---

By leveraging the power of **Apache Spark** in a **Databricks** environment, this project showcases how massive datasets can be efficiently processed and analyzed, demonstrating the practical utility of the PageRank algorithm in understanding web structures.

