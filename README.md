1. Consider the following code snippet:

```csharp
using System;

namespace Solution
{
    class Solution
    {
        static void Main(string[] args)
        {
            Console.WriteLine(Console.Read());
            Console.ReadKey();
            Console.WriteLine(Console.ReadLine());
        }
    }
}
```

There is a single line input provide in the console, hello. The output of the code is: 

Pick ONE option

<ol>
    <li>
        h<br>
        ello
    </li>
    <li>
        104<br>
        ello
    </li>
    <li>
        104<br>
        llo
    </li>
    <li>
        Compilation Error<br>
    </li>
</ol>

Answer:

The Console.Read() method reads the next character from the standard input stream and returns its ASCII value. In this case, the input "hello" is read character by character.

Console.WriteLine(Console.Read()) reads the first character 'h' and writes its ASCII value, which is 104, to the console.

Console.ReadKey() waits for a key press before continuing.

Console.WriteLine(Console.ReadLine()) reads the remaining characters of the input ("ello") as a single line and writes it to the console.

Therefore, the output of the code will be:

<ul>
    <li>
        104<br>
        llo
    </li>
</ul>

<hr>

2. What happens when a client sends a GET request to http://localhost:3000/users?

```javascript
const http = require("http");

http.createServer((request, response) => {
    if (request.method === "GET" && request.url === "/users") {
      response.writeHead(200, { "Content-Type": "application/json" });
      response.end([
        { name: "Alice", age: 25 },
        { name: "Bob", age: 30 },
      ]);
    } else {
      response.writeHead(404, { "Content-Type": "text/plain" });
      response.end("Not found");
    }
  })
  .listen(3000);

console.log("Server is running on port 3000");
```

Pick ONE option

<ol>
  <li>The server responds with a JSON array that contains user data.</li>
  <li>The server responds with a plain text message that contains the request data.</li>
  <li>The server responds with an error.</li>
  <li>The server sends an empty response.</li>
</ol>

Answer:

When a client sends a GET request to http://localhost:3000/users, the server code checks if the request method is GET and the URL is "/users". In this case, both conditions are satisfied, so the server responds with a status code of 200 (OK) and sets the "Content-Type" header to "application/json" to indicate that the response will be in JSON format.

The server then sends a JSON array containing user data as the response body:

```javascript
[
  { name: "Alice", age: 25 },
  { name: "Bob", age: 30 }
]
```

Therefore,

<ul>
    <li>
        The server responds with a JSON array that contains user data.
    </li>
</ul>

<hr>

3. Given an array, which of the following commands opens the file "demo.txt" (or creates it if the file does not exist) and writes the contents of the array to the file?  

```javascript
const arr = ["apple", "mango", "banana"];
```

Pick ONE option

<ol>
  <li>fs.writeFileSync("demo.txt", arr);</li>
  <li>fs.writeFileSync("demo.txt", JSON.stringify(arr));</li>
  <li>fs.writeFile("demo.txt", arr, (err) => {console.log(err);});</li>
  <li>fs.write("demo.txt", JSON.stringify(arr));</li>
</ol>

Answer:

fs.writeFileSync("demo.txt", JSON.stringify(arr)); - This command converts the array to a JSON string representation using JSON.stringify(). It then writes the JSON string to the file "demo.txt". This is the correct option as it writes the contents of the array to the file.

Therefore, 

```javascript
fs.writeFileSync("demo.txt", JSON.stringify(arr));
```

<hr>

4. Select the expression(s) that cause a MySQL error.

Pick ONE OR MORE options

<ol>
  <li>SELECT customer_id, COUNT( * ) FROM transactions GROUP BY customer_id HAVING COUNT( * ) > 10</li>
  <li>SELECT customer_id, COUNT( * ) AS transactions FROM transactions GROUP BY customer_id HAVING transactions > 10</li>
  <li>SELECT customer_id, COUNT( * ) AS transactions FROM transactions WHERE transactions > 10 GROUP BY customer_id</li>
  <li>SELECT customer_id, COUNT( * ) AS transactions FROM transactions GROUP BY 1 HAVING transactions > 10</li>
</ol>

Answer:

The column alias "transactions" is referenced in the HAVING clause as HAVING transactions > 10. This will result in a MySQL error because the column alias cannot be directly used in the HAVING clause.

Therefore,

```sql
SELECT customer_id, COUNT( * ) FROM transactions GROUP BY customer_id HAVING COUNT( * ) > 10
```