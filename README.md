# Console-Sort
Shows a file sorted in the console

#include <iostream>
#include <fstream>
using namespace std;

int i=0;
string a[2000];
void bubbleSort(string arr[], int k)
{
    for (int i = 0; i < k - 1; i++)
        for (int j = 0; j < k - i - 1; j++)
            if (arr[j] > arr[j + 1])
            {
                string temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
}

int main()
{
    cout<<"This program sorts the text file named 'FILE', if you do not have it you have to create it/rename the one you want"
    <<endl<<"(the program needs to be in the same folder as the file)"<<endl<<endl;

    ifstream f("FILE.txt");
    while (f>>a[i])
        i++;
    i--;
    cout<<"The unsorted file (if empty then it wasn't found):"<<endl;
    for (int j=0;j<i;j++)
        cout<<a[j]<<" ";
    cout<<endl;
    bubbleSort(a,i);
    cout<<"The sorted file:"<<endl<<endl;
    for (int j=0;j<i;j++)
        cout<<a[j]<<" ";
}
