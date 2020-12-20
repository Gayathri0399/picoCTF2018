# picoCTF 2018 Writeups

## Contents
**Forensics**
* [Forensics Warmup 1     ](#Forensics-Warmup1-Points-50)
* [Forensics Warmup 2     ](#Forensics-Warmup2-Points-50)

**General Sills**
* [General Warmup 1       ](#General-Warmup1-Points-50)
* [General Warmup 2       ](#General-Warmup2-Points-50)
* [General Warmup 3       ](#General-Warmup3-Points-50)

**Cryptography**
* [Blaise's cipher        ](#Blaises-cipher-Points-200)

---------------------------------------------------------------------------------
## Forensics Warmup1-Points 50

**Challenge**

Can you unzip this file for me and retreive the flag?

**Solution**

When we unzip the downloaded file we will get an image. It is the flag.

**Flag**
```
picoCTF{welcome_to_forensics}
```
--------------------------------------------------------------------------------

## Forensics Warmup2-Points 50

**Challenge**

Hmm for some reason I can't open this PNG? Any ideas?

**Solution**

When we download and open the file we will get an image which is the flag.

**Flag**
```
picoCTF{extensions_are_a_lie}
```
----------------------------------------------------------------------------------

## General Warmup1-Points 50

**Challenge**

If I told you your grade was 0x41 in hexadecimal, what would it be in ASCII?

**Solution**

By using the python command ```chr(int('41',16))``` we will get the answer as 'A'. 
Concept used: hexadecimal to string conversion.

**Flag**
```
picoCTF{A}
```
----------------------------------------------------------------------------------

## General Warmup2-Points 50

**Challenge**

Can you convert the number 27 (base 10) to binary (base 2)?

**Solution**

Since 27 is of base10 it is a decimal number. So here we want to convert a decimal number to binary. I used pen and paper mode to find its answer. 
But it can also be found using the python command ```bin(27)```. We will get the answer as ```11011```.

**Flag**
```
picoCTF{11011}
```
-------------------------------------------------------------------------------------------

## General Warmup3-Points 50

**Challenge**

What is 0x3D (base 16) in decimal (base 10)

**Solution**

Python command can be used to convert the hexadecimal to binary.

```python
>>> int('3D',16)
61
```

**Flag**
```
picoCTF{61}
```
--------------------------------------------------------------------------------------

## Blaise's cipher-Points 200

**Challenge**

My buddy Blaise told me he learned about this cool cipher invented by a guy also named Blaise! Can you figure out what it says? Connect with nc 2018shell.picoctf.com 46966

**Hint**
-There are tools that make this easy.
-This cipher was NOT invented by Pascal

**Solution**

Even though the name of the person who invented this cipher is BLaise this cipher is known as Vigenere Cipher. So here we have to decode Vigenere Cipher to plaintext. When we connect with ```nc 2018shell.picoctf.com 46966``` we will get a large output from which we will be able to find the text ``` pohzCZK{g1gt3w3_n1pn3wd_ax3s7_maj_hof08hk0}``` which is in the format of the flag that we required. So this is the cipher text that we need to decode. But the problem here is that the key is not provided. We know that the format of the flag is picoCTF{}, therefore here pohzCZK corresponds to picoCTF. From this when I tried to find the key by using the Vigenere cipher matrix I got something like "AGFLAGF". It will give picoCTF for pohzCZK but the rest of the text is not decoded correctly. So I assumed that the key is ```flag``` and to get the correct form of the key I added two random characters in front of ```pohzCZK{g1gt3w3_n1pn3wd_ax3s7_maj_hof08hk0}```. It is only after that I was able to find the correct flag.

**Flag**
```
picoCTF{v1gn3r3_c1ph3rs_ar3n7_bad_cdf08bf0}
```
----------------------------------------------------------------------------------------------------------------
