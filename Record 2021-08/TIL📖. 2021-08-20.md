# TIL π βοΈ

   
 ### 1. μκ³ λ¦¬μ¦
 
  - bubbleSort
    * ν΄λΉ μμκ° μ°μμ μΌλ‘ μ€λ₯Έμͺ½ μμμ λΉκ΅νμ¬ ν¬λ©΄ μ΄λ μμΌλ©΄ λΉκ΅ λμ μμκ° λ°λλ νΉμ§
    * worst case: O(n^2)
    * best case: O(n)

  ```js
  
function bubbleSort (arr) {

  for(let i = 0; i < arr.length; i++) {
  	for(let j = 0; j < arr.length -1 - i; j++) {
    	if(arr[j] > arr[j + 1]) {
        	let swap = arr[j]
            arr[j] = arr[j + 1]
          	arr[j + 1] = swap
        }
    }
  }
  return arr
}

 
  ```
  
  - Selection Sort
    * μ ν μ λ ¬μ λ§€μ»€λμ¦μ΄ μ§νλ  μλ¦¬λ μ ν΄μ Έ μμΌλ©°, μ²«λ²μ§Έ μλ¦¬μ λ°°μ΄μ μ΅μκ°μ ν λΉνμ¬ μ§ν
    * worst case: O(n^2)
    * best case: O(n^2)
  
   ```js
 
   function selectionSort (arr) {
      for (let i = 0; i < arr.length; i++) {
         let minIndex = i;
         for (let j = i + 1; j < arr.length; j++) {
            if (arr[minIndex] > arr[j]) {
               minIndex = j;
            }
         }
         if (minIndex !== i) {
            let swap = arr[minIndex];
            array[minIndex] = arr[i];
            arr[i] = swap;
         }

      }
      return arr;
   }

  ```
  
  - Insertion Sort
    * λ°°μ΄μ ν μμμΈ keyλΌλ κ°μ μ°μ  κ°μ§κ³  μμΌλ©°, ν΄λΉ keyλ₯Ό μλ§μ μλ¦¬μ μ½μ
    * worst case: O(n^2)
    * best case: O(n)

   ```js
 
   
   function insertionSort (arr) {
      
      for (let i = 1; i < arr.length; i++) {
         let cur = arr[i];
         let left = i - 1;
         
         while (left >= 0 && arr[left] > cur) {
            arr[left + 1] = arr[left];
            arr[left] = cur;
            cur = arr[left];
            left--;
         }
      }
      return arr;
   }

   ```
  

