## PROGRAM
```
data <- c(200, 300, 400, 600, 1000)

# Min-max normalization to [0, 1]
min_max <- (data - min(data)) / (max(data) - min(data))
cat("Min-max normalization:\n")
print(min_max)

# Z-score normalization
z_score <- (data - mean(data)) / sd(data)
cat("Z-score normalization:\n")
print(z_score)
```
# OUTPUT
<img width="444" height="197" alt="image" src="https://github.com/user-attachments/assets/9f43883e-d242-4300-b57d-1e48a4714890" />


