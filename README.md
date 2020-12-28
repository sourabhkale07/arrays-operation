# Reverse the given array 
This is a demo repository


#include<iostream>
using namespace std;

void swap(int *p,int *q){
	int temp;
	temp = *p;
	*p = *q;
	*q = temp;
}

void reversearray(int a[],int start,int end){
	
	while(start<end){
	swap(&a[start],&a[end]);
	start++;
	end--;
   }
}

void printarray(int a[],int n){

	int i;
	for( i = 0;i<n;i++){
		cout<<a[i]<<" ";
	}
	cout<<endl<<endl;
}

int main(){
	int a[] = {2,3,4,5,6,7,8};
	int n = sizeof(a)/sizeof(a[0]);
	
	printarray(a,n);
	reversearray(a,0,n-1);
	printarray(a,n); 
	
return 0;
}
