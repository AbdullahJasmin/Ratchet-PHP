# Ratchet-PHP
 
## Pre Requisites

You should have `php` installed in your machine

## Using the simple chat application

Run the script at `bin/server.php` using `php Ratchet/bin/server.php`

Open `Main/index.html` in 2 seperate tabs or windows

Type in a comment and press enter or send. 


## Testing it out yourself

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
