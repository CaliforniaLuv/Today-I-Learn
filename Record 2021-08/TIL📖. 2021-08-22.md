# TIL ๐ โ๏ธ

   
 ### 1. ์๊ณ ๋ฆฌ์ฆ
 
  - quickSort
    * ์ ์๋ฅผ ์์๋ก ๊ฐ๋ ๋ฐฐ์ด์ ์๋ ฅ๋ฐ์ ์ค๋ฆ์ฐจ์์ผ๋ก ์ ๋ ฌ
    * ํ๊ท ์ ์ผ๋ก ๋งค์ฐ ๋น ๋ฅธ ์ํ ์๋๋ฅผ ์๋ํ๋ ์ ๋ ฌ ๋ฐฉ๋ฒ
    * worst case: O(n^2)
    * best case: O(nlogโn)

  ```js
  

  function quicksort (arr) {
    if(arr.length <= 1) {
        return arr
    }

    let cur = arr[0]
    let left = []
    let rigth = []

    for(let i = 1; i < arr.length; i++) {

        if(arr[i] < cur) {
            left.push(arr[i])
        } else {
            rigth.push(arr[i])
        }
    }

    let leftsort = quicksort(left)
    let rigthsort = quicksort(rigth)

    return [...leftsort, cur, ...rigthsort]
  }
 
  ```
  
   ### 2. ๋ธ๋ก๊น
   
   
    - bubbleSort, selcetSort, insertionSort, quickSort ์ ๋ ฌ 
  
  
