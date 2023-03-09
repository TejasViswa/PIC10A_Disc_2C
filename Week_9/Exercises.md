# Exercises

## Question 1
Write a class for a Rectangle:
1. Provide two constructors:
	a. A default constructor that sets the rectangle to a unit square;
	b. A constructor to construct a rectangle with a givenwidthandheight;
2. Member functions getperimeter and getarea that compute and return the perimeter and area;
3. Member function void resize(double factor) that resizes the rectangle by multiplying the width and height by the given factor.
### Solution
```c++
# include <iostream>

using namespace std;



class Rectangle {

public:
	Rectangle();
	Rectangle(double L1, double L2);
	double get_perimeter() const;
	double get_area() const;
	void resize(double factor);
private:
	double width;
	double length;

};


Rectangle::Rectangle() {
	width = 1;
	length = 1;
}

Rectangle::Rectangle(double L1, double L2) {
	width = L1;
	length = L2;
}

double Rectangle::get_perimeter() const {
	double perimeter = 2 * (width + length);
	return perimeter;
}

double Rectangle::get_area() const {
	double area = width * length;
	return area;
}

void Rectangle::resize(double factor) {
	width = factor * width;
	length = factor * length;
}


int main() {
    
	Rectangle r1; //default, unit sq

	double perimeter_1 = r1.get_perimeter();
	cout << "The perimeter of rectangle is " << perimeter_1 << endl;
	double area_1 = r1.get_area(); 
	cout << "The area of rectangle is " << area_1 << endl;

	r1.resize(1.5);
	perimeter_1 = r1.get_perimeter();
	cout << "The perimeter of rectangle after resizing is " << perimeter_1 << endl;
	area_1 = r1.get_area();
	cout << "The area of rectangle after resizing is " << area_1 << endl;


	Rectangle r2(4, 10); // self defined 4by10

	double perimeter_2 = r2.get_perimeter();
	cout << "The perimeter of rectangle is " << perimeter_2 << endl;
	double area_2 = r2.get_area();
	cout << "The area of rectangle is " << area_2 << endl;

	r2.resize(1.5);
	perimeter_2 = r2.get_perimeter();
	cout << "The perimeter of rectangle after resizing is " << perimeter_2 << endl;
	area_2 = r2.get_area();
	cout << "The area of rectangle after resizing is " << area_2 << endl;

}
```

## Question 2
Write a class Bug that models a bug moving along a horizontal line. The bug moves either to the right or left. Initially, the bug moves to the right,but it can turn to change its direction. In each move, its position changesby one unit in the current direction. You may also practice separat ecompilation for this example (may discuss this on next discussion session).

1. Provide two constructors
	a. Bug()(Default constructor, set initial position to be 0.)
	b. Bug(int initialposition)
2. Member functions
	a. void turn()
	b. void move()
	c. int getposition()
### Solution
```c++
# include <iostream>

using namespace std;



class Bug {
public:
	Bug();
	Bug(int initial_position);
	void move();
	void turn();
	int get_position() const;
private:
	int bug_position;
	int direction; // 1: move right, -1: move left
};

Bug::Bug() {
	bug_position = 0;
	direction = 1;
}

Bug::Bug(int initial_position) {
	bug_position = initial_position;
	direction = 1;
}

void Bug::move() {
	bug_position = bug_position + direction;
}

void Bug::turn() {
	direction = -direction;
}

int Bug::get_position() const {
	return bug_position;
}



int main() {

	Bug bug(10);
	cout << "Current position: " << bug.get_position() << endl;
	bug.turn();
	cout << "Turn Direction!" << endl;
	bug.move();
	cout << "Current position: " << bug.get_position() << endl;
	bug.move();
	cout << "Current position: " << bug.get_position() << endl;
	bug.move();
	cout << "Current position: " << bug.get_position() << endl;
	bug.move();
	cout << "Current position: " << bug.get_position() << endl;
	bug.turn();
	cout << "Turn Direction!" << endl;
	bug.move();
	cout << "Current position: " << bug.get_position() << endl;
	bug.move();
	cout << "Current position: " << bug.get_position() << endl;
	bug.move();
	cout << "Current position: " << bug.get_position() << endl;

}
```
