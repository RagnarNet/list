#include <iostream>
#include <clocale>

using namespace std;

void rev(int);

struct node {
	int value;
	node* prev = nullptr;
};


node* g_top(nullptr); // init top of stack

bool isempty() {
	return !g_top;
}

void push(int value) {
	node* tmp = new node();
	tmp->value = value;
	tmp->prev = g_top;
	g_top = tmp;
}

int* pop() {
	if (!isempty()) {
		//int tmp_val = g_top->value;
		int* tmp_val = new int(g_top->value);
		node* tmp_top = g_top;
		g_top = g_top->prev;
		delete tmp_top;
		return tmp_val;
	}
	return nullptr;
}


int main() {

	int n = 10;

	for (int i = 0; i < n; i++)
		push(i + 1);

	rev(n);

	for (int i = 0; i < n; i++)
		cout << *pop() << endl;
	return 0;
}

void rev(int n) {
	int* arr[10];

	for (int i = 0; i < n; i++) {
		arr[i] = pop();
	}

	for (int i = 0; i < n; i++) {
		push(*arr[i]);
	}

}
