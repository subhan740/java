import java.util.*; 
  
class GFG 
{ 
// function to print half of the array in  
// ascending order and the other half in  
// descending order 
static void printOrder(int[] arr, int n) 
{ 
    // sorting the array 
    Arrays.sort(arr); 
  
    // printing first half in ascending  
    // order 
    for (int i = 0; i < n / 2; i++)  
        System.out.print(arr[i]+" "); 
  
    // printing second half in descending  
    // order 
    for (int j = n - 1; j >= n / 2; j--) 
    System.out.print(arr[j]+" "); 
      
} 
  
// Driver code 
public static void main(String[] args) 
{ 
    int[] arr = { 5, 4, 6, 2, 1, 3, 8, 9, 7 }; 
    int n = arr.length; 
    printOrder(arr, n); 
  
} 
} 
/* This code is contributed by Mr. Somesh Awasthi */

public class SecondLargestInArrayExample{
public static int getSecondLargest(int[] a, int total){
int temp;
for (int i = 0; i < total; i++) 
        {
            for (int j = i + 1; j < total; j++) 
            {
                if (a[i] > a[j]) 
                {
                    temp = a[i];
                    a[i] = a[j];
                    a[j] = temp;
                }
            }
        }
       return a[total-2];
}
public static void main(String args[]){
int a[]={1,2,5,6,3,2};
int b[]={44,66,99,77,33,22,55};
System.out.println("Second Largest:"+getSecondLargest(a,6));
System.out.println("Second Largest:"+getSecondLargest(b,7));
}}
1.	package com.candidjava;
2.	 
3.	public class SecondLargest {
4.	 
5.		public static void main(String[] args) {
6.	 
7.			int arr[] = { 14, 46, 47, 86, 92, 52, 48, 36, 66, 85 };
8.			int largest = arr[0];
9.			int secondLargest = arr[0];
10.			
11.			System.out.println("The given array is:" );
12.			for (int i = 0; i < arr.length; i++) {
13.				System.out.print(arr[i]+"\t");
14.			}
15.			for (int i = 0; i < arr.length; i++) {
16.	 
17.				if (arr[i] > largest) {
18.					secondLargest = largest;
19.					largest = arr[i];
20.	 
21.				} else if (arr[i] > secondLargest) {
22.					secondLargest = arr[i];
23.	 
24.				}
25.			}
26.	 
27.			System.out.println("\nSecond largest number is:" + secondLargest);
28.	 
29.		}
30.	}


public class ThirdLargestNumberInAnArray {
   public static void main(String args[]){
      int temp, size;
      int array[] = {10, 20, 25, 63, 96, 57};
      size = array.length;

      for(int i = 0; i<size; i++ ){
         for(int j = i+1; j<size; j++){

            if(array[i]>array[j]){
               temp = array[i];
               array[i] = array[j];
               array[j] = temp;
            }
         }
      }
      System.out.println("Third second largest number is:: "+array[size-2]);
   }
}

