### Running the container

```shell
docker run -d -it ubuntu sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
```

### Installing deps

```shell
% docker exec -it 59b1b187e30e bash
root@59b1b187e30e:/# apt update
root@59b1b187e30e:/# apt install curl
```

### Testing input

```shell
% docker attach 59b1b187e30e       
hello
Searching..
curl: (6) Could not resolve host: hello
Input website:
helsinki.fi
Searching..
<html>
<head><title>301 Moved Permanently</title></head>
<body>
<center><h1>301 Moved Permanently</h1></center>
<hr><center>nginx/1.22.1</center>
</body>
</html>
Input website:
```
