# apache-bechmark-test
We can test any site's load time using this tool provided by apache server.

When we deploy web servers we need to ensure that consumers are able to load the site fast without any lag. We can measure the load times using browsers inspection tool. But many times we need to check the load time from command line itself. By checking the load time using command line we can also ensure that browser cache is not included while testing the site. 

### Installing the package
We need to install the package by following command for centOS 7 machines 
```
yum install httpd-tools -y
```

### Command to apply
We can use the below command to test a site 
```
ab -n 100 -c 10 https://www.google.com/
```
In the above command <b><i> -n </i></b> refers to the connection request made and <b><i> -c </i></b> refers to concurrent connection. So we can also define how much load we need to put on the server to test the load time. 

### Results 
The command will show the below output 
```
ab -n 100 -c 10 https://www.google.com/
This is ApacheBench, Version 2.3 <$Revision: 1430300 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking www.google.com (be patient).....done


Server Software:        gws
Server Hostname:        www.google.com
Server Port:            443
SSL/TLS Protocol:       TLSv1.2,ECDHE-RSA-AES128-GCM-SHA256,2048,128

Document Path:          /
Document Length:        18704 bytes

Concurrency Level:      10
Time taken for tests:   2.533 seconds
Complete requests:      100
Failed requests:        98
   (Connect: 0, Receive: 0, Length: 98, Exceptions: 0)
Write errors:           0
Total transferred:      1988091 bytes
HTML transferred:       1869932 bytes
Requests per second:    39.48 [#/sec] (mean)
Time per request:       253.316 [ms] (mean)
Time per request:       25.332 [ms] (mean, across all concurrent requests)
Transfer rate:          766.43 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:       37   57  51.1     44     528
Processing:   106  131  17.8    127     210
Waiting:      104  125  15.8    122     206
Total:        149  188  55.2    174     658

Percentage of the requests served within a certain time (ms)
  50%    174
  66%    184
  75%    194
  80%    197
  90%    243
  95%    253
  98%    272
  99%    658
 100%    658 (longest request)
```
