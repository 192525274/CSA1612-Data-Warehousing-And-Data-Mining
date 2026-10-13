## PROGRAM
```
lower <- c(1, 5, 15, 20, 50, 80)
upper <- c(5, 15, 20, 50, 80, 110)
freq <- c(200, 450, 300, 1500, 700, 44)

N <- sum(freq)
cf <- cumsum(freq)
i <- which(cf >= N / 2)[1]

L <- lower[i]
f <- freq[i]
cf_prev <- if (i == 1) 0 else cf[i - 1]
h <- upper[i] - lower[i]

median <- L + ((N / 2 - cf_prev) / f) * h

cat("Total frequency =", N, "\n")
cat("Approximate median =", median, "\n")
```
# OUTPUT
<img width="338" height="245" alt="image" src="https://github.com/user-attachments/assets/4f560527-6f8e-4da4-9c24-0d1441730cb0" />

