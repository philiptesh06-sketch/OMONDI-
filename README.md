#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    int arr[20], odd[20], even[20];
    int oddIdx = 0, evenIdx = 0;

    srand(time(0));
    for (int i = 0; i < 20; i++) arr[i] = rand() % 100 + 1;

    for (int i = 0; i < 20; i++) {
        if (arr[i] % 2 == 0) even[evenIdx++] = arr[i];
        else odd[oddIdx++] = arr[i];
    }

    cout << "Odd: ";
    for (int i = 0; i < oddIdx; i++) cout << odd[i] << " ";
    cout << "\nEven: ";
    for (int i = 0; i < evenIdx; i++) cout << even[i] << " ";
    return 0;
}
import random

# Generate 20 random numbers between 1 and 100
numbers = [random.randint(1, 100) for _ in range(20)]

# Split into odd and even lists
odd = [n for n in numbers if n % 2 != 0]
even = [n for n in numbers if n % 2 == 0]

print("Original:", numbers)
print("Odd:", odd)
print("Even:", even)
