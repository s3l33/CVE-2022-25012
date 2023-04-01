# Argus Surveillance DVR 4.0 - Weak Password Encryption
## CVE-2022-25012
Updated version of this weak password encryption script

Exploit DB REF: https://www.exploit-db.com/exploits/50130

Author REF: https://deathflash1411.github.io/blog/dvr4-hash-crack

NIST REF: https://nvd.nist.gov/vuln/detail/CVE-2022-25012

## Description:
The author had stated that they didnt make additional entries for special ASCII characters. 
I have updated this to include them and provide a password output to make it more user friendly
as well as it accepting arguements rather than needing to edit the script to place the password hash.

## Usage

`python3 CVE-2022-25012.py <hash>`

Example:

`python3 CVE-2022-25012.py E1B0BD8F4D7B73573F7EF539A935735753D190839083C165BD8FCA79418DB398F7DF`



## Generating our own proof of concept

We set a complex password in the argus DVR user screen

![image](https://user-images.githubusercontent.com/60675004/229265535-5a17dbe9-0de1-4800-9605-0b644745f533.png)

Using other avenues to gain access to the following file: `C:\ProgramData\PY_Software\Argus Surveillance DVR\DVRParams.ini`

We can see the entry for our user and corresponding password:

![image](https://user-images.githubusercontent.com/60675004/229265593-23edff63-3d29-48d4-acf9-49193dd73101.png)

We can then run this hash as an arguement (as seen in the usage example)

![image](https://user-images.githubusercontent.com/60675004/229265784-9c33acff-c749-461d-8f0b-4ca9a3130831.png)




