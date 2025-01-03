# Vector
### Sum of all elements of a vector
**std::accumulate()**\
The std::accumulate() function is used to find the sum (or any other binary operation) of all the values lying in a range.

**Syntax**\
std::accumulate(first, last, init, op);

**Parameters**\
**first:** Iterator to the first element of the range.\
**last:** Iterator to the element one after the last element of the range.\
**init:** Initial value to start the accumulation with.\
***op:** An optional function pointer that provides the binary operation to perform. By default, addition is used to get the sum.*

**Return Value**\
Returns the accumulated value after performing the operation on each element.

**Note:**\
***For adding larger values beyond the int range, the sum should be initialized with 0ll or any other value with the suffix ll, else the sum will be overflown. (here ll refers to long long int)***

#### Multiplication and Addition using Accumulate
```cpp
// Custom function to multiply adjacent numbers
int op(int a, int b) {
    return a * b;
}

int main() {
    vector<int> vec = {5, 10, 15};  
    auto first = vec.begin();
    auto last = vec.end();
  
    // Using accumulate function with user-defined operation
    int product = accumulate(first, last, 1, op);
    cout << product << endl;


    // Use accumulate to find the sum of elements in the vector
    int sum = accumulate(first, last, 0);  
    cout << sum << endl;
      
    return 0;
}
```