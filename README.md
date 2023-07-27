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
