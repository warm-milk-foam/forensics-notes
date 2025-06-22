#  Chapter5: Zip archives  #
Usually, people would open zip files in real life by having software such as `WinRAR`. `7zip`, etc.    
However, CTF challenges would use special gimmicks of zip files which normal software won't be able to help much with. I will try to explain to you .  
And as mentioned before, here are some of the tools this chapter will run through:   

- `7z` tool (Can unzip many file formats)
- `unzip` tool (the standard which should always be present)
- `tar` tool (extract from .tar files)
- `unrar` tool (extract from .rar files)
- `zipinfo OR 7z l` (Information about zip encryption. Yes that matters)
- `fcrackzip` (Bruteforce specifically for zip files)
- `john + zip2john` (Bruteforce for many kinds of files)
- `bkcrack` (Plaintext attack for zipped files)
- `hashcat` (Bruteforce password hash when you extract it with `john`)
- `rockyou.txt` (Your standard password dictionary containing just about every common password)   

There are two kinds of attacks you would need to know:  
1) Bruteforce - Guess the password by sending different characters and lengths
2) Dictionary - Send passwords from a dictionary (like `rockyou.txt`) in hopes that the password is commonly used 
   
## 1) Password-encrypted zip files
- Most of the time you zip files in forensics are encrypted with a password
- These zip files are encrypted in different ways, so different cracking software should be used against each one
- Here are some tools to deal with such challenges   
### 1) fcrackzip
- Good for zip files that have weak encryption (Not AES encrypted, which you can tell with `zipinfo`)
- It can be very easily installed with `sudo apt install fcrackzip`
- Command to run it:   
`fcrackzip -v -u -D -p rockyou.txt -z secret.zip` where rockyou.txt is a dictionary
`-v` means verbose, where the attack progress is shown  
`-u` tests the first file, making the attack faster  
`-D -p` means a dictionary attack and supplies a password list  

### 2) john & hashcat
- Work better for AES-encrypted zips than `fcrackzip` by extrracting a hash to break    
- Use `zip2john challenge.zip > zip.hash` to extract the hash  
- `john zip.hash --wordlist=rockyou.txt` to attempt dictionary attack 
- `hashcat -m 13600 zip.hash rockyou.txt` as another alternative  
- `hashcat` can handle many hash varieties and is faster than john