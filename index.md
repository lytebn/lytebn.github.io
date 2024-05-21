




   [Tools](#Tools) | [Commands](#Commands) | [Books](#Books) | [Useful Code](#Useful_code)






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

**Ocr:** `tesseract image.file.jpg text-file-name`

**Open files:** `xdg-open report.pdf`

**Extract strings from image:**  `strings image.png > textfile.txt`

**Compare 2 text files:** `diff file1.txt file2.txt`

**qr reader:** zbar tools `zbarimg image.png`

**Bash for extracting 999 files:** `for i in $(seq 999 -1 0); do tar -xvf "$i.tar"; done`

**Converts many files names from base64** `for file in $(ls); do mv "$file" "$(echo $file | base64 -d)"; done`



> If a file without extension happen to be image after exiftool research the image extension and compare hex code of the header to find the cause of corruption.
> 
>  if no results try [this](https://stylesuxx.github.io/steganography/) on images.




## Books

 1. [CTF Wiki](https://ctf-wiki.mahaloz.re/)
 2. [CTF Playbook](https://fareedfauzi.gitbook.io/ctf-playbook)


## Useful code
**Script that solves binary empty space encoding:**

    import sys
    	    
    input_file = sys.argv[1]    
    output_file = "output.txt"
                  
    with open(input_file, 'r') as infile:
    	with open(output_file, 'w') as outfile:
    		for line in file:
    			replaced_line = line.replace('\t', '1').replace(' ', '0')
    			outfile.write(replaced_line)
    print(f"{output_file}")
