# Chapter8: Audio file analysis #  
Sometimes, files can also be hidden in audio files  
This means that there are two methods the flags can be hidden:  
1) Files/Data can be extracted and read with `exiftool`, `binwalk`  
2) The flag is hidden making use of the audio file medium  

If its 2, usually it would be a tool called `Audacity` and walk through a few challenges showcasing some properties of the tool    

## Spectrogram and waveform ##  

For our first challenge, let us analyse this file called `chall.wav`, which I uploaded to a directory called "Challenge files"   

![alt text](../images/image-19.png)  
Here, I opened up `chall.wav` in Audacity, showing us a waveform version of the audio that is stored  
A waveform version refers to the time-domain representation of the sound played, where the y-axis refers to amplitude and the x-axis to the corresponding time  
However, there is nothing of note here, so we would have to change to spectrogram view by clicking the three dots and selecting, `Spectrogram view`    

![alt text](../images/image-20.png)  

And here, we find something interesting:   
![alt text](../images/image-21.png)  
And by zooming in, we can see the flag:  
![alt text](../images/image-22.png)

Sometimes, the flag can be hidden through the waveform representation as well, through rhythmic pauses (binary encoding, morse code, etc), but ultimately depends on the context to find anomalies in how the file is presented to you  

## Mixing the files together ##  

Sometimes, flags can only be revealed by mixing the files together in audacity

https://sumit-arora.medium.com/audio-steganography-the-art-of-hiding-secrets-within-earshot-part-2-of-2-c76b1be719b3
