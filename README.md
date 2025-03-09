# Array4
1. Swapping the two elements with the help of temporary variable.

2. Swapping the two elements without the help of temporary variable.
-> a=a+b
   b=a-b;
   a=a-b

3. Reversing the Array.
-> i) Using the another array
   int j=0;
   for(int i=n-1;i>=0;i--){
     ans[j++]=arr[i];
   }

   or

   int i=n-1,j=0;
   while(i>=0){
    ans[j++]=arr[i];
   }

-> ii)Using the same array
    // Online Java Compiler
// Use this editor to write, compile and run your Java code online

class Main {
    static void printArray(int[] arr){
        for(int i=0;i<arr.length;i++){
            System.out.print(arr[i]);
        }
        System.out.println();
    }
    static void swap(int[] arr,int a, int b){
        int n=arr.length;
        int temp=arr[a];
        arr[a]=arr[b];
        arr[b]=temp;
    }
    public static void main(String[] args) {
        int arr[] = {1,2,3,4,5,6,7,8};
        int n=arr.length;
        printArray(arr);
        int i=0;
        int j=n-1;
        while(i<j){
            swap(arr,i,j);
            i++;
            j--;
        }
        printArray(arr);
    }
}

4.Given a value k , rotate the Array K times given k is a non negative integer.

->i) With Different Array
    import java.util.Scanner;

class Main {
    static void printArray(int[] arr) {
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " "); // ✅ Added space for better readability
        }
        System.out.println();
    }

    static int[] rotateArray(int[] arr, int k) {
        int n = arr.length;
        k = k % n;
        int j = 0;
        int[] ans = new int[n];

        for (int i = n - k; i < n; i++) {
            ans[j++] = arr[i];
        }
        for (int i = 0; i < n - k; i++) { 
            ans[j++] = arr[i];
        }
        return ans;
    }

    public static void main(String[] args) {
        int arr[] = {1, 2, 3, 4, 5, 6, 7, 8};
        printArray(arr);

        System.out.println("Enter the rotate constant:");
        Scanner sc = new Scanner(System.in);
        int k = sc.nextInt();
        sc.close();

        int[] ans = rotateArray(arr, k);
        printArray(ans);
    }
}

->ii)With the same Array
  
   
