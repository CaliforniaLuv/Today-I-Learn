# TIL π βοΈ

   
 ### 1. node.js
 
  - HTTP νΈλμ­μ ν΄λΆ
    * request, responseλ₯Ό ν΅ν΄ μλ² μΈ‘ κ΅¬μ±
     
     ```javascript
     const http = require('http');

    http.createServer((request, response) => {
    const { headers, method, url } = request;
    let body = [];
    request.on('error', (err) => {
    console.error(err);
    }).on('data', (chunk) => {
    body.push(chunk);
    }).on('end', () => {
    body = Buffer.concat(body).toString();
    // μ¬κΈ°μλΆν° μλ‘μ΄ λΆλΆμλλ€.

    response.on('error', (err) => {
      console.error(err);
    });

    response.statusCode = 200;
    response.setHeader('Content-Type', 'application/json');
    // μ£Όμ: μ λ μ€μ λ€μ ν μ€λ‘ λμ²΄ν  μλ μμ΅λλ€.
    // response.writeHead(200, {'Content-Type': 'application/json'})

    const responseBody = { headers, method, url, body };

    response.write(JSON.stringify(responseBody));
    response.end();
    // μ£Όμ: μ λ μ€μ λ€μ ν μ€λ‘ λμ²΄ν  μλ μμ΅λλ€.
    // response.end(JSON.stringify(responseBody))

    // μλ‘μ΄ λΆλΆμ΄ λλ¬μ΅λλ€.
    });
    }).listen(8080);
    
     ```
     
     * λ§μΌ ν΄λΉ μλ² μΈ‘μ λλ²κΉμ μν  κ²½μ° ```node --inspect``` νμ©νλκ² μΆμ² (ν΄λΌμ΄μΈνΈ μΈ‘μ ν¬μ€νΈλ§¨)
     
     * cors preflightλ λλ²μ μμ²­μ μ§ν ν¨ (1λ²μ OPTIONS λ©μλ, 2λ²μ§Έ λΆν°λ μνλ λ©μλ μμ©)
     

