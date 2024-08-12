# CDS-experiment-8
AIM:- To study and implement C++ multidimensional arrays (matrices) <br>

Software Used:- VS code<br>

Theory:-<br>
A multidimensional array in C++ is an array of arrays that enables tabular data storage. A 2D array, for instance, can be shown as a matrix with rows and columns. A 3x4 matrix is created when it is stated with multiple sets of square brackets, such as {int matrix[3][4];}. Two indices—one for the row and one for the column—are used to access each element. Similar to this, 3D arrays like {int cube[2][3][4];{ add a dimension. These arrays are helpful for displaying intricate data structures like tables, grids, and matrices. Performance with large multidimensional arrays depends on effective memory management and access patterns.<br>

Code:-<br>
 
    #include <iostream>
    using namespace std;

    int main() {
    int r, c;

    // Ask for matrix dimensions
    cout << "Enter the number of rows: ";
    cin >> r;
    cout << "Enter the number of columns: ";
    cin >> c;

    // Declare matrices
    int m1[r][c], m2[r][c], sum[r][c], prod[r][c];

    // Input elements for the first matrix
    cout << "Enter the elements of the first matrix:\n";
    for (int i = 0; i < r; i++) {
        for (int j = 0; j < c; j++) {
            cout << "Element [" << i + 1 << "][" << j + 1 << "]: ";
            cin >> m1[i][j];
        }
    }

    // Input elements for the second matrix
    cout << "Enter the elements of the second matrix:\n";
    for (int i = 0; i < r; i++) {
        for (int j = 0; j < c; j++) {
            cout << "Element [" << i + 1 << "][" << j + 1 << "]: ";
            cin >> m2[i][j];
        }
    }

    // Perform matrix addition
    for (int i = 0; i < r; i++) {
        for (int j = 0; j < c; j++) {
            sum[i][j] = m1[i][j] + m2[i][j];
        }
    }

    // Perform matrix multiplication
    for (int i = 0; i < r; i++) {
        for (int j = 0; j < c; j++) {
            prod[i][j] = 0;
            for (int k = 0; k < c; k++) {
                prod[i][j] += m1[i][k] * m2[k][j];
            }
        }
    }

    // Calculate diagonal sum of the first matrix
    int diagSum = 0;
    for (int i = 0; i < r; i++) {
        diagSum += m1[i][i];
    }

    // Check if the elements of the first row are equal to the elements of the second row in the first matrix
    bool rowEqual = true;
    for (int j = 0; j < c; j++) {
        if (m1[0][j] != m1[1][j]) {
            rowEqual = false;
            break;
        }
    }

    // Display the first matrix
    cout << "\nThe first matrix is:\n";
    for (int i = 0; i < r; i++) {
        for (int j = 0; j < c; j++) {
            cout << m1[i][j] << " ";
        }
        cout << endl;
    }

    // Display the second matrix
    cout << "\nThe second matrix is:\n";
    for (int i = 0; i < r; i++) {
        for (int j = 0; j < c; j++) {
            cout << m2[i][j] << " ";
        }
        cout << endl;
    }

    // Display the sum of the matrices
    cout << "\nThe resultant matrix after addition is:\n";
    for (int i = 0; i < r; i++) {
        for (int j = 0; j < c; j++) {
            cout << sum[i][j] << " ";
        }
        cout << endl;
    }

    // Display the product of the matrices
    cout << "\nThe resultant matrix after multiplication is:\n";
    for (int i = 0; i < r; i++) {
        for (int j = 0; j < c; j++) {
            cout << prod[i][j] << " ";
        }
        cout << endl;
    }

    // Display the diagonal sum of the first matrix
    cout << "\nThe diagonal sum of the first matrix is: " << diagSum << endl;

    // Display whether the first row is equal to the second row in the first matrix
    if (rowEqual) {
        cout << "The elements of the first row are equal to the elements of the second row in the first matrix.\n";
    } else {
        cout << "The elements of the first row are NOT equal to the elements of the second row in the first matrix.\n";
    }

    return 0;
    }


Conclusion:-<br>
in this experiment we learnt to use the multidimensional arrays (matrix) and how to perform operations on them<br>






