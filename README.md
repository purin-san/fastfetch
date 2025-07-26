# Fastfetch Config + Custom ASCII Logo

This repo contains my customized Fastfetch configuration and a personalized ASCII logo.

You can also get more customization by using the Fastcat theme pack: https://github.com/m3tozz/FastCat

To use these files you'll need fastfetch and the kitty terminal

## Files Included

- `config.jsonc` — My Fastfetch configuration file with custom modules and colors.
- `ascii.txt` — Custom ASCII art displayed as the logo in terminal output.



## How to Use

All steps below are performed in the Terminal. You can open it by pressing Ctrl + Alt + T or searching for "Terminal" in the start menu.

1. **Install Kitty Terminal** 

'''sudo apt update'''
sudo apt install kitty

2. **Set Kitty Terminal as default** 

sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator ~/.local/kitty.app/bin/kitty 50
sudo update-alternatives --config x-terminal-emulator

> choose Kitty from the list, and type in the correct number

3. **Install fastfetch**

sudo apt update  
sudo apt install fastfetch   

4. **Create the Fastfetch config folder** (if it doesn’t exist):

mkdir -p ~/.config/fastfetch


5. **Copy the files into your config directory** 

cp config.jsonc ~/.config/fastfetch/config.jsonc  
cp ascii.txt ~/.config/fastfetch/logo.txt


6. **Run Fastfetch** 

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

## Terminal transparency:

Use the following code in kitty and choose a value between 0.0 and 1.0 (I used 0.8 on my pc).

0.0 = fully transparent  
1.0 = fully opaque  

echo "background_opacity 0.8" >> ~/.config/kitty/kitty.conf && killall -SIGUSR1 kitty

## Terminal color:

Use the following code in kitty and use a Hex code for the color you want to use (in the code example the hex code = #28353b, which is a dark-cyan-gray color).

echo "background #28353b" >> ~/.config/kitty/kitty.conf && killall -SIGUSR1 kitty


**Note on Line Breaks**

You can remove the line breaks ("break") in the config file if you want. I put them there so you can't see my username, and the hostname at the command line.


echo "background_opacity 0.7" >> ~/.config/kitty/kitty.conf && killall -SIGUSR1 kitty

