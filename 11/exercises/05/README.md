### Exercise 11.05
Write the following function

```c
void split_time(int t , int *h , int *m , int *s);
```

`total_sec` is a time represented as the number of seconds since midnight. `hr`,
`min` and `sec` are pointers to variables in which the function will store the
equivalent time in hours (0-23), minutes (0-59) and seconds (0-59),
respectively.

### Solution

```c
void split_time(int t , int *h , int *m , int *s) {
    *h = t / 3600 <= 23 ? t / 3600 : 23;
    t -= *h * 3600;
    *m = t / 60 <= 60 ? t / 60 : 60;
    t -= *m * 60;
    *s = t;}
```
