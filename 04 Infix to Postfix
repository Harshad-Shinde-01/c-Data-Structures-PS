#include <iostream>
using namespace std;
int top = -1;
char stack[20], c;
void push(char x) {
  top += 1;
  stack[top] = x;
}
char pop() {
  char data = stack[top];
  top -= 1;
  return data;
}
int fun_pre(char c) {
  if (c == '+' || c == '-') {
    return 1;
  } else if (c == '*' || c == '/') {
    return 2;
  } else if (c == '^') {
    return 3;
  } else {
    return -1;
  }
}
int main() {
  char a[20], x;
  int n, i;
  cout << "enter the number of characters in infix expression: ";
  cin >> n;
  cout << "enter the infix expression: ";
  for (i = 0; i < n; i++) {
    cin >> a[i];
  }
  cout << "The postfix expression is:";
  for (i = 0; i < n; i++) {
    c = a[i];
    if (fun_pre(c) > 0) {
      while (top != -1 && fun_pre(stack[top]) >= fun_pre(c)) {
        cout << pop();
      }
      push(c);
    } else if (c == ')') {
      x = pop();
      while (x != '(') {
        cout << x;
        x = pop();
      }
    } else if (c == '(') {
      push(c);
    } else {
      cout << c;
    }
  }
  while (top != -1) {
    cout << pop();
  }
  return 0;
}
