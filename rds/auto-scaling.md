# Auto Scaling in RDS

- Auto Scaling in RDS helps you increase the storage on your RDS DB instance dynamically. When RDS detects that you are running out of free database storage, it scales automatically, helping you avoid the need to manually scale your database storage.

- You need to set a Maximum Storage Threshold, which is the maximum limit for DB storage.

- RDS will automatically modify storage if the following conditions are met:
    - Free storage is less than 10% of the allocated storage.
    - The low-storage condition lasts for at least 5 minutes.
    - At least 6 hours have passed since the last storage modification.

- This feature is particularly useful for applications with unpredictable workloads.