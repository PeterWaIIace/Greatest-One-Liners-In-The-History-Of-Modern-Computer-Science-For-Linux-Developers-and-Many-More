# Greatest-One-Liners-In-The-History-Of-Modern-Computer-Science-For-Linux-Developers-and-Many-More
In my opinion the greates, gluten free, proLGBT, blessed by Linux demigods, Bash onliners I found or created.


1. Port scanning:

for i in {21..29}; do nc -v -n -z -w 1 192.168.0.$i 443; done 

2. Basically this same but with ssh:

for i in {1..255}; do ssh pi@192.168.0.$i ; done 
