# TIL ๐ โ๏ธ

   
 ### 1. ์๊ณ ๋ฆฌ์ฆ
 
  - balancedBrackets
    
  ```js
   const balancedBrackets = function (str) {
   
    let objBr = {
      "[" : "]",
      "(" : ")",
      "{" : "}"
    }
    let stack = []
    let closer = "])}"
    
    
    for(let i = 0; i < str.length; i++) {
      if(str[i] in objBr) {
        stack.push(str[i])
      } else if(closer.includes(str[i])) {
        let top = stack.pop()
        let check = objBr[top]
          if(check !== str[i]) {
            return false;        
          }
      }
    }

    return stack.length === 0
   }
   
  ```
  
   * ์ด๋ฆฌ๊ณ  ๋ซํ๋ ๊ณผ์ ์ด ์ฑ๋ฆฝ๋๋ฉด ์์ฐ์ค๋  ํด์ฅํ๋๋ก stack ์๋ฃ๊ตฌ์กฐ๋ฅผ ์์ฉํ๋ค.
   * ์ด๋ฆฌ๋ bracket์ objBr ๊ฐ์ฒด๋ก ์ ์ฅ, ๋ซํ๋ bracket์ closer ๋ฌธ์์ด๋ก ์ ์ฅ
   * ๋ฐ๋ณต๋ฌธ ๊ณผ์ ์์ ๋ง์ผ ํด๋น ์ธ๋ฑ์ค๊ฐ ์ด๋ฆฌ๋ ๋ฐฐ์ด ์์์ ๊ฒฝ์ฐ if(str[i] in objBr)
   * ๋ซํ๋ ๊ณผ์ ์ผ ๊ฒฝ์ฐ closer.includes(str[i])๋ก ๋ถ๋ฆฌ ํ๋ค

 ### 2. React UI Component ์ ๋ฆฌ

 - Modal
 - toggle
 - tap
 - tags
 - Autocomplete
 - ClickToEdit 
