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
5. Copy with tar
```
tar --exclude='.svn' -c -f - /path/to/sourcedir/* | (cd /path/to/destdir ; tar xfp -)
```
6. Check if file changes (when file changes watch stops)
```
watch -d -t -g "ls -lah {filename}" 
```
7. Compile C/C++ during development (watch execute makes)
```
watch "make ; [executable_name]" 
```
8. Pythonic progress bar (Bit cheated though)
```
def progress_bar(finished, total): done = int((finished/total)*100); empty = 100 - done; string = "|"*done+" "*empty; print(f"\rProgress {done}%: [{string}]", end="\r")
```
