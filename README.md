// geometry-calculator

#include<iostream>
#include<cmath>
using namespace std;

int main()
{
	const float PI = 3.14159;
	int choice;

	cout << "Geometry Calculator" << endl << endl;
	cout << "1. Calculate the area of a circle" << endl;
	cout << "2. Calculate the area of a rectangle" << endl;
	cout << "3. Calculate the area of a triangle" << endl;
	cout << "4. Quit" << endl << endl;
	cout << "Enter your choice (1-4)" << endl;
	cin >> choice;
	cout << endl;

	switch (choice)
	{
		float area;

		case 1:
			int radius;
			cout << "What is the radius?: ";
			cin >> radius;
			if (radius < 0)
			{
				cout << "Sorry! You must enter a positive number!";
			}
			else
			{
				area = PI * pow(radius, 2);
				cout << "The area of the circle is " << area << endl;
			}
			break;

		case 2:
			float width, length;
			cout << "What is the length?: "<<endl;
			cin >> length;
			if (length > 0)
			{
				cout << "What is the wdith?: "<<endl;
				cin >> width;

				if (width > 0)
				{
					area = length * width;
					cout << "The area of the rectangle is " << area << endl;
				}
				else
				{
					cout << "Sorry! The width must be greater than 0." << endl;
				}
			}
			else
			{
				cout << "Sorry! The length must be greater than 0." << endl;
			}
			break;

		case 3:
			int height, base;
			cout << "What is the base?: " << endl;
			cin >> base;
			if (base > 0)
			{
				cout << "What is the height?: " << endl;
				cin >> height;

				if (height > 0)
				{
					area = (base * height) * .5;
					cout << "Area of the triangle is: " << area << endl;
				}
				else
				{
					cout << "Sorry! The height must be greater than 0." << endl;
				}
			}
			else
			{
				cout << "Sorry! The base must be greater than 0." << endl;
			}
			break;

		case 4:
			cout << "Thank you for using the program!" << endl;
			break;

		default:
			cout << "Sorry! Your choice must be between 1 and 4. Rerun the program!" << endl;
			break;

	}

	cout << endl;

	return 0;
}
