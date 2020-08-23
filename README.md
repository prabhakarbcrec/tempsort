import matplotlib.pyplot as plt
ax = plt.gca()
font = {'family': 'serif',
        'color':  'darkred',
        'weight': 'normal',
        'size': 16,
        }
plt.xlabel('Date and Time',fontdict=font)
plt.ylabel('Number Of Confirmed cases of Covid-19',fontdict=font)
plt.title('Covid-19 Data Analysis Among Countrys',fontdict=font)
plt.text(55, 10, r'$INDIA$', fontdict=font)
plt.legend()
#plt.text(55, 3, r'$INDIA$', fontdict=font)
#fig.set_size_inches(30.5, 20.5)
covidIndData.plot(x='Last Update',y='Confirmed',label='INDIA',color='Black',figsize=(16,10),ax=ax)
covidItalyData.plot(x='Last Update',y='Confirmed',color='red',label='ITALY',ax=ax)
covidSpainData.plot(x='Last Update',y='Confirmed',color='blue',label='SPAIN',ax=ax)
#Pakistan.plot(x='Last Update',y='Confirmed',color='green',label='PAKISTAN',ax=ax)




code share li k:
https://drive.google.com/file/d/1lcCzCu6q9vfBzLubwhn0UFtDBa2-QLtx/view?usp=sharing coda

https://drive.google.com/drive/folders/12EE3O_BMbsNo-lPG53gNsiZITDQOmJSh?usp=sharing



https://ide.geeksforgeeks.org/cdPM9zDe4v

https://ide.geeksforgeeks.org/EQgwj8nSvR


https://www.java2novice.com/java-sorting-algorithms/quick-sort/ start sortinmg from here

https://www.codepedia.org/

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
