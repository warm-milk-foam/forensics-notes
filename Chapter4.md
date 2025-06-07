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

We will go through these tools later in `steganography` chapter 

## 2. Zip archives
- If you do not not know how to extract these, you can try the folllowing:
1) Most zip files
- `7z` tool (Can unzip many file formats)
- `unzip` tool (the standard which should always be present)
- `tar` tool (extract from .tar files)
- `unrar` tool (extract from .rar files)
2) Sometimes said zip files will be protected with a password and guess what you don't know them   
(You would be in for a bad time)
- `zipinfo OR 7z l` (Information about zip encryption. Yes that matters)
- `fcrackzip` (Bruteforce specifically for zip files)
- `john + zip2john` (Bruteforce for many kinds of files)
- `bkcrack` (Plaintext attack for zipped files)
- `hashcat` (Bruteforce password hash when you extract it with `john`)
- `rockyou.txt` (Your standard password dictionary containing just about every common password)   
Usually, if you had to bruteforce, the flag would be obtainable quite quickly (Maybe 2hrs at most? Depending on challenge)

## 3. Memory Dumps 
- You can easily tell these from the chunky size of the file (Maybe like 500mb - 2 gb)
- Volatility 2
- Volatility 3
- I will teach you how to install later

## 4. pcap files 
- Its automatic - We have to analyse internet traffic
- The tool for this is Wireshrk

## 5. Video and Audio Analysis
- This one sucks boooooo
1) Audio analysis
- Audacity/Sonic visualiser
- Deep Sound (I haven't used this yet)
2) Video analysis
- ffprobe
- mediainfo  

Exiftool and binwalk will still be quite important here
## 6. Disk imagery ##
- You can easily tell this from the `.img` extension
- FTK Imager (For quick look)
- Autopsy (For deep analysis)

## 7 .sal files
- You are probably looking at a capure file from Saleae Logic analyser
- Use [Logic](https://www.google.com/search?q=logic%202.4.29&client=firefox-b-d&sclient=gws-wiz-serp)

I have given only the common ones that people (or me in this case) would use during CTFs.  
For more tools, you can look here:   
https://github.com/cugu/awesome-forensics?tab=readme-ov-file    
https://wiki.bi0s.in/steganography/roadmap/  