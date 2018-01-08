File2PNG
========

This is a shell script that stores any file as PNG image. It's based on `convert` util from **Imagemagick**.

### Usage

Store `input_file` as `output_file.png`:

    file2png -store input_file output_file.png

Print stored file info (size in bytes, original file name and sha256):

    file2png -info container.png

Restore file:
    
    file2png -restore input_file.png output_file

This restores file from `input_file.png` to `output_file`.

    file2png -restore `input_file.png`

Ommiting output file name will restore to original file name.
    
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
