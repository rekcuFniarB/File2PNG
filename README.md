File2PNG
========

This simple shell utility converts any file into a PNG image. Powered by **ImageMagick**'s `convert` tool, its primary purpose is to bypass file restrictions on platforms that only allow image uploads. Not a steganography tool.

### Usage

Store `input_file` as `output_file.png`:

    file2png -store input_file output_file.png

Print stored file info (size in bytes, original file name and sha256):

    file2png -info container.png

Restore file:
    
    file2png -restore input_file.png output_file

This restores file from `input_file.png` to `output_file`.

    file2png -restore input_file.png

Ommiting output file name will restore to original file name.

Using `-` as filename will use stdin/stdout (not supported when using `-store`).

Example container-image:

![output example](https://i.imgur.com/G6MYiXh.png "output example")

Resulting image file size remains almost the same.

### Install

Copy `file2png` script to any place where you will run it from (`/usr/local/bin` for example).

Requirements:

* `convert` util from Imagemagick
* `grep`
* `sed`
* `bc`
* `awk`
* `sha256sum`
* `dd`
* `mktemp`
