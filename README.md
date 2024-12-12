# Sorting Algorithms and Big O Notation

## Four Different Sorting Algorithms

### 1. Bubble Sort
- **Description**: Repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.
- **Big O Notation**:
  - Best Case: `O(n)` (already sorted list).
  - Average Case: `O(n^2)`.
  - Worst Case: `O(n^2)`.
- **Key Properties**: Simple but inefficient for large inputs.

### 2. Quick Sort
- **Description**: Selects a pivot, partitions the array into elements less than and greater than the pivot, and recursively sorts the partitions.
- **Big O Notation**:
  - Best and Average Case: `O(n log n)`.
  - Worst Case: `O(n^2)` (occurs when pivot selection is poor, e.g., always selecting the smallest or largest element).
- **Key Properties**: In-place but not stable. Fast for large datasets with a good pivot strategy.

### 3. Merge Sort
- **Description**: Divides the array into halves, recursively sorts them, and merges the sorted halves.
- **Big O Notation**:
  - Best, Average, and Worst Case: `O(n log n)`.
- **Key Properties**: Stable but not in-place (requires additional space).

### 4. Selection Sort
- **Description**: Finds the smallest element in the array, swaps it with the first element, and repeats for the rest of the array.
- **Big O Notation**:
  - Best, Average, and Worst Case: `O(n^2)`.
- **Key Properties**: In-place but not stable.

---

## Big O Notation and Evaluating Time Complexity

### What is Big O Notation?
Big O Notation describes how the runtime of an algorithm grows as the input size increases. It focuses on the **dominant term**, ignoring constants and lower-order terms.

### Steps to Evaluate Time Complexity
1. **Identify Loops**:
   - Single loops over `n`: `O(n)`.
   - Nested loops: Multiply their iterations, e.g., two nested loops: `O(n^2)`.
2. **Recursive Calls**:
   - Use the recurrence relation (e.g., `T(n) = 2T(n/2) + O(n)`) and solve it.
3. **Operation Counts**: Count dominant operations and relate them to input size.
4. **Special Structures**: Consider divide-and-conquer or other strategies.

---

## Selecting the Best Sorting Algorithm

### Factors to Consider
1. **Input Size**:
   - Small datasets: Insertion Sort or Bubble Sort may suffice.
   - Large datasets: Merge Sort or Quick Sort is preferable.
2. **Data Characteristics**:
   - Nearly sorted data: Insertion Sort is efficient (`O(n)`).
   - Data with many duplicates: Algorithms like Counting Sort or Bucket Sort may excel.
3. **Memory Constraints**:
   - Low memory: In-place algorithms like Quick Sort or Heap Sort.
   - High memory: Merge Sort (requires additional space).
4. **Stability Requirement**:
   - Stable sorting needed: Use Merge Sort or Bubble Sort.

---

## Stable Sorting Algorithm

### What is Stability?
A **stable sorting algorithm** preserves the relative order of records with equal keys. For example, if two elements have the same value, they remain in the same order as in the original input.

### Examples of Stable Sorting Algorithms
- Merge Sort.
- Bubble Sort.
- Insertion Sort.

### Examples of Unstable Sorting Algorithms
- Quick Sort.
- Heap Sort.
- Selection Sort.

### When Does Stability Matter?
Stability is important when sorting multi-field data and secondary sorting depends on previous ordering. For example, sorting by name after sorting by age while keeping people with the same age in the same relative order as before.

---

## Summary Table

| Algorithm        | Best Case    | Average Case | Worst Case   | Stable | In-place |
|-------------------|--------------|--------------|--------------|--------|----------|
| Bubble Sort       | `O(n)`       | `O(n^2)`     | `O(n^2)`     | Yes    | Yes      |
| Quick Sort        | `O(n log n)` | `O(n log n)` | `O(n^2)`     | No     | Yes      |
| Merge Sort        | `O(n log n)` | `O(n log n)` | `O(n log n)` | Yes    | No       |
| Selection Sort    | `O(n^2)`     | `O(n^2)`     | `O(n^2)`     | No     | Yes      |

---

For more examples or explanations, feel free to ask!