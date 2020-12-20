picoCTF 2018 Writeups

## Contents
1. [Forensics Warmup 1     ](#Forensics-Warmup1-50-points)
2. [Forensics Warmup 2     ](#Forensics-Warmup2-50-points)
3. [General Warmup 1       ](#General-Warmup1-50-points)
4. [General Warmup 2       ](#General-Warmup2-50-points)
5. [General Warmup 3       ](#General-Warmup3-50-points)

---------------------------------------------------------------------------------
## Forensics Warmup1-50 points

**Challenge**

Can you unzip this file for me and retreive the flag?

**Solution**

When we unzip the downloaded file we will get an image. It is the flag.

**Flag**
```
picoCTF{welcome_to_forensics}
```
--------------------------------------------------------------------------------

## Forensics Warmup2-50 points

**Challenge**

Hmm for some reason I can't open this PNG? Any ideas?

**Solution**

When we download and open the file we will get an image which is the flag.

**Flag**
```
picoCTF{extensions_are_a_lie}
```
----------------------------------------------------------------------------------

## General Warmup1-50 points

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

## General Warmup2-50 points

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

## General Warmup3-50 points

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
