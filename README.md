goal: create a extremely short program that you can eyeball and tell
it's not malicious. This program will monitor your lightning node, and
if any invoices are paid, it will send a telegram message to you.

The node needs to be on the local network: ie, 192.168.1.XXX I will be
making REST API URL calls to get the data. Program runs once a min and
sleeps otherwise.

this is just for fun, and no guarantees are made.

git clone https://github.com/bimmerr2019/lnd_watcher.git

cd lnd_watcher

make cmdlinesocket

./cmdlinesocket api.coindesk.com 80 GET "/v1/bpi/currentprice.json" "" "Connection: close" "Content-Type: text/html" "Host: api.coindesk.com"

MIT license
