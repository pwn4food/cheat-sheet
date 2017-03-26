# Commandline cheat-sheet

### Search recursively for a string inside files and directories 
```
grep -R 'string' dir/
```

### Download entire website w/ wget
```
wget --limit-rate=200k --no-clobber --convert-links --random-wait -r -p -E -e robots=off -U mozilla http://www.asdasdsaqd.com
```

### Custom convert any video format to GIF
```
ffmpeg -i video.mp4 -vf scale=400:-1 -r 3 -f image2pipe -vcodec ppm - | convert -delay 5 -loop 0 - video.gif | convert -layers Optimize - video.gif
```

### Connect via SSH and send commands to Server (commands in bash file)
```
ssh user@server -p 22 'bash -s' < cmd.sh
```

### See all strings in any file
```
strings FILE
```

### Search for STRING in all strings of a file
```
strings FILE |gre STRING
```

### Convert string to md5
```
import hashlib
hashlib.md5("meuovo".encode("utf")).hexdigest()
```

### Convert hex to ascii
```
echo 0x00000000746F6F72 | xxd -rp
```

### Convert string to hex 
```
printf intrd | xxd
```

### Convert hex to decimal
```
echo $((0x3c))
```

### Convert decimal to char
```
printf "\101\n"
python hex to dec
python -c "print(int('0x00000000746F6F72', 16))"
```

### Convert hex to ascii
```
python -c print '"deadbeef".decode("hex")''
```

### Convert dec to hex
```
python -c "print hex(int(65537))"
```

### Encode base64
```
python -c 'import base64; print(base64.b64encode("dssss"))'
```

### Decode base64
```
python -c 'import base64; print(base64.b64decode("dsfdsfsdfd="))'
python -c 'import base64; print(base64.b64decode("SEFDS0FGTEFHe09ubHkgU24wd2QzbiBjYW4gZGl2aWRlIGJ5IFplcjB9Cg=="))'
```

### Simple sed search n replace
```
sed -i 's/foo/bar/g' FILENAME
sed -i 's/(//g' abc_patched.txt
```

### Print only numbers
```
sed "s/[^0-9]//g" ARQUIVO
```

### Remove spaces
```
sed '/^\s*$/d' ARQUIVO
```

### Tabela simples de comparação Hexa, Decimal, Octal e Binário


|Hex  |Dec  |Oct  |Bin  |
|-----|-----|-----|-----|
|    0|    0|    0| 0000|
|    1|    1|    1| 0001|
|    2|    2|    2| 0010|
|    3|    3|    3| 0011|
|    4|    4|    4| 0400|
|    5|    5|    5| 0101|
|    6|    6|    6| 0110|
|    7|    7|    7| 0111|
|    8|    8|   10| 1000|
|    9|    9|   11| 1001|
|    A|   10|   12| 1010|
|    B|   11|   13| 1011|
|    C|   12|   14| 1100|
|    D|   13|   15| 1101|
|    E|   14|   16| 1110|
|    F|   15|   17| 1111|
