#  Chapter5: Volatility   #
The files are very big because they are memory dumps  
Memory dumps are basically all the information in the RAM of a system at a current point of time    
This is useful when a system crashes, because it tells you what could have went wrong   
In CTFs, the flag would be hidden in one of the processes occurring  

## How do I install?
-To install `Volatility 2` follow these steps:  
```
git clone https://github.com/volatilityfoundation/volatility.git

cd volatility

python2 setup.py install
```
You may see something like this:  

![alt text](image-8.png)  
To fix this, you  can run

- Which I took from https://mahim-firoj.medium.com/how-to-install-volatility-2-and-how-to-use-it-8d7335e2c26c
- Alternatively, you could also use the executable version, which bypasses the need for you to invoke `python2` for use
```
sudo python2 get-pip.py (Install pip2)
sudo apt install python2-dev  (So that the next function can run)
pip2 install pycryptodome distorm3    

Note: this may not be something you encounter. Just putting it here because it happened to me. 
```


-To install `Volatility 3` follow these steps:
```
git clone https://github.com/volatilityfoundation/volatility3.git

cd volatility3/

pip3 install -r requirements.txt

Also, its good practice to download the volatility 3 symbols if they do not show up  

volatility3/volatility3/symbols/  
git clone https://github.com/volatilityfoundation/volatility3-symbols.git  

```  
You may be asking, why do I have to install 2 volatility versions?   
`Volatility 2` - Has large plugin support for older systems  
`Volatility 3` - Modern and has ongoing development for it  
Personally, I like to use volatility 2 for CTF challenges more   

## How do I use? 
