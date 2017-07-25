#### 19. Making Filesystem Images

###### Image File Formats
- Proprietary with metadata in separate file 
- Raw with hashes stored in a separate file

###### Creating an Image

```dd``` - convert and copy a file

```
dd if=<subject device> of=<image file> bs=512
```


```dcfldd``` - enhanced version of dd for forensics and security

```
dcfldd if=<subject device> of=<image file> bs=512 hash=<algorithm> hashwindow=<chunk size> hashlog=<hash file>
```

###### Write Blocking
		- Cheap at about $25
		- Slow due to limits of microcontroller that is full-speed (```12 Mbps```) only

- Software write blocking
	- Boot live forensics Linux on subject computer
	- Boot live forensics Linux on forensics workstation