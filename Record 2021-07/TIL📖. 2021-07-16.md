# TIL ๐ โ๏ธ
     

 ### 1. ์๊ณ ๋ฆฌ์ฆ
 
  - ํ๋ก๊ทธ๋๋จธ์ค 2016๋
    * getDay() ๋ฉ์๋๋ฅผ ํตํด ์์ผ ๊ฐ ์ถ์  ๊ฐ๋ฅ
    * new Date('ํด๋น๋๋ ๋ฐ ์, ์ผ') ์์ฑ ์ ๊ฒ์ ๊ฐ๋ฅ
    * switch๋ฌธ์ผ๋ก ๋๋ ์ ์งํ
    * [] ๋ฐฐ์ด๋ก ๋๋์ด ๋ก์ง ๊ตฌํ๋ 


     ```javascript

          function solution(a, b) {
    // new Date("2016-05-26").getDay() // 4
    // 0๋ถํฐ ํ ์์ผ 
    let month = a
    let day = b
    let _2016_day = new Date(`2016-${a}-${b}`).getDay()
    
    
    switch(_2016_day) {
    case 0:
    return "SUN"
    case 1:
    return "MON"
    case 2:
    return "TUE"
    case 3:
    return "WED"
    case 4:
    return "THU"
    case 5:
    return "FRI"
    default :
    return "SAT"
    }
}

     ```
