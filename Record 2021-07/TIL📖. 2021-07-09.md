# TIL π βοΈ
     

 ### 1. Redux
 
  - μ‘μ μμ±ν¨μ (Action Creator)
     * μ‘μ μμ±ν¨μλ, μ‘μμ λ§λλ ν¨μ. λ¨μν νλΌλ―Έν°λ₯Ό λ°μμμ μ‘μ κ°μ²΄ ννλ‘ λ§λ¬
   
   ```javascript
  
    function addTodo(data) {
      return {
        type: "ADD_TODO",
        data
      };
    }
   ```
   
  - λ¦¬λμ (Reducer)
     * λ¦¬λμλ λ³νλ₯Ό μΌμΌν€λ ν¨μ. λ¦¬λμλ λκ°μ§μ νλΌλ―Έν°λ₯Ό λ°μμ΄ (stateμ νμ¬ μνμ λ°μ΄ν° μ’ν©, actionμ μ λ¬λ°μ λ°μ΄ν°)

     ```javascript
    function reducer(state, action) {

    switch (action.type) {
      case ADD_TODO:
      return {
        ...state,
        cartItems: [...state.cartItems, action.payload]
      }
    }
     ```
   
   
  - λμ€ν¨μΉ (dispatch)
  
     * λμ€ν¨μΉλ μ€ν μ΄μ λ΄μ₯ν¨μ μ€ νλμ. μ½κ² μ‘μμ λ°μ μν€λ κ²μ΄λΌκ³  λ³΄λ©΄ μ’μ.
     * dispatch λΌλ ν¨μμλ μ‘μμ νλΌλ―Έν°λ‘ μ λ¬. ex) dispatch(action) 
   


