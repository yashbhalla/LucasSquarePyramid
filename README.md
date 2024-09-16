# LucasSquarePyramid

## The following project has been developed by Shrey Gupta and Yash Bhalla for Project 1: Lucas Square Pyramid (COP5615).

### 1. Optimal Size of the Work Unit
Through experimentation, we determined that a work unit size of chunkSize based on the formula (n / workerCount).max(1) provides the best performance for our implementation. This size was chosen because it optimizes the balance between parallel processing and individual worker workload.

Here, the chunk size is computed by dividing the total range n by the number of workers. We ensure that the chunk size is at least 1 using .max(1) to handle cases where there are fewer numbers than workers.
Code: let chunkSize = (nBoss / workerCount.u64()).max(1)

The optimal chunk size can vary based on the problem size and the number of workers. For this implementation, ensuring that the work unit size is neither too small nor too large relative to the number of workers and problem size leads to effective parallel processing and efficient performance.

### 2. Result of running: lukas 1000000 4
<img width="1512" alt="image" src="https://github.com/user-attachments/assets/d4d7e1c9-ac07-43bb-a360-2e9bc7530c26">






