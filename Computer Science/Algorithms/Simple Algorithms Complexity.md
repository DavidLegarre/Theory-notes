# Simple Algorithms Complexity

## Simple loop

The following function finds the maximal element in an array

```c
int find_max(const in *array, size_t len) {
	int max = INT_MIN;
	for (size_t i = 0; i < len; i++) {
		if (max < array[i]) {
			max = array[i];
		}
	}
}
```

The input size is the size of the array, which I called `len` in the code.

Let's count the operations.

```c
int max = INT_MIN;
size_t i = 0;
```

These two assignments are done only once, so that's 2 operations.  The operations that are looped are:

```c
if (max < array[i])
i++;
max = array[i]
```

Since there are 3 operations in the loop, and the loop is done $n$ times, we add $3n$ to our already existing 2 operations to get $3n+2$. So our functions takes $3n+2$ operations to find the max (its complexity is $3n+2$). This is a polynomial where the fastest growing term is a factor of $n$, so it is $O(n)$. 

## A nested loop

```c
contains_duplicates(const int *array, size_t len) {
	for (int i = 0; i < len -1; i++) {
		for (int j = 0; j < len; j++) {
			if (i != j && array[i] == array[j]) {
				return 1;
			}
		}
	}
}
```

