#include <algorithm>
#include <iostream>
using namespace std;
void linearSearch(int arr[], int size, int key) {
  bool found = false;
  for (int i = 0; i < size; ++i) {
    if (arr[i] == key) {
      found = true;
      break;
    }
  }
  if (found) {
    cout << "Roll number " << key << " is found in the list (linear search).\n";
  } else {
    cout << "Roll number " << key
         << " is not found in the list (linear search).\n";
  }
}
void binarySearch(int arr[], int size, int key) {
  int left = 0;
  int right = size - 1;
  bool found = false;
  while (left <= right) {
    int mid = left + (right - left) / 2;

    if (arr[mid] == key) {
      found = true;
      break;
    } else if (arr[mid] < key) {
      left = mid + 1;
    } else {
      right = mid - 1;
    }
  }
  if (found) {
    cout << "Roll number " << key << " is found in the list (binary search).\n";
  } else {
    cout << "Roll number " << key
         << " is not found in the list (binary search).\n";
  }
}
int main() {
  int n;
  cout << "Enter the number of students who attended the training program: ";
  cin >> n;
  if (n <= 0) {
    cout << "Invalid number of students." << endl;
    return 1;
  }
  int a[n];
  cout << "Enter the roll numbers of the students:\n";
  for (int i = 0; i < n; ++i) {
    cin >> a[i];
  }
  sort(a, a + n);
  cout << "Sorted roll numbers:\n";
  for (int i = 0; i < n; ++i) {
    cout << a[i] << " ";
  }
  cout << endl;
  int key;
  int choice;
  cout << "Choose the type of search:\n";
  cout << "1. Linear Search\n";
  cout << "2. Binary Search\n";
  cout << "Enter your choice (1 or 2): ";
  cin >> choice;
  cout << "Enter a roll number to search: ";
  cin >> key;
  switch (choice) {
  case 1:
    linearSearch(a, n, key);
    break;
  case 2:
    binarySearch(a, n, key);
    break;
  default:
    cout << "Invalid choice. Please select 1 or 2.\n";
    break;
  }
  return 0;
}
