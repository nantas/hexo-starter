title: kitchensink
date: 2014-11-22 15:04:16
permalink: /kitchensink
---

{% blockquote nantas, prose starter http://nantas.github.io/starter %}
Don't eat bacon.
{% endblockquote %}

{% codeblock lang:js %}
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
{% endcodeblock %}
