# Prefix Sum

Given an array **arr[] of size N**, find the prefix sum of the array. A prefix sum array is another array prefixSum[] of the same size, such that the value of **prefixSum[i] is arr[0] + arr[1] + arr[2] . . . arr[i].**
```cpp
void fillPrefixSum(int arr[], int n, int prefixSum[]){
    prefixSum[0] = arr[0];
    for (int i = 1; i < n; i++)
        prefixSum[i] = prefixSum[i - 1] + arr[i];
}
```

# Check Vowels - A Better Way
```cpp
// General Style
bool isVowel(char ch){
    return (ch=='a' || ch=='e' || ch=='i' || ch=='o'|| ch=='u');
}
// Better Approach - Easy but we don't use it often
unordered_set<char> vowels{'a', 'e', 'i', 'o', 'u'};
if(vowels.count(ch)) 
 