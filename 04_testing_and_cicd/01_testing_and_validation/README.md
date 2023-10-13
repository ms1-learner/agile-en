# Challenge 1: Testing and Validation
​
## Description
Use your knowledge of testing to complete the requirements below.
- Only "Mt. Fuji" requirements need to be completed for this Challenge
- "Mt. Kilimanjaro" and "Mt. Everest" are optional for completion. They are intended to challenge you and help you grow your skills. In order to complete them, these optional difficulty levels may require you to do independent research for topics not covered in this course.
​
## Base Requirements
Write a function `my_assert` in C++, that accepts two arguments:
1. an expression `expr` that will evaluate to a bool value.
2. an optional message `msg` to be thrown in an exception if `expr` evaluates to `false`.
​
Then, using `my_assert`, complete the tests for the functions provided. Please start writing your code after the "/*----Your code here----*/" comment.
​
```cpp
#include <iostream>
#include <vector>
#include <string>
​
/*----These functions do not need to be changed----*/
​
std::vector<std::string> names {"Nick", "Lewis", "Nikos"};
​
bool contains(const std::string& name, const std::vector<std::string>& list_of_names) {
    return std::find(list_of_names.begin(), list_of_names.end(), name) != list_of_names.end();
}
​
std::string get_name(const std::string& name, const std::vector<std::string>& list_of_names) {
    if (contains(name, list_of_names)) {
        return name;
    } else {
        return "";
    }
}
​
void add_name(const std::string& name, std::vector<std::string>& list_of_names) {
    list_of_names.push_back(name);
}
​
int add_two(int num) {
    return num + 2;
}
​
double divide_by_two(double num) {
    return num / 2;
}
​
std::string greeting(const std::string& name, double num) {
    std::string message {"Hello, " + name + ". It is " + std::to_string(num) + " degrees warmer today than yesterday"};
    std::cout << message << std::endl;
    return message;
}
​
/*----Your code here----*/
/*----Difficulty: Mt. Fuji----*/
​
// define `my_assert` here, and use it for the subsequent tests
​
// make a test called `test_contains` for `contains` here
​
// make a test called `test_get_name` for `get_name` here
​
// make a test called `test_add_name` for `add_name` here
​
// make a test called `test_add_two` for `add_two` here
​
// make a test called `test_divide_by_two` for `divide_by_two` here
​
// make a test called `test_greeting` for `greeting` here
​
​
/*----Difficulty: Mt Kilimanjaro----*/
​
// make a test called `test_my_assert_false` for `my_assert` to check if it correctly returns the given optional `msg` when the expression evaluates to false
​
// make a test called `test_my_assert_true` for `my_assert` to check if it correctly handles an expression that evaluates to true
​
/*----Difficulty: Mt. Everest----*/
​
// make a test called `test_complex_greeting` for the entire following expression using `my_assert`. If the expression fails, make sure to give a descriptive message for `msg` that describes how the expression fails.
// greeting(get_name("Frosty the Snowman", {"Oatmeal", "Prancer", "Rudolph", "Andy"}), divide_by_two(add_two(2)));
​
```