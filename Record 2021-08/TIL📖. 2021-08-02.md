# TIL ๐ โ๏ธ


 ### 1. ์๊ณ ๋ฆฌ์ฆ
  
  - ๋ถ์กฑํ ๊ธ์ก ๊ณ์ฐํ๊ธฐ
  
  ```js
  
    function solution(price, money, count) {
    
      let sum = price

      for(let i = 2; i <= count; i++) {
        sum = sum + (price * i)
      }
    
      return sum < money ? 0 : sum - money
     }
     
   ```
   
 ### 2. React
 
  - useEffect
    * ๊ฐ ์ข์ ๋ฐฐ์ด์ ์ฐจ์ด ๊ตฌ๋ณ
      1. []: ํ๋ฒ๋ง useEffect ๊ธฐ๋ฅ์ด ์คํ (์ธ๋ถ ๋ฆฌ์์ค ์ ๊ทผํ  ๊ฒฝ์ฐ)
      2. ์ง์ ์ํ  ๊ฒฝ์ฐ: ๋งค ํด๋น ์ปดํฌ๋ํธ ๋ด์์ ๋ณํ๊ฐ ์ผ์ด๋  ๊ฒฝ์ฐ useEffect ๊ธฐ๋ฅ์ด ์คํ
      3. [value]: ํด๋น value์ ๋ํ ๊ฐ์ด ๋ณํ๊ฐ ์ผ์ด๋  ๊ฒฝ์ฐ๊ฐ useEffect ๊ธฐ๋ฅ์ด ์คํ
     

