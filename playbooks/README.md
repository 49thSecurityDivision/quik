## Usage:
1. Writing a new module is as simple as:  
```
mkdir -p module/files && make ln && cd <module>
printf 'this is a file\n' > /tmp/file
printf '#!/bin/sh\necho this is a script\n' > script
```

2. deploying it is as simple as:
```
cd <module>
echo 'SERVERS = user@server1 user@server2 user@server3' > config.mk
make
```

---

## How to parallelize:
```
make -j 3 # tell make to use 3 threads
```
