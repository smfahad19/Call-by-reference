# Call-by-reference
#include <iostream>
using namespace std;
	void swapPointer(int* a , int* b){
		int temp = *a;
		*a = *b;
		*b = temp;
	}
int main(){
	int a = 5 , b = 7;
	cout<<"before swap the value of a " << a << " and the value at b is " << b <<endl;
	swapPointer(&a , &b);	
	cout<<"After swap the value of a " << a << " and the value at b is " << b <<endl;

	return 0;
}

//Now using call by value
#include <iostream>
using namespace std;
	int* swapPointer(int &a , int &b){
		int temp = a;
		a = b;
		b = temp;
	}
int main(){
	int a = 5 , b = 7;
	cout<<"before swap the value of a " << a << " and the value at b is " << b <<endl;
	swapPointer(a , b);	
	cout<<"After swap the value of a " << a << " and the value at b is " << b <<endl;

	return 0;
