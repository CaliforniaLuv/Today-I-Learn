# TIL ๐ โ๏ธ


 ### 1. ๊ฐ์ฒด์งํฅ์ธ์ด OOP
 
  - ์๋ฐ์คํฌ๋ฆฝํธ Object.prototype
    * ์ํ ๊ฐ์ฒด์ ํน์ง์ธ ๊ด๊ณ๋ก ์์ฑ ๊ฐ์ฒด์ ๋ณต์ 
    
    ```javascript
      var student = {
  		name: 'Lee',
  		score: 90
	    };

	  console.dir(student)
	  // __proto__ ๋ถ๋ชจ ๊ฐ์ฒด์ ์์๋ ๊ฒ์ ๋ปํ๋ค.

	  console.log(student.__proto__ === Object.prototype); // true
	  // Object.prototype ์๋ฐ์คํฌ๋ฆฝํธ์ ๋ถ๋ชจ ๊ฐ์ฒด๋ฅผ ์๋ฏธ
    ```
     

 ### 2. ํ๋ก๊ทธ๋๋จธ์ค
 
  - ์์ฃผํ์ง ๋ชปํ ์ ์
  
   ```javascript
      function solution(participant, completion) {

    participant.sort()
    completion.sort()
    
    for (let i = 0; i < participant.length; i++) {
        if(participant[i] !== completion[i]) {
           let result = participant[i]      
            return result;
        }
    }
    
    }
   ``` 

   * sort()๋ก ๊ฐ ๋์ ์, ์์ฃผ์ ์ ๋ ฌํ์ฌ ์ง์ด ์๋ ๊ฒฝ์ฐ ์์ฃผ ๋ชปํ ์ ์๋ก ํ๋จ
