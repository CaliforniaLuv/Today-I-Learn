# TIL ๐ โ๏ธ
     

 ### 1. ์๊ณ ๋ฆฌ์ฆ
 
  - isSubsetOf

  ```js
     let isSubsetOf = function (base, sample) {

  // ๊ทธ๋ฅ sort() ํด๋ฒ๋ฆฌ๋ฉด ์๊ฐ ๋ณต์ก๋์ ๋ฐ๋ผ ์์ฒญ ๋นํจ์จ์ ์ด๋ฏ๋ก ์ค๋ฆ์ฐจ์ ์กฐ๊ฑด ์ค์ ํ๊ธฐ!!
  base.sort((a, b) => a - b)
  sample.sort((a, b) => a - b)


  let baseIdx = 0
  for(let i = 0; i < sample.length; i++) {
    baseIdx = currentIdx(sample[i], base, baseIdx)
    // ํจ์ ๋๊ณ  ์๋๋ฐ ๋ง์ฝ ๊ฐ์๊ฒ ์์ผ๋ฉด ๋์ด์ ๋น๊ตํ  ๊ฐ์น๊ฐ ์์ผ๋ฏ๋ก ๋ฐ๋ก false
    if(baseIdx === -1) {
      return false;
    }
  }
  return true
};


function currentIdx(sample, base, baseIdx) {
  for(let i = baseIdx; i < base.length; i++) {
    // ๊ฐ์ผ๋ฉด ํด๋น i ๋ฐ๋ก ๋ฆฌํด
    if(sample === base[i]) {
      return i
    // ์ซ์ ์ฐจ์ด๊ฐ ํฌ๊ฒ ๋๋ฉด ๋์ด์ ๋น๊ตํ  ๊ฐ์น๊ฐ ์์ผ๋ฏ๋ก ๋ฐ๋ก -1 ๋ฆฌํด
    } else if (sample < base[i]) {
      return -1
    }
  }
    return -1
}

  ```
 
