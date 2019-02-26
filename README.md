# distroverify data

Data for Distroverify

# Maintainers
I am looking for maintainers to maintain certain distros, simply edit the MAINTAINERS file and do a Pull Request, same goes for updates to a certain distribution.

# How to add a distribution ?
Simply create a folder for the distributon, version, edition and architecture.<br>
After that you put the checksums and signatures in it.<br>
Then you create a file called `DATA.json` it has this syntax:
```
{
    "version": "18.0.3", //The version
    "hash": "SHA1", //The hash method
    "gpg": true, // If a GPG signature is availbile
    "sigfileiso": "manjaro-kde-18.0.3-stable-x86_64.iso.sig", // Set it too false if the CHECKSUM file is signed and not the ISO
    "key": "0x11C7F07E", // The keys
    "keyserver": "hkp://pool.sks-keyservers.net" // The keyserver from where to fetch the keys
}
```
Notice: A signed file with the checksums must have the name of the hashing method plus .gpg<br>
For example:<br>
SHA256SUMS - Hashing file<br>
SHA256SUMS.gpg - The signed file<br>
<br>
Valid filenames are for example:<br>
MD5SUMS, SHA1SUMS, SHA256SUMS, SHA512SUMS, etc
