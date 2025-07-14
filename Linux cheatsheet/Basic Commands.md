mktemp -d : The command creates a **new, unique, temporary directory** with a random name.

cp ~/<filename> .   : Copies `filename` from your home directory (`~`) to the current directory (`.`).

xxd -r <oldfile.txt> <oldfile.bin> :Converts the **hexdump** (oldfile.txt) back into binary format using `xxd`. `-r` means reverse the hexdump. Output is saved to `oldfile.bin.
 
file <filename> : determines the **type of content** in the file (e.g., gzip, bzip2, tar, ASCII text). Very useful to know how to extract it.

gunzip file.gz : Decompresses a `.gz` (gzip) file.
bzip2 -d <file.bz2> : Decompresses a `.bz2` (bzip2) file. `-d` stands for **decompress**.
tar -xf <file.tar> Extracts files from a `.tar` archive. `-x` = extract, `-f` = specify file.





