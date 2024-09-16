# Lucas Square Pyramid

## The following project has been developed by Shrey Gupta and Yash Bhalla for Project 1: Lucas Square Pyramid (COP5615).

### 1. Optimal Size of the Work Unit
Through experimentation, we determined that a work unit size of chunkSize based on the formula (n / workerCount).max(1) provides the best performance for our implementation. This size was chosen because it optimizes the balance between parallel processing and individual worker workload.

Here, the chunk size is computed by dividing the total range n by the number of workers. We ensure that the chunk size is at least 1 using .max(1) to handle cases where there are fewer numbers than workers.
Code: let chunkSize = (nBoss / workerCount.u64()).max(1)

The optimal chunk size can vary based on the problem size and the number of workers. For this implementation, ensuring that the work unit size is neither too small nor too large relative to the number of workers and problem size leads to effective parallel processing and efficient performance.

### 2. Result of running: lukas 1000000 4

Below is the result of running Lucas with N = 1000000 and k = 4:

<img width="645" alt="Result of running ./LucasSquarePyramid 1000000 4" src="https://github.com/user-attachments/assets/9d62e6a9-ff91-4f13-bee5-915702e6ed37">

### 3. CPU Ratio of running: lukas 1000000 4

Below is the result of running Lucas with N = 1000000 and k = 4:

<img width="721" alt="Result of running  time ./LucasSquarePyramid 1000000 4" src="https://github.com/user-attachments/assets/d1d3af1f-b3fd-4734-8982-db6e75b096fe">

To calculate the CPU ratio,
  CPU Ratio = (User Time + System Time) / (Total Time)

  Here, User Time = 0.03 s
        System Time = 0.00 s
        Total Time = 0.01 s
  Hence, CPU Ratio = (0.03 + 0.00) / 0.01 = 3
This indicates that the CPU time used is three times the real time, which suggests that the program is utilizing more than one core effectively.

NOTE: We can also see in the image provided above that CPU usage is given as 301%, indicating CPU usage being three times the real time.

### 4. Largest Problem Solved on a Single Machine:  lukas 1000000000 30

Below is the result of running Lucas with N = 1000000000 and k = 30:

<img width="710" alt="image" src="https://github.com/user-attachments/assets/8ccd8c16-9365-43c7-963f-d09f741056a1">

Here, the CPU usage is given as 396%, indicating CPU usage being approximately four times the real time and utilizing more than one core effectively.














