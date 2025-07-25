# Fastfetch Config + Custom ASCII Logo

This repo contains my customized Fastfetch configuration and a personalized ASCII logo.

You can also get more customization by using the Fastcat theme pack: https://github.com/m3tozz/FastCat

To use these files you'll need fastfetch.

## Files Included

- `config.jsonc` — My Fastfetch configuration file with custom modules and colors.
- `ascii.txt` — Custom ASCII art displayed as the logo in terminal output.



## How to Use

All steps below are performed in the Terminal. You can open it by pressing Ctrl + Alt + T or searching for "Terminal" in the start menu.

1. **Install fastfetch If you havent**

sudo apt update  
sudo apt install fastfetch   

3. **Create the Fastfetch config folder** (if it doesn’t exist):

mkdir -p ~/.config/fastfetch


2. **Copy the files into your config directory** 

cp config.jsonc ~/.config/fastfetch/config.jsonc  
cp ascii.txt ~/.config/fastfetch/logo.txt


3. **Run Fastfetch** 

fastfetch

## Customization Tips ASCII Art

To replace the logo with your own custom ASCII art:

1. **Open the ASCII logo file in a text editor**

xed ~/.config/fastfetch/ascii.txt

2. **Replace the existing art with your own, then save and close the file**

3. **Run Fastfetch again to see your changes**

fastfetch

## Customization Tips Color

In your config.jsonc, you can set colors using ANSI codes or 24-bit RGB values.

**Examples of color codes:**

31 = red  
32 = green  
34 = blue  

RGB format: 38;2;&lt;R&gt;;&lt;G&gt;;&lt;B&gt;    
Example: 38;2;152;255;152 for pastel green  

**To apply the color, change the relevant color key in your config.jsonc, for example:**

"keyColor": "38;2;152;255;152"  
"keyColor": "32"  

**Note on Line Breaks**

You can remove the line breaks ("break") in the config file if you want. I put them there so you can't see my username, and the hostname at the command line.

