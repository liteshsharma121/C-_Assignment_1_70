#include <iostream>
using namespace std;

class Student
{
private:
    char name[30];
    int rollNo;
    int marks;

public:

    // Constructor
    Student()
    {
        cout << "Enter Student Name: ";
        cin >> name;

        cout << "Enter Roll No: ";
        cin >> rollNo;

        cout << "Enter Marks: ";
        cin >> marks;

        cout << "\nConstructor called." << endl;
    }

    // User-defined function
    void display()
    {
        cout << "\n--- Student Details ---" << endl;
        cout << "Name     : " << name << endl;
        cout << "Roll No. : " << rollNo << endl;
        cout << "Marks    : " << marks << endl;
    }

    // User-defined function
    void checkResult()
    {
        if (marks >= 40)
        {
            cout << "Result   : PASS" << endl;
        }
        else
        {
            cout << "Result   : FAIL" << endl;
        }
    }

    // Destructor
    ~Student()
    {
        cout << "\nDestructor called." << endl;
    }
};

int main()
{
    Student s;

    s.display();
    s.checkResult();

    return 0;
}
