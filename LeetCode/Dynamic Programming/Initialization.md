When we have a new dp definition, the most structured and clearest way to initialize is to follow the smallest value of definition. As long as the values follow the definition, they are guaranteed to be correct. 

After we do initialization in the standard way, we may find a way to incorporate the initialization into our recurrece process. The first iteration of the recurrence loop could accomplish the job of initialization. To aid the recurrence process to initialize, we assign the dp array some initial values that are not within the scope of the definition, which is confusing sometimes. Just remember these values are nothing special. They are just there to help the recurrence loop to accomplish initialization. 

Although this optimization of implicit definition makes our code more concise, it reduces the redability of the code, making the reader wondering what those initial values mean and where exactly we initialize. Therefore, with a new dp definition, it's always suggested to do the structured way first. Then we can come up with some optimizations. However, if the problem uses a dp definition you are already familiar with, like the knapsack problems, it's faster to use the implicit initialization trick. 

Below are some dp templates where we use implicit initialization. Explicit initialization is written out first to help illustrate the implicit initialization

# 0-1 Knapsack problem

## Max value

[[0-1 Knapsack Problem]]

[[416. Partition Equal Subset Sum]]

[[1049. Last Stone Weight II]]

## Number of items