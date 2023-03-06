# Ratchet-PHP

##Simple Ratchet PHP WebSocket server

Run the script at `bin/server.php` using `php Ratchet/bin/server.php`

Open a Javascript console or a page with the following Javascript:

```
var conn = new WebSocket('ws://localhost:8080');
conn.onopen = function(e) {
    console.log("Connection established!");
};

conn.onmessage = function(e) {
    console.log(e.data);
};
```

Once you see the console message "Connection established!" you can start sending messages to other connected browsers:

```
conn.send('Hello World!');
```