## Fast C++ Tutorial

## First of all
```c++
int n = 5;
printf("%d\n", n) = cout << n << endl;
scanf("%d", &n) = cin >> n;
```
---------
## Default template:

```c++
#include <bits/stdc++.h> // includes the "bits" library, which is a compilation of many C++ libraries;
using namespace std; // saves from having to write "std::" before each standard library function
  
int main() {
  ios::sync_with_stdio(0);
  cin.tie(0);
  // speeds up the code for large inputs

  return 0;
}
```
---------
## The string type:
In C++, we have the string type to represent sequences of characters. It provides a convenient way to work with text data.
- You can declare a string variable like this:

```c++
string str = "Hello, world!";
string name;
cin >> name;
```

- You can perform various operations on strings, such as concatenation:

```c++
string str1 = "Hello, ";
string str2 = "world!";
string result = str1 + str2; // result contains "Hello, world!"
```
- You can access individual characters in a string using array notation:

```c++
string str = "Hello";
char firstChar = str[0]; // 'H'
char thirdChar = str[2]; // 'l'
```
- You can also find the length of a string using the size() or length() functions:
```c++
string str = "Hello";
int len = str.size(); // len will be 5
```

- Strings support many useful functions for manipulation and searching, such as find(), substr(), replace(), and more. Here's an example of using find():

```c++
string str = "Hello, world!";
size_t found = str.find("world");
if (found != string::npos) {
    cout << "Substring found at position " << found << endl;
} else {
    cout << "Substring not found" << endl;
}
```
- You can also compare strings using comparison operators such as ==, >, and <. Here are some examples:
```c++
string str1 = "apple";
string str2 = "banana";

if (str1 == str2) {
    cout << "str1 is equal to str2" << endl;
} else if (str1 > str2) {
    cout << "str1 is greater than str2" << endl;
} else {
    cout << "str1 is less than str2" << endl;
}
```
---------
## max() and min() functions:
The max() and min() functions in C++ are used to return the maximum and minimum of two or more values, respectively.

The basic syntax of these functions is as follows:

```bash
max(a, b): Returns the greater value between a and b.
min(a, b): Returns the lesser value between a and b.
```

```c++
int a = 5;
int b = 8;

// Finding the maximum between two variables
int max_value = max(a, b);
cout << "The maximum between " << a << " and " << b << " is: " << max_value << endl;

// Finding the minimum between two variables
int min_value = min(a, b);
cout << "The minimum between " << a << " and " << b << " is: " << min_value << endl;
```

```c++
int a = 5;
int b = 8;
int c = 3;

// Finding the maximum among three variables
int max_value = max({a, b, c});
cout << "The maximum among {" << a << ", " << b << ", " << c << "} is: " << max_value << endl;

// Finding the minimum among three variables
int min_value = min({a, b, c});
cout << "The minimum among {" << a << ", " << b << ", " << c << "} is: " << min_value << endl;
```
---------
## Common data structures:
### vector<>
it's a vector, can hold any type within the <>, example of usage

- Without dynamic allocation
```c++
int n;
cin >> n;
vector<int> a(n); // the size inside () is allocated
for (int i = 0; i < n; i++) cin >> a[i];
```
- With dynamic allocation
```c++
int n;
cin >> n;
vector<int> a;
for (int i = 0; i < n; i++) {
  int e; cin >> e;
  a.push_back(e);
}
```

### sort() function
```c++
sort(a.begin(), a.end()); // it's a good sort
```
### map<>
it's a key-value pair container, example of usage

```c++
map<int, string> mp;
mp[1] = "one";
mp[2] = "two";
cout << mp[1] << endl; // outputs "one"
```
### set<>
it's a container that stores unique elements, example of usage

```c++
set<int> s;
s.insert(1);
s.insert(2);
s.insert(1); // will not be inserted again
cout << s.size() << endl; // outputs 2
```
### queue<>
it's a first-in-first-out (FIFO) container, example of usage
```c++
queue<int> q;
q.push(1);
q.push(2);
cout << q.front() << endl; // outputs 1
q.pop();
cout << q.front() << endl; // outputs 2
```
For more information, take a look at https://cplusplus.com/
