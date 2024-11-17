#include <iostream>
#include <string>
using namespace std;
bool isPalindrome(string str) {
  char stack[100];
  int top = -1;
  for (int i = 0; i < str.length(); i++) {
    if (top == 99) {
      cout << "Stack Overflow!" << endl;
      return false;
    }
    stack[++top] = str[i];
  }
  for (int i = 0; i < str.length(); i++) {
    if (stack[top--] != str[i]) {
      return false;
    }
  }
  return true;
}
int main() {
  string str;
  cout << "Enter a string: ";
  cin >> str;
  if (isPalindrome(str)) {
    cout << str << " is a palindrome." << endl;
  } else {
    cout << str << " is not a palindrome." << endl;
  }
  return 0;
}
