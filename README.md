# Fastfetch Config + Custom ASCII Logo

This repo contains my customized Fastfetch configuration and a personalized ASCII logo.

You can also get more customization by using the Fastcat theme pack: https://github.com/m3tozz/FastCat

To use these files you'll need fastfetch and the kitty terminal

## Files Included

- `config.jsonc` — My Fastfetch configuration file with custom modules and colors.
- `ascii.txt` — Custom ASCII art displayed as the logo in terminal output.



## How to Use

1. Press the "<> Code" button and download the ZIP file
2. Unzip the file in your download folder

All steps below are performed in the Terminal. You can open it by pressing Ctrl + Alt + T or searching for "Terminal" in the start menu.

3. **Install Kitty Terminal** 

```bash
sudo apt update  
sudo apt install kitty
```

4. **Set Kitty Terminal as default** 

```bash
sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator ~/.local/kitty.app/bin/kitty 50
sudo update-alternatives --config x-terminal-emulator
```
5. **Choose Kitty from the list, and type in the correct number**
    
6. **Close your Terminal and use Ctrl + Alt + T. Check if you're using the Kitty Terminal, and use that Terminal for all the following steps**

7. **Install fastfetch**

```bash
sudo apt update  
sudo apt install fastfetch   
```

8. **Create the Fastfetch config folder** (if it doesn’t exist):

```bash
mkdir -p ~/.config/fastfetch
```

9. **Copy the files into your config directory** 

```bash
cp ~/Downloads/fastfetch-main/config.jsonc ~/.config/fastfetch/config.jsonc
cp ~/Downloads/fastfetch-main/ascii.txt ~/.config/fastfetch/ascii.txt
```

10. **Run Fastfetch** 

```bash
fastfetch
```
## Customization Tips ASCII Art

To replace the logo with your own custom ASCII art:

1. **Open the ASCII logo file in a text editor**

```bash
xed ~/.config/fastfetch/ascii.txt
```

2. **Replace the existing art with your own, then save and close the file**

3. **Run Fastfetch again to see your changes**

```bash
fastfetch
```

## Customization Tips Color

In your config.jsonc, you can set colors using ANSI codes or 24-bit RGB values.  

To open the config.jsonc file:

```bash
xed ~/.config/fastfetch/config.jsonc
```

**Examples of color codes:**

31 = red  
32 = green  
34 = blue  

RGB format: 38;2;&lt;R&gt;;&lt;G&gt;;&lt;B&gt;    
Example: ```38;2;152;255;152 ``` for pastel green  

**To apply the color, change the relevant color key in your config.jsonc, for example:**

```bash
"keyColor": "38;2;152;255;152"  
"keyColor": "32"  
```
**Note on Line Breaks**

You can remove the line breaks ("break") in the config file if you want. I put them there so you can't see my username, and the hostname at the command line.

## Terminal transparency:

Use the following code in kitty and choose a value between 0.0 and 1.0 (I used 0.8 on my pc).

0.0 = fully transparent  
1.0 = fully opaque  

```bash
echo "background_opacity 0.8" >> ~/.config/kitty/kitty.conf && killall -SIGUSR1 kitty
```

## Terminal color:

Use the following code in kitty and use a Hex code for the color you want to use (in the code example the hex code = #28353b, which is a dark-cyan-gray color).

```bash
echo "background #28353b" >> ~/.config/kitty/kitty.conf && killall -SIGUSR1 kitty
```
