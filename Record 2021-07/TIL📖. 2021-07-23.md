# TIL ๐ โ๏ธ
     

 ### 1. ์๊ณ ๋ฆฌ์ฆ
 
  - bubbleSort

  ```js
     
    const bubbleSort = function (arr) { 
      for(let i = 0; i < arr.length; i++) {
          let count = 0;
        for(let j = 0; j < arr.length - i - 1; j++) {
          if(arr[j] > arr[j+1]) {
            count++
            arrSort(j, j + 1, arr)
          }
        }
           if(count === 0) {
        break;
      }
      }
      return arr
    }


    function arrSort(num1, num2, arr) {
      return [arr[num1], arr[num2]] = [arr[num2], arr[num1]]
    }
  ```
 
  * arrSort() ํจ์ํ ํ๋ก๊ทธ๋๋ฐ์ผ๋ก ๊ตฌ์ฑํ์ฌ ๊ตฌ์กฐ๋ถํดํ ๋น์ผ๋ก ๋ฐฐ์ด ์์ ๋ณ๊ฒฝ
  
