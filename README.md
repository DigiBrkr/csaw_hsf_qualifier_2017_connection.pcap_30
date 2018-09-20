# connection.pcap
30 points
> This site is another suspicious site you found in his Herbert's browser history.
>OwnForAll has a dump of some of Herbert's activity, can we use this?
>We've uploaded it here for your convenience.
## Solving it
We are given a *pcap*(packet capture) file that means that we open it in [wireshark](https://www.wireshark.org/).

Looking at the file we can tell it's a file transfer of some sort.
![FileTransfer.pcap](https://github.com/DigiBrkr/csaw_hsf_qualifier_2017_connection.pcap_30/blob/master/screenshot%201.PNG?raw=true)
Since we know [FTP](http://techgenix.com/understanding-ftp-protocol/) uses [tcp](http://searchnetworking.techtarget.com/definition/TCP) as it's [transport layer](https://en.wikipedia.org/wiki/Transport_layer) the first thing to try is one of the simplest things:
`tcp contains flag`
in the wireshark filter bar. This does a search of all tcp packets for the word flag.
And that gives us our flag.
`flag{h3y_u_canT_C_M333lslsls}`

![flag](https://github.com/DigiBrkr/csaw_hsf_qualifier_2017_connection.pcap_30/blob/master/screenshot%202.PNG?raw=true)


