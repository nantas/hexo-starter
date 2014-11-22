title: About
date: 2014-11-22 14:51:51
layout: page
permalink: /aboutus
---

This is the main body text. Here is where we write the major content of the page. Try to keep it concise and relevant. This is what the user will most likely read directly after looking at the title, so it should immediately hook their interest and keep them involved until the end. This is crappy filler text but serves mostly as an example of what you could do with stored bits of filler text. No more having to copy paste from a text file or generator. Immediately have what you need, a mere hotkey away!

<img src='//placehold.it/600x400/013e89/FFFFFF.png'/>

``` javascript TimeServer http://nantas.github.io/starter code-on-github
var net = require('net');
function zeroFill(i) {
    return (i < 10 ? '0' : '') + i;
}

var server = net.createServer( function(socket) {
    //
    var date = new Date();
    var result = date.getFullYear() + "-"
    + zeroFill(date.getMonth() + 1) + "-"
    + zeroFill(date.getDate()) + " "
    + zeroFill(date.getHours()) + ":"
    + zeroFill(date.getMinutes()) + '\n';
    socket.end(result);
    });

server.listen(process.argv[2]);
```
