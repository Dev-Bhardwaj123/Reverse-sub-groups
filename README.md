# Reverse-sub-groups
Reverse sub groups of array with d places
//Reverse sub groups of arrays w.r.t d places 
#include<iostream>
using namespace std;

void rev(int arr[],int s,int e){
	while(s<=e){
		int temp=arr[s];
		arr[s]=arr[e];
		arr[e]=temp;
		s++;
		e--;
	}
}

int main(){
	int n;
	cout<<"Enter size of array: ";
	cin>>n;
	int arr[n];
	for(int i=0;i<n;i++){
		cin>>arr[i];
	}
	int d;
	cout<<"Reverse group: ";
	cin>>d;
	for(int i=0;i<n;i+=d){
		rev(arr,i,i+d-1);
	}
	for(int i=0;i<n;i++){
		cout<<arr[i]<<" ";
	}
	return 0;
}
