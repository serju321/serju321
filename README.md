#include <iostream>

void reverseArray(double arr[], int size) {
    for (int i = 0; i < size / 2; ++i) {
        // Меняем элементы местами, начиная с краев массива
        double temp = arr[i];
        arr[i] = arr[size - 1 - i];
        arr[size - 1 - i] = temp;
    }
}

int main() {
    double arr[] = {1, 2, 3, 4, 5};
    int size = sizeof(arr) / sizeof(arr[0]);

    std::cout << "Исходный массив: ";
    for (int i = 0; i < size; ++i) {
        std::cout << arr[i] << " ";
    }

    reverseArray(arr, size);

    std::cout << "\nМассив после изменения порядка: ";
    for (int i = 0; i < size; ++i) {
        std::cout << arr[i] << " ";
    }

    std::cout << std::endl;

    return 0;
}
