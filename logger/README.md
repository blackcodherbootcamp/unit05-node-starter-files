# Writing and Logging

In this task, we'll set up a basic server using Express and implement a logging module to track server requests.

1. **Install Dependencies**: Run `npm install` in the terminal to install Express.
2. **Review Server File**: Examine the file `src/server.js`.
3. **Start Server**: Use the command `node src/server.js` to start the server.
4. **Testing**: To test, open Postman and visit `http://localhost:8080`. Try different paths for various responses.

   ```js
   const express = require("express");
   const app = express();

   app.get("/", (req, res) => {
     res.send("Morning");
   });

   app.patch("/greet", (req, res) => {
     res.send("Good Evening");
   });

   app.post("/bye", (req, res) => {
     res.send("Good Night");
   });

   app.listen(8080, function () {});
   ```

5. **Logging Module**: Create a module to log all server requests in a file named `log.txt`.
6. **Log Details**: Each log entry in `log.txt` should include:

   - Date and time of the request.
   - Request method (e.g., `GET`, `PATCH`, `POST`).
   - The response sent back to the client.

   ```txt
   2021/11/25 09:38:20 - GET "Morning"
   2021/11/25 09:38:22 - POST "Good Evening"
   2021/11/25 09:38:23 - PATCH "Good Night"
   ```
