## PROGRAM
```
data <- c(11, 13, 13, 15, 15, 16, 19, 20,
          20, 20, 21, 21, 22, 23, 24, 30,
          40, 45, 45, 45, 71, 72, 73, 75)

# Divide into 3 equal-frequency bins
bins <- split(data, rep(1:3, each = 8))

cat("Original bins:\n")
print(bins)

# Smoothing by bin mean
bin_mean <- lapply(bins, function(x) rep(mean(x), length(x)))
cat("Smoothing by bin mean:\n")
print(bin_mean)

# Smoothing by bin median
bin_median <- lapply(bins, function(x) rep(median(x), length(x)))
cat("Smoothing by bin median:\n")
print(bin_median)

# Smoothing by bin boundaries
bin_boundaries <- lapply(bins, function(x) {
  low <- min(x)
  high <- max(x)
  sapply(x, function(v) {
    if (abs(v - low) <= abs(v - high)) low else high
  })
})
```
# OUTPUT
<img width="472" height="368" alt="image" src="https://github.com/user-attachments/assets/48e3ec32-23ad-4917-a0fc-ccfa470391e8" />
<img width="470" height="344" alt="image" src="https://github.com/user-attachments/assets/91f75e1b-b03c-4ade-a82f-2e94bceb2003" />
<img width="401" height="160" alt="image" src="https://github.com/user-attachments/assets/efc24c42-97da-42a2-8af1-4c1146ec2b6d" />



cat("Smoothing by bin boundaries:\n")
print(bin_boundaries)
