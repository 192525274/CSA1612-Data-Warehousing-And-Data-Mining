## PROGRAM
```
x <- sort(c(55,60,71,63,55,65,50,55,58,59,61,63,65,67,71,72,75))

# Equal frequency
print(split(x, cut(seq_along(x),3,labels=FALSE)))

# Equal width
print(split(x, cut(x,3,include.lowest=TRUE)))

hist(x, breaks=3, main="Marks Histogram")
```
# OUTPUT
<img width="948" height="377" alt="image" src="https://github.com/user-attachments/assets/df202852-0feb-4394-9773-204aa7d4fb30" />

