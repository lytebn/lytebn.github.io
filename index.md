



   [Tools](#Tools) | [Commands](#Commands) | [Books](#Books)






# Tools

## [stenography tools](https://github.com/DominicBreuker/stego-toolkit/blob/master/README.md#tools)
## [general CTF tools](https://github.com/zardus/ctf-tools/tree/master)




# Commands
## [list of most used commands](https://dvd848.github.io/CTFs/CheatSheet.html)

**exiftool :** usage `exiftool image.jpg` | | shows details of image

**strings :** usage `strings image.jpg` | shows strings in image

**steghide :** usage `steghide --extract -sf image.jpg` | shows stegno in image

**binwalk :** usage `binwalk -e image.jpg` | shows files in image | `binwalk --dd='.*' [filename]`

**file :** usage `file image.jpg` | shows info and type of file

**grep:** find in strings or anything (first command `| grep “string"` 

**zsteg:** usage `(zsteg -a image.png)` + `| grep -i “flag”)`

**stegsolve:** GUI tool to find things in images

> If a file without extension happen to be image after exiftool research the image extension and compare hex code of the header to find the cause of corruption.
> 
>  if no results try [this](https://stylesuxx.github.io/steganography/) on images.




## Books

 1. [CTF Wiki](https://ctf-wiki.mahaloz.re/)
 2. [CTF Playbook](https://fareedfauzi.gitbook.io/ctf-playbook)

