#include <iostream>
using namespace std;
int main() {
  int i, n, flag = 0, key, ch, low, high, mid;
  cout << "enter no of elements: ";
  cin >> n;
  int a[n];
  cout << "Enter the array elements : ";
  for (i = 0; i < n; i++) {
    cin >> a[i];
  }
  cout << "1. Linear search \n2. Binary search" << endl;
  cin >> ch;
  switch (ch) {
  case 1:
    cout << "Enter the number you want to search: ";
    cin >> key;

    for (i = 0; i < n; i++) {
      if (key == a[i]) {
        cout << "\n" << key << " found at " << i << " position\n";
        flag = 1;
        break;
      }
    }
    if (flag == 0) {
      cout << "number not found";
    }
    break;
  case 2:
    cout << "Enter the number you want to search: ";
    cin >> key;
    low = 0, high = n - 1;
    while (low <= high) {
      mid = (low + high) / 2;
      if (key == a[mid]) {
        cout << key << " present at " << mid;
        break;
      } else if (key > a[mid]) {
        low = mid + 1;
      } else {
        high = mid - 1;
      }
    }
    if (low > high) {
      cout << "number not found";
    }
    break;
  default:
    cout << "Wrong choice";
  }
  return 0;
}
