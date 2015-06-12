# array-pointer
this is how to make a array with pointer in a function


#include <iostream>
using namespace std;

void carray(int *p, int size){
    for(int i = 0; i < size; i++){
    *p = i+1;
    p++;
    }
}
void cmatrix(int *p, int size1,int size2){
    for(int i = 0; i < size1; i++){
        for(int j = 0; j <size2; j++){
            *p = j+1;
            p++;
        }
    }
}

int main(){

int array[3] = {0};
int matrix[2][3] = {0};

carray(array,3);
cmatrix(matrix[0],2,3);

for( int i = 0; i<3; i++){
	cout<<"["<<array[i]<<"]";
}
cout<<endl<<endl;

for(int i = 0; i<2; i++){
	for(int j = 0; j<3; j++){
		cout<<"["<<matrix[i][j]<<"]";
	}
	cout<<endl;
}
return 0;
}
