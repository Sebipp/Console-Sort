    #include <iostream>
    #include <fstream>
    using namespace std;

    int main()
    {
        cout<<"This program sorts the text file named 'FILE', if you do not have it you have to create it/rename the one you want"
        <<endl<<"(the program needs to be in the same folder as the file)"<<endl<<endl;
    
        int k=0;
        string a[2000];
    
        ifstream f("FILE.txt");
        while (f>>a[i])
           k++;
        k-;
        cout<<"The unsorted file (if empty then it wasn't found):"<<endl;
        for (int j=0;j<i;j++)
            cout<<a[j]<<" ";
        cout<<endl;
        
        for (int i = 0; i < k - 1; i++)
         for (int j = 0; j < k - i - 1; j++)
             if (arr[j] > arr[j + 1])
                {
                    string temp = a[j];
                    a[j] = a[j + 1];
                    a[j + 1] = temp;
                }
    
        cout<<"The sorted file:"<<endl<<endl;
        for (int j=0;j<k;j++)
            cout<<a[j]<<" ";
    }
