https://ide.geeksforgeeks.org/cdPM9zDe4v

https://ide.geeksforgeeks.org/EQgwj8nSvR

above link is to refer on GFG

import java.io.*;

class prabhakar {
	public static void main (String[] args) {
		int [] arr=new int[]{12,11,4,3,67,4};
	System.out.println("Unsorted Array:");
	int n=arr.length-1;

	//start sorting
	mergeSort(arr,0,n);
		for(int a:arr)
	{
	    	System.out.print(""+a+" ");
	}
	

	}
	public static void mergeSort(int array[],int low,int high){
	   
	    if(high<=low)
	    {
	       return; 
	    }
	     int mid=(low+high)/2;
	     mergeSort(array,low,mid);
	     mergeSort(array,mid+1,high);
	    merge(array,low,mid,high);
	    
	    
	}
	public static void merge(int array[],int low,int mid,int high){
	    int left[]=new int[mid - low + 1];
	    int right[]=new int[high - mid];
	    for(int i=0;i<left.length;i++)
	    {
	        left[i]=array[low + i];
	    }
	    for(int i=0;i<right.length;i++)
	    {
	        right[i]=array[mid+1+i];
	    }
	    int leftIndex = 0;
    int rightIndex = 0;
   for (int i = low; i < high + 1; i++)
    {
	    if(leftIndex<left.length&&rightIndex<right.length)
	    {
	        if(left[leftIndex]<right[rightIndex])
	        {
	            array[i]=left[leftIndex];
	            
	       leftIndex++;
	        }
	        else{
	             array[i]=right[rightIndex];
	            
	       rightIndex++;
	        }
	    }
	    else if (leftIndex < left.length) {
           
            array[i] = left[leftIndex];
            leftIndex++;
        } else if (rightIndex < right.length) {
           
            array[i] = right[rightIndex];
            rightIndex++;
        }
    }
	}
}
