## PROGRAM
```
age <- c(13, 15, 16, 16, 19, 20, 20, 21, 22,
         22, 25, 25, 25, 25, 30, 33, 33, 35,
         35, 35, 35, 36, 40, 45, 46, 52, 70)

cat("Mean =", mean(age), "\n")
cat("Median =", median(age), "\n")

freq <- table(age)
mode_values <- as.numeric(names(freq)[freq == max(freq)])
cat("Mode =", mode_values, "\n")

cat("Midrange =", (min(age) + max(age)) / 2, "\n")
cat("First quartile Q1 =", quantile(age, 0.25), "\n")
cat("Third quartile Q3 =", quantile(age, 0.75), "\n")
```
# OUTPUT
<img width="490" height="260" alt="image" src="https://github.com/user-attachments/assets/738028bb-da44-4d43-b620-e51b5a21a819" />
