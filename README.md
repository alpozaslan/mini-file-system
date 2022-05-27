# Mini File System
## A COMP 304 Project by Alp Özaslan and Onur Eren Arpacı

In this project we implemented a file system API library which operates on virtual disks. The file system is based on File Allocation Table (FAT), and it does not support directories, i.e., all files are stored flat in the virtual disk. The virtual disk itself is actually a binary file.

First we implemented disk manipulation functions: 
* **mini_fat_create(filename, block size, block count)** to create new filesystem
* **mini_fat_save(fs)** to save the filesystem to real file on the disk. It saves only the metadata of the filesystem.
* **mini_fat_load(filename)** to load the fs that is previously saved.

Then we implemented file system manipulation functions:
* **mini_file_open(fs, filename, is write)** to open the file
* **mini_file_close(fs, open file)** to close the file
* **mini_file_delete(fs, filename)** to delete the file
* **mini_file_seek(fs, open file, offset, from start)** to change the position of the cursor in an opened file.
* **mini_file_write(fs, open file, size, buffer)** to write buffer to the file
* **mini_file_read(fs, open file, size, buffer)** to read the file to the buffer

We use C file functions like fopen, fseek, fread etc. to manipulate the file.
## All parts of the code are working well.
