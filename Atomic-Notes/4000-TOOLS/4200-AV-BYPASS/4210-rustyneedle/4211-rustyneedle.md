rustyneedle is a python script used to modify raw shellcode, and provide an executable.

https://codeberg.org/mttaggart/rustyneedle

There's a few things we have to do. We have to install rust, modify the  src/main.rs file to our options

Specifically, modify the number of base64 iterations, and where the shellcode is downloaded from.

Take note of lines 10 and 12
![[Pasted image 20250529002207.png]]


```
# Create raw shellcode, like with C2 Mythic. It will be an output option, .bin extension
git clone https://codeberg.org/mttaggart/rustyneedle.git
cd rustyneedle
cp ~/c2/shellcode.bin .


```

Now, we need to make our enco