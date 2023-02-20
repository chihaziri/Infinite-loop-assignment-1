#include <iostream>
#include <sstream>
#include <string>

using namespace std;
bool isNumber(string s)
{
	std::stringstream ss(s);
	float x;
	return (ss >> x) && ss.eof();
}

int main()
{
	// declare and store choice, user's name, age and occupation
	// changed age declaration to integer//
	int choice = 0;
	
	string name = "";
	int age = 0;
	string occup = "";

	//start the loop
	while (choice != -1)
	{
		// declare the input
		string input = "";
		choice = 0;

		cout << "-1: Exit\n";
		cout << "1: Enter Name\n";
		cout << "2: Enter Age\n";
		cout << "3: Enter Occupation\n";
		cin >> choice;

		//removed if statement from comments//
			if (choice== -1)
			break; 

		getline(cin, input);
		
		if (isNumber(input));
		switch (choice)
		{

		case 1:
			cout << "What is your Name: \n";
			getline(cin, name);
			break;
		case 2:
			cout << "What is your Age? \n";
			cin >> age;
			break;
		case 3:
			cout << "What is your Occupation? \n";
			getline (cin, occup);
			break;
		default:
			// Assume Invalid Menu Choice
			cout << "Sorry that choice is not valid!";
			continue;
		}
	}

	age += 1;

	cout << "Thank you for using our application, " << name << " and hope your career in " << occup << " is successful.";
	cout << "Hope your " << age << " birthday will enjoyable and exciting";

	return 0;
}
