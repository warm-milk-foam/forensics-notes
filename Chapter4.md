#  Chapter4: File formats - What challenge is this? What tools should I use?? #
Sometimes, you will receive files that are strange to you (I mean for the everyday person)  
So this chapter serves as a guide for what tools to use for different file formats you may encounter.  
(Or if you are in a hurry in an actual CTF as a noob, look at this to figure out how to crack the challenge)  

## 1. Images ##
1) Online tools that will help you:
- [Aperisolve](https://www.aperisolve.com/) aka the all in one lazy tool
- [Cyberchef](https://gchq.github.io/CyberChef/) contains many tools that can help to extract for forensics (and also some crypto for decrypting, if you come upon a encoded flag)
- [Fotoforensics](https://fotoforensics.com/) I guess if you want more...
- [Photopea](https://www.photopea.com/) A free online tool to edit photos, would come in handy when you need to change an image (like QR codes)
- [Forensically](https://29a.ch/photo-forensics/#forensic-magnifier) - Analyse images from the surface level
- [StegOnline](https://georgeom.net/StegOnline/upload) for steganography (which we will cover later)
2) CLI tools:
- Exiftool, Binwalk, strings, file and cat (The basics)
- Pngcheck (Check PNGs for corruption)
- stegsolve (Analyse images in different planes)
- steghide (Hide and extract secret data)
- stegdetect (Detect secret data)
- dd (Carving tool like binwalk)

## 2. Zip archives
- If you do not not know how to extract these, you can try the folllowing:
1) Most zip files
- `7z` tool (Can unzip many file formats)
- `unzip` tool (the standard which should always be present)
- `tar` tool (extract from .tar files)
- `unrar` tool (extract from .rar files)
2) Sometimes said zip files will be protected with a password and guess what you don't know them
- `fcrackzip` (Bruteforce specifically for zip files)
- `john` (Bruteforce for many kinds of files)

I have given only the common ones that people (or me in this case) would use during CTFs.  
For more tools, you can look here: https://github.com/cugu/awesome-forensics?tab=readme-ov-file