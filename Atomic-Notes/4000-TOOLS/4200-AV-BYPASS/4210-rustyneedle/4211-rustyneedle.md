rustyneedle is a python script used to modify raw shellcode, and provide an executable.

https://codeberg.org/mttaggart/rustyneedle

```
git clone https://codeberg.org/mttaggart/rustyneedle.git
```
There's a few things we have to do. We have to install rust, modify the  src/main.rs file to our options

Specifically, modify the number of base64 iterations, and where the shellcode is downloaded from.

Take note of lines 10 and 12
![[Pasted image 20250529002207.png]]

Now, we need to make our encoded shellcode.
```
# Create raw shellcode, like with C2 Mythic. It will be an output option, .bin extension
cd rustyneedle
cp ~/c2/shellcode.bin .

# Encode the shellcode. note that the output file name is note.txt
python3 encode.py ../shellcode.bin 3 note.txt


```

