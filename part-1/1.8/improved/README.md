## Exercise 1.8: Image for script
```
ville@RB18:~/repos/devops-with-docker/part-1/1.8$ docker build . -t curler

ville@RB18:~/repos/devops-with-docker/part-1/1.8$ docker run -it curler
Input website:
helsinki.fi
Searching..
<html>
<head><title>301 Moved Permanently</title></head>
<body>
<center><h1>301 Moved Permanently</h1></center>
<hr><center>nginx/1.20.1</center>
</body>
</html>
```