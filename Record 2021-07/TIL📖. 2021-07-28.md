# TIL ๐ โ๏ธ
     

 ### 1. fetch๋ฅผ ์ด์ฉํ ๋คํธ์ํฌ ์์ฒญ

  - fetch()
    * ๋น๋๊ธฐ ์์ฒญ์ ๋ํ์ ์ธ ์ฌ๋ก๋ก ๋คํธ์ํฌ ์์ฒญ์ด๋ฉฐ, ๋คํธ์ํฌ๋ฅผ ์ด์ฉํ์ฌ ์ด๋ค์ง๋ URL ์์ฒญ
    * ๋๊ฐ Promise์ ํ์์ผ๋ก ๊ตฌ์ฑ๋์ด ์์

  ```js
  
  let los_angeles = "https://api.weather.com/cailfornia/LA"
  let new_york = "https://api.weather.com/newyork/NY"
  let sanfrancisco = "https://api.weather.com/cailfornia/SF"

  let total = [
  				      fetch(los_angeles), 
  				      fetch(new_york), 
  				      fetch(sanfrancisco)
			        ]
              
  Promise.all(total)
    .then((response) => Promise.all(response.map((el) => { return el.json() }))
    .then((json) => console.log(json))
    .catch((error) => console.log(error));

  ```
  
   ### 2. ๋ธ๋ก๊น
   
  - ๋น๋๊ธฐ ํธ์ถ ์ฒ๋ฆฌ
