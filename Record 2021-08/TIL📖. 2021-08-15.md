# TIL π βοΈ

   
 ### 1. μκ³ λ¦¬μ¦
 
  - LPS

    
  ```js
  const LPS = function (str) {
  // TODO: μ¬κΈ°μ μ½λλ₯Ό μμ±ν©λλ€.
  let result = ""

  for(let i = 0; i < parseInt(str.length / 2); i++) {
    let prefix = str.slice(0, i)
    let suffix = str.slice(str.length - i)

    if(prefix === suffix) {
      result = prefix
    }
  }

  return result.length
};

   
  ```
  
   ### 2. λΈλ‘κΉ
   
   - Redux
     * Redux ν¨ν΄λ
     * actions - reducer - store - view κ³Όμ μ λν μ½λ ν΄μ
