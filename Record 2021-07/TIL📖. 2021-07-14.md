# TIL ๐ โ๏ธ
     

 ### 1. ์๊ณ ๋ฆฌ์ฆ (ํ๋ก๊ทธ๋๋จธ์ค)
 
  - K๋ฒ์งธ์
    * ์ฃผ์ด์ง ๋ฐฐ์ด์ ๋ง์ถฐ์ง ๋ณ๋์ ๋ฐฐ์ด ์ ๋ฆฌ
    * sort ๋ฉ์๋ ์์ฉํ์ฌ ์ ๋ ฌ 
    * slice ๋ฉ์๋๋ฅผ ํตํด ์ํ๋ ์์น ์ ๋ฆฌ
    * ๊ทธ๋ฌ๋ slice๋ ์๊ฐ ๋ณต์ก๋์ ๊ด๋ จํ์ฌ ์ฑ๋ฅ ์ ํ๋ฅผ ์ผ๊ธฐ ์ํค๋ฏ๋ก ์ฃผ์ํ์ฌ ์ธ ๊ฒ!!!!
  
  ```javascript
  
  function solution(array, commands) {
    var answer = [];
    // commands [[2, 5, 3], [4, 4, 1], [1, 7, 3]]
    // sortArr  [1, 2, 3, 4, 5, 6, 7]
    
    for (let i = 0; i < commands.length; i++) {
        // ์๋ฅด๊ณ 
        let arrnew = array.slice(commands[i][0] - 1, commands[i][1])
        // ์ ๋ ฌํด์
        arrnew.sort((x, y) => x - y)
        // k๋ฒ์งธ ์๋ฆฌ ๋น๋ฐฐ์ด ํ ๋นํด์ค๋ผ
        answer.push(arrnew.slice(commands[i][2] - 1, commands[i][2]))
    }

    return answer.flat();
}
  ```
  
