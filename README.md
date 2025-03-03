# Polynomial Multiplication Analysis

## Overview
This project analyzes the performance of three polynomial multiplication algorithms:
1. **Naive Multiplication** - A straightforward O(n^2) approach using nested loops.
2. **Karatsuba Multiplication** - A divide-and-conquer algorithm with a complexity of O(n^log2(3)).
3. **Fast Fourier Transform (FFT) Multiplication** - Uses FFT and Inverse FFT to achieve O(n log n) complexity.

The goal of this analysis is to compare the execution times of these algorithms across various polynomial sizes.

## Implementation Details
### FFT Multiplication
- Implements the Cooley-Tukey FFT algorithm for converting between coefficient and value representations.
- Performs polynomial multiplication in the value domain and converts back using inverse FFT.

### Karatsuba Multiplication
- Implements the Karatsuba algorithm by recursively breaking down the multiplication into three smaller multiplications.
- Optimized by padding polynomials to the nearest power of 2.

### Naive Multiplication
- Implements basic polynomial multiplication using two nested loops.

## Performance Analysis
The provided script runs experiments on polynomials of increasing size and measures the average execution time of each algorithm. The results are visualized using two plots:
1. **Log Scale Plot** - Shows the execution time on a logarithmic scale for better visibility of differences in growth rates.
2. **Linear Scale Plot** - Provides a direct comparison of execution times for large polynomial sizes.

The generated graph demonstrates that:
- Naive multiplication scales poorly for large polynomials.
- Karatsuba provides a speedup over naive multiplication but is outperformed by FFT for large sizes.
- FFT is the most efficient for large polynomials due to its O(n log n) complexity.

## Dependencies
- Python 3
- Matplotlib (for visualization)
- NumPy (for numerical operations)
- tqdm (for progress tracking)

## Running the Analysis
To execute the script, run the provided Jupyter notebook.

After execution, a graph comparing the three multiplication methods will be generated, showcasing their runtime differences.

## Conclusion
This analysis confirms that FFT-based multiplication is the most efficient for large polynomials, while Karatsuba serves as a practical middle-ground between naive and FFT approaches. The insights gained from this comparison are valuable for applications requiring efficient polynomial multiplication, such as cryptography, signal processing, and numerical methods.
![image](https://github.com/user-attachments/assets/1f68f38e-3664-4d52-999b-edfebe8a778d)
