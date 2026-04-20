# Python Algorithm Classification Dataset (PACD)

The Python Algorithm Classification Dataset (PACD) is a collection of algorithm implementations sourced from publicly available GitHub Gists. Each algorithm is human reviewed and categorized by type (i.e "bubble sort", "sieve of Eratosthenes" etc), and the dataset covers 3 unique problems (sorting, primality testing, search). The dataset is designed for benchmarking code classification, code quality analysis, and machine learning models focused on algorithm identification. The compilation of this dataset focused on several key methodologies:

(1) All algorithms are either completly isolated functions or utilize Python's built-in libraries such as math or random

(2) All algorithms return an object instead of doing in-place manipulation

(3) All comments and docstrings from the original implementation are preserved

(4) No duplicate algorithm implementations

(5) Careful manual review of each algorithm's classification label and correctness

(6) A "natural" variety of implementation details, including comments in multiple languages and a variety of whitespace and stylistic choices.

*NOTE: Algorithm implementations were sometimes repaired to fix the following issues:

(1) In-place algorithms were converted to return objects

(2) Usage of non built-in libraries was replaced with pure python


## Dataset Structure

The dataset is provided in CSV format and contains the following columns:

| Column | Description |
| :--- | :--- |
| **Location** | The source URL of the GitHub Gist. |
| **Source** | The raw Python source code for the algorithm. |
| **Problem** | A numerical ID representing the general class of the algorithm. |
| **Type** | A numerical ID representing the specific implementation or variant within a problem class. |
| **Entrypoint** | The name of the primary function or method intended for execution. |
| **Validated** | A flag (1.0) indicating that the code has been verified for basic correctness. |

---

## Numerical Indicators

The dataset uses numerical IDs to categorize algorithms. Below are the mappings for the `Problem` and `Type` columns.

### Problem 1: Sorting
| Type ID | Algorithm Variant |
| :--- | :--- |
| 1 | Bubble Sort |
| 2 | Merge Sort |
| 3 | Heap Sort |
| 4 | Quick Sort |

### Problem 2: Primality Testing
| Type ID | Algorithm Variant |
| :--- | :--- |
| 1 | Basic Trial Division |
| 2 | Miller-Rabin Primality Test |
| 3 | Sieve of Eratosthenes |

### Problem 3: Searching
| Type ID | Algorithm Variant |
| :--- | :--- |
| 1 | Binary Search |
| 2 | Sequential (Linear) Search |
| 3 | Jump Search |

---

## Usage

This dataset is suitable for tasks including:
- **Algorithm Classification:** Predicting the `Problem` or `Type` based on the `Source` code.
- **Code Summarization:** Generating function names or docstrings from implementations.
- **Clone Detection:** Identifying similar algorithmic logic across different coding styles.

## Statistics
Total instances: N = 329
| Problem Category  | Algorithm      | Problem Label | Type Label | Count |
|-------------------|----------------|---------------|------------|-------|
| Sorting           | Bubble Sort    | 1             | 1          | 39    |
| Sorting           | Selection Sort | 1             | 2          | 37    |
| Sorting           | Merge Sort     | 1             | 3          | 38    |
| Sorting           | Quick Sort     | 1             | 4          | 42    |
| Primality Testing | Naive / Sieve  | 2             | 1          | 35    |
| Primality Testing | Miller-Rabin   | 2             | 2          | 30    |
| Primality Testing | Other          | 2             | 3          | 28    |
| Searching         | Binary Search  | 3             | 1          | 40    |
| Searching         | Linear Search  | 3             | 2          | 35    |
| Searching         | Jump Search    | 3             | 3          | 5     |


## Citation
```
@misc{sohail2025measurealgorithmsimilarity,
      title={Towards a Measure of Algorithm Similarity},
      author={Shairoz Sohail and Taher Ali},
      year={2025},
      eprint={2510.27063},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2510.27063},
}
```
