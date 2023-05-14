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
<hr>
Answer:

The Console.Read() method reads the next character from the standard input stream and returns its ASCII value. In this case, the input "hello" is read character by character.

Console.WriteLine(Console.Read()) reads the first character 'h' and writes its ASCII value, which is 104, to the console.

Console.ReadKey() waits for a key press before continuing.

Console.WriteLine(Console.ReadLine()) reads the remaining characters of the input ("ello") as a single line and writes it to the console.

Therefore, the output of the code will be:

3. 
    104<br>
    llo

<hr>
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

<hr>

Answer:
