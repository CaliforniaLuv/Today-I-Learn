# TIL ๐ โ๏ธ

   
 ### 1. 
 
  - insertionSort
    * bubbleSort์ ๋ด๋ฆผ์ฐจ์๊ณผ ๋ฌ๋ฆฌ insertionSort์ ์ค๋ฆ์ฐจ์์ ํน์ง์ ์ง๋

```js
let insertionSort = function (arr, sortArr = (item) => item) {
  

  for(let i = 1; i < arr.length; i++) {
    let list = arr[i]
    let left = i - 1

    while(left >= 0) {
      if(sortArr(arr[left]) > sortArr(arr[left + 1])) {
        arr[left + 1] = arr[left]
        arr[left] = list
      }
      left--
    }
  
  }
    return arr
};


```

 ### 2. node.js
 
  - res.json()๊ณผ res.send()์ ์ฐจ์ด
    * res.json(obj)
      1. res.json ํจ์์ ๋ช์๋ ์ธ์๋ก๋ obj
      2. obj๋ JSON ๋ฌธ์์ด๋ก ๋ณํ๋์ body๋ผ๋ ๋ณ์์ ์ ์ฅ
      3. Content-Type ํค๋๊ฐ ์ธํ๋์ง ์์์ ๊ฒฝ์ฐ, Content-Type ์ผ๋ก application/json์ ์ธํ(๊ฒฐ๊ตญ ๋ด๋ถ์ ์ผ๋ก send() ํธ์ถ

      ```javascript     
      
      res.json(object)
      res.send(string)
      
      ```
      
    * res.send(body)
      1. res.send ํจ์์ ์ธ์๋ก๋ body๊ฐ ์๊ณ  body๋ ๋ฐ๋ก chunk๋ก ํ ๋น
      2. chunk๊ฐ object ํ์์ด๋ฉด res.json์ ํธ์ถ
      3. ๊ฒฐ๊ตญ ๋ ๊ฐ์ ํจ์๊ฐ ์๋ก ํธ์ถํ๊ธฐ ๋๋ฌธ์ ํจ์ ํธ์ถ ์คํ์ด ๋์นจ

      ```javascript

      res.send(object)
      res.json(object)
      res.send(string)
      
      ```
