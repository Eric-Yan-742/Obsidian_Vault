When we have a new dp definition, the most structured and clearest way to initialize is to follow the smallest value of definition. As long as the values follow the definition, they are guaranteed to be correct. 

After we do initialization in the standard way, we may find a way to incorporate the initialization into our recurrece process. The first iteration of the recurrence loop could accomplish the job of initialization. To aid the recurrence process to initialize, we assign the dp array some dummy initial values that are not within the scope of the definition, which is confusing sometimes. Just remember these values are nothing special. They are just there to help the recurrence loop to accomplish initialization. 

Although this optimization of implicit definition makes our code cleaner, it reduces the redability of the code, making the reader wondering what those initial values mean and where exactly we initialize. Therefore, with a new dp definition, it's always suggested to do the structured way first. Then we can come up with some optimizations. However, if the problem uses a dp definition you are already familiar with, like the knapsack problems, it's faster to use the implicit initialization trick. 

General Steps of Initialization for a new dp definition
1. Come up with an explicit initialization with the smallest value **within** the scope of definition. No index out of bound.
2. Then we can try to integrate some parts of the initialization into the recurrence loop. We can insert some dummy initial values to help us. Those values are either completely meaningless or ambiguously defined. The first round of the loop will use the dummy values to get the correct smallest value within the definition. 

Below are some dp templates where we use implicit initialization. Explicit initialization is written out first to help illustrate the implicit initialization

# Knapsack Problem

Only considering the first item is strictly within our definition and must be a valid initialization. A trick of initialization for knapsack problem is that you can think of the base case as not considering any element or an empty set `{}`. This is ambiguously within the definition, but does produce the right result for all our definitions. Now all the implicit definition makes more sense. 

## 0-1 Knapsack problem

### Max value

[[0-1 Knapsack Problem]]

[[416. Partition Equal Subset Sum]]

[[1049. Last Stone Weight II]]

### Number of combinations

[[494. Target Sum]]

## Complete Knapsack problem

Initialization is basically the same as 0-1 knapsack. However, it becomes more complicated. Elements later in the dp array depend on the elements before. Thus, we cannot simply assign some elments in the first row with some values. We have to use the recurrence relation (or at least a simplified version) during the explicit initialization. Similarly, we can use the empty bag trick that avoids the overhead of empty bag. 
### Max value

[[Complete Knapsack Problem]]

### Number of combinations

[[518. Coin Change II]]

### Number of permutations

Use a different definition of climbing stairs. 

[[377. Combination Sum IV]]

### Number of items

Sometimes by the definition, there just shouldn't be anything in that cell of the array. 

[[322. Coin Change]]

[[279. Perfect Squares]]

# Common Subarray/Subsequence Problem

Explicit initialization start from the first element of both arrays `nums1[0]` and `nums2[0]`. However, we can consider empty string just like how we do in [[#Knapsack Problem]]. It works for all common subarray/subsequence problems as well. 

## Subarray length

[[718. Maximum Length of Repeated Subarray]]

## Subsequence length

[[1143. Longest Common Subsequence]]

[[1035. Uncrossed Lines]]

## Mix

### Length

[[392. Is Subsequence]]

### Number that matches

[[115. Distinct Subsequences]]

## Min number of operations

[[583. Delete Operation for Two Strings]]

[[72. Edit Distance]]

# Palindromic

## Number

[[647. Palindromic Substrings]]

## Length

[[516. Longest Palindromic Subsequence]]