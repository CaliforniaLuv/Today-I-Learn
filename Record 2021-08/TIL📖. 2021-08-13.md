# TIL ð âï¸

   
 ### 1. ìê³ ë¦¬ì¦
 
  - ì¤í¨ì¨

    
  ```js
  function solution(N, stages) {
    
    let record = []
    let fail = []
    let person = []
    let total = []
    let challenger = stages.length
    
    
    
    // step.1 ê° ì¤íì´ì§ ë¹ ì¤í¨ì íì   
    // ê²°ê³¼: ê° ë¼ì´ë ì¤í¨ì [1, 3, 2, 1, 0] 
    // ê²°ê³¼: ê° ë¼ì´ë ì´ìë¨ì ëì ì [8, 7, 4, 2, 1]
    for(let i = 1; i <= N; i++) {
        let count = 0
        for(let j = 0; j < stages.length; j++) {
            if(i == stages[j]) {
                count++
     
            }  
        }
        fail.push(count)
        person.push(challenger)
        challenger = challenger - count
    } 

    
    
    // step.2 ì¤í¨ì¨ ì¢í©
    // ê²°ê³¼: ê° ë¼ì´ë ì¤í¨ì [1, 3, 2, 1, 0] 
    // ê²°ê³¼: ê° ë¼ì´ë ì´ìë¨ì ëì ì [8, 7, 4, 2, 1]
    
     for(let i = 0; i < N; i++) { 
        total.push({type : i + 1})
        total[i]["value"] = fail[i] / person[i]
    }
    
    
    
    // step.3 ì¤í¨ì¨ ìµì¢ ìì ì¢í©  
    // ê° ì¤íì´ì§ ì¤í¨ì¨ ìµì¢ ìì(ëì íë¥ ë¶í° ë®ì íë¥ ê¹ì§)   
    let result = []
    let valueSort = total.sort((x, y) => y.value - x.value  )
   
    valueSort.map((el, idx) => {
        result.push(valueSort[idx]["type"])
    })
        
 
    return result;
}

   
  ```
  
   ### 2. Redux
   
   -  Reduxë ì»´í¬ëí¸ì ìíë¥¼ ë¶ë¦¬íë í¨í´
   -  Redux ììëì ë°ë¥¸ ì½ë êµ¬í ì ë¦¬
  
