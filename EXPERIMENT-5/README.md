# Experiment-5
## title 5a)to implememt interface
```
// Interface
interface Sortable {
    void sort(int[] arr);
}

// BubbleSort class implementing Sortable
class BubbleSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;

        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {

                if (arr[j] > arr[j + 1]) {
                    // swap
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
}

// SelectionSort class implementing Sortable
class SelectionSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;

        for (int i = 0; i < n - 1; i++) {

            int minIndex = i;

            for (int j = i + 1; j < n; j++) {
                if (arr[j] < arr[minIndex]) {
                    minIndex = j;
                }
            }

            // swap
            int temp = arr[minIndex];
            arr[minIndex] = arr[i];
            arr[i] = temp;
        }
    }
}

// Main class
public class TestSort {

    public static void main(String[] args) {

        int[] arr1 = {5, 2, 9, 1, 3};

        Sortable ref;

        ref = new BubbleSort();
        ref.sort(arr1);

        System.out.println("Array sorted using BubbleSort:");
        display(arr1);

        int[] arr2 = {8, 4, 7, 6, 2};

        ref = new SelectionSort();
        ref.sort(arr2);

        System.out.println("Array sorted using SelectionSort:");
        display(arr2);
    }

    static void display(int[] arr) {
        for (int num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();
    }
}
```
# output
![5a output](https://github.com/user-attachments/assets/46ad5b2d-6a92-49c3-9b71-255dcce51a4c)
