# Big O

## What is Big O notation
Big O notation typically refers to a notation that represents how quickly an algorithm scales with the increase of the number of elements it operates on.

#### Algorithm A
```c++
int[] nums = new int[n];
for(int i = 0; i < n; i++){
	nums[i] += 1;
}
```
Would have a big O notation of $O(n)$ since it scales linearly with the amount of elements.

#### Algorithm B
```c++
int[] nums = new int[n];
for(int i = 0; i < n; i++){
	for(int j = 0; j < n; j++){
		nums[j] += 1;
	}
}
```
Would have a big O notation of $O(n^2)$. Since algorithm B essentially repeats algorithm A n times it has a quadratic growth curve. 

Big O notation is not exact. It measures the worst term of the growth curve and discards all numeric multipliers.

The following are some examples of algorithms who's growth curves are different from their big O notations.
#### Algorithm C
```c++
int[] nums = new int[n];
for(int i = 0; i < n; i++){
	for(int j = 0; j < n; j++){
		nums[j] += 1;
	}
}
for(int i = 0; i < n; i++){
	nums[j] += 1;
}
```

In this case the exact curve can be described as $n^2 + n$ but the big O notation would still be $O(n^2)$ because their worst term is quadratic and all other terms can be discarded.

#### Algorithm D
```c++
int[] nums = new int[n];
for(int i = 0; i < n; i++){
	nums[i] += 1;
}
for(int i = 0; i < n; i++){
	nums[i] += 1;
}
```
#### Algorithm E
```c++
int[] nums = new int[n];
for(int i = 0; i < n; i++){
	nums[i] += 1;
	nums[i] += 1;
	nums[i] += 1;
}
```

In the case of the algorithm D and E the growth curves are $2n$ and $3n$ respectively but the numeric term is discarded so we're left with $O(n)$ for both.

> [!attention] 
> Any multiplicative constants should be discarded when writing Big O notation. The catch is this also incudes things like bases of logarithms.
> 
> So for instance the big O of $log_2 n$ and $log_e n$ is $O(\log{n})$ because they differ by a constant factor $\frac{1}{log \space 2}$ which is discarded. 



> [!tldr] TLDR
> Big O notation studies how algorithms grow when the amount of elements they operate on (n) grows. 
> 
> Typical Big O examples include:
> - $O(1)$ - constant 
> - $O(n)$ - *linear*
> - $O(n^2)$ - *quadratic*
> - $O(\log{n})$ - *logarithmic*
>
> Big O is simplified so constant factors are discarded and only the biggest term is considered

## Worst case and best case for Big O
Worst and best case scenarios refer to changes in the algorithm growth curve depending on how the algorithm end up being run.

With the algorithms we've seen so far the algorithm can only be run one way. It doesn't depend on the parameters given or on the values of the elements given.

Some algorithms however will depend on external parameters and thus must be analyzed with worst and best case scenarios.

> [!warning] 
> Worst and best case scenarios don't refer to changing the amount of elements the algorithm runs on (**n**). **n** always remains as an unknown term and Big O is always expressed as a function of n. 
> 
> Instead what changes between the worst and best case scenarios are things like values of external parameters that influence the way the algorithm runs.

An example of an algorithm that would have different best and worst case scenarios could be:
```c++
int[] nums = new int[n];
for(int i = 0; i < n; i++){
	if(nums[i] % 2 == 0){// if number even
		//add 1 to all
		for(int j = 0; j < n; j++){
			nums[j] += 1;
		}
	}
}
```

This algorithm runs through all the numbers given and adds 1 to all for each even number found.

The best and worst case scenarios would differ since if all the numbers given are odd the algorithm would only run through the elements **once**. However if all the numbers are even the algorithm would run through all elements **for every number given**. 

**Thus the big O notation in the best case scenario would be $O(n)$ and in the worst case scenario $O(n^2)$
## Sorting algorithms
Sorting Algorithms have been proven to be of $O(n\log{n})$ in the **worst case scenario**. It is mathematically impossible for a sorting algorithm to sort an array faster than $O(n\log{n})$ as a worst case.

>[!note] 
>When talking about sorting algorithms we generally consider the worst or average case scenarios. That's because that for almost any sorting algorithm the best case scenario is that the array is already sorted which brings the time complexity down to $O(n)$. 

This divides sorting algorithms in 2 types:
#### "Fast" sorting algorithms
Fast sorting algorithms are those that have their **worst case** time complexity as $O(n\log{n})$. The most famous examples include:
- Merge sort
- Quick sort
#### "Slow" sorting algorithms
Fast sorting algorithms are those that have their **worst case** time complexity as $O(n^2)$. These algorithms typically have a "sorted" area in the array and function by expanding that sorted are 1 cell at a time (usually by running through all the other unsorted cells and doing something). 

Common examples include:
- Bubble sort
- Selection sort
- Insertion sort

>[!attention] 
>This distinction is rather broad than strict and isn't used "officially". The algorithms from these groups can differ amongst each other in average time complexities or outperform others under specific circumstances.

>[!info] Sorting algorithm animations
>### Bubble sort
>![[Bubble-sort.gif|300]]
>### Merge sort
>![[Merge-Sort.gif|300]]