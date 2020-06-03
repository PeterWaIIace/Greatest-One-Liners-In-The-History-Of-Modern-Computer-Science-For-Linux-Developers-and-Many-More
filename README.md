# Greatest-One-Liners-In-The-History-Of-Modern-Computer-Science-For-Linux-Developers-and-Many-More
In my opinion the greates, gluten free, proLGBT, blessed by Linux demigods, Bash oneliners I found or I created.


1. Port scanning:
```
for i in {21..29}; do nc -v -n -z -w 1 192.168.0.$i 443; done 
```
2. Basically this same but with ssh: (you can do this same stuff with nc)
```
for i in {1..255}; do ssh hostname@192.168.0.$i ; done 
```
3. Executing find output in cat:
```
find <find_args> -exec cat {} 
```
4. Adding network privileges to dummy object (ie python in venv):
```
#setcap 'CAP_NET_RAW+eip CAP_NET_ADMIN+eip' /venv/bin/dummy
```
