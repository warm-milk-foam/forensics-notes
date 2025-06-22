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

## 1) Password-encrypted zip files
- Most of the time you zip files in forensics are encrypted with a password
- These zip files are encrypted in different ways, so different cracking software should be used against each one