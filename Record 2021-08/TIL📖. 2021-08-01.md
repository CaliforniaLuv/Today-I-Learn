# TIL π βοΈ


 ### 1. binary search tree 
  
  - μκ°λ³΅μ‘λ μ΅μνμ λ°λ₯Έ μ½λ λ¦¬νν λ§

     * μ¬κ·ν¨μλ₯Ό ν΅ν΄ μκ°λ³΅μ‘μ μ΅μν
  
  ```js
  
    let nums = [0, 2, 5, 8, 11, 15, 18, 19] 
    
    function binarySearch(array, target) {
      return binarySearchAdd(array, target, 0, array.length - 1)
    }
    
    function binarySearchAdd(array, target, left, right) {
      
      let mid = parseInt((left + right) / 2) 
      
      if(left > right) {
        return false
      } else if(target < array[mid]) {
        return binarySearchAdd(array, target, left, mid - 1)
      } else {
        return binarySearchAdd(array, target, mid + 1, right)
      }
    }
    
   ```
     

 ### 2. λΈλ‘κΉ
 
  - μλ£κ΅¬μ‘° Tree μ λ¦¬
