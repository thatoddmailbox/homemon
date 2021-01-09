# homemon
## Components
There are three different components:
* [homemon-daemon](https://github.com/thatoddmailbox/homemon-daemon) - The program that runs on a device and regularly sends reports to a server.
* [homemon-server](https://github.com/thatoddmailbox/homemon-server) - Receives reports over HTTP, logs them, and provides a web UI to view the most recent data.
* [homemon-receiver](https://github.com/thatoddmailbox/homemon-receiver) - (optional) Receives reports over an efficient UDP-based protocol. Only needed if you want to use the UDP transport.

## Transports
There are two methods of sending reports:
* HTTP - makes a POST request to [homemon-server](https://github.com/thatoddmailbox/homemon-server). Simple to set up and maintain.
* UDP - fires a UDP packet with report data to [homemon-receiver](https://github.com/thatoddmailbox/homemon-receiver). More complex setup, but uses significantly less data. (estimated to be around 90 bytes per report, as counted by T-Mobile)