# Prefix Sum

Given an array **arr[] of size N**, find the prefix sum of the array. A prefix sum array is another array prefixSum[] of the same size, such that the value of **prefixSum[i] is arr[0] + arr[1] + arr[2] . . . arr[i].**
```cpp
void fillPrefixSum(int arr[], int n, int prefixSum[]){
    prefixSum[0] = arr[0];
    for (int i = 1; i < n; i++)
        prefixSum[i] = prefixSum[i - 1] + arr[i];
}
```
