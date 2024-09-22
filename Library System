#include <iostream>
using namespace std;

class Library {
private:
  int cost[50], n = 0;
  string name[50], edition[50];

public:
  void entry() {
    int m;
    cout << "Enter the number of books you want to insert: ";
    cin >> m;
    for (int i = n; i < n + m; i++) {
      cout << "Enter book name: ";
      cin >> name[i];
      cout << "Enter book edition: ";
      cin >> edition[i];
      cout << "Enter book cost: ";
      cin >> cost[i];
    }
    n += m;
  }

  void display() {
    for (int i = 0; i < n; i++) {
      cout << "Book name: " << name[i] << " \tBook edition: " << edition[i]
           << "\tBook cost: " << cost[i] << "\n";
    }
  }

  void sortDescending() {
    for (int i = 0; i < n - 1; i++) {
      for (int j = 0; j < n - i - 1; j++) {
        if (cost[j] < cost[j + 1]) { 
          swap(cost[j], cost[j + 1]);
          swap(name[j], name[j + 1]);
          swap(edition[j], edition[j + 1]);
        }
      }
    }
  }

  void copyCostsLessThan500() {
    int lessCost[50];
    string lessName[50];
    string lessEdition[50];
    int less = 0;

    for (int i = 0; i < n; i++) {
      if (cost[i] <= 500) { 
        lessCost[less] = cost[i];
        lessName[less] = name[i];
        lessEdition[less] = edition[i];
        less++;
      }
    }

    cout << "Books with cost less than 500:\n";
    for (int i = 0; i < less; i++) {
      cout << lessName[i] << "\t" << lessEdition[i] << "\t" << lessCost[i] << endl;
    }
  }

  void Duplicate_Temp() {
    int tempCost[50];
    string tempName[50];
    string tempEdition[50];
    int tempN = 0;

    for (int i = 0; i < n; i++) {
      bool isDuplicate = false;
      for (int j = 0; j < tempN; j++) {
        if (name[i] == tempName[j] && edition[i] == tempEdition[j] && cost[i] == tempCost[j]) {
          isDuplicate = true;
          break;
        }
      }
      if (!isDuplicate) {
        tempCost[tempN] = cost[i];
        tempName[tempN] = name[i];
        tempEdition[tempN] = edition[i];
        tempN++;
      }
    }

    n = tempN;
    for (int i = 0; i < n; i++) {
      cost[i] = tempCost[i];
      name[i] = tempName[i];
      edition[i] = tempEdition[i];
    }
  }

  void Duplicate_WithoutTemp() {
    for (int i = 0; i < n; i++) {
      for (int j = i + 1; j < n; j++) {
        if (name[i] == name[j] && edition[i] == edition[j] && cost[i] == cost[j]) {
          for (int k = j; k < n - 1; k++) {
            name[k] = name[k + 1];
            edition[k] = edition[k + 1];
            cost[k] = cost[k + 1];
          }
          n--;
          j--; 
        }
      }
    }
  }

  void countMoreThan500() {
    int count = 0;
    for (int i = 0; i < n; i++) {
      if (cost[i] > 500) {
        count++;
      }
    }
    cout << "Number of books with cost more than 500: " << count << endl;
  }
};

int main() {
  Library a;
  int ch;
  do {
    cout << "\n\nWhich operation do you want to perform?\n";
    cout << "1. Add book\n2. Display original details\n3. Sort array in descending order\n";
    cout << "4. Remove duplicates with temporary array\n5. Remove duplicates without temporary array\n";
    cout << "6. Copy costs less than 500\n7. Count books with cost more than 500\n8. Exit\n";
    cout << "Enter your choice: ";
    cin >> ch;
    switch (ch) {
    case 1:
      a.entry();
      break;
    case 2:
      a.display();
      break;
    case 3:
      a.sortDescending();
      break;
    case 4:
      a.Duplicate_Temp();
      break;
    case 5:
      a.Duplicate_WithoutTemp();
      break;
    case 6:
      a.copyCostsLessThan500();
      break;
    case 7:
      a.countMoreThan500();
      break;
    case 8:
      cout << "Exiting...";
      break;
    default:
      cout << "Enter a valid choice!";
      break;
    }
  } while (ch != 8);

  return 0;
}
