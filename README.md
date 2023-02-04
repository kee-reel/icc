NAME: icc - Insert Color Code

USAGE: `icc [CODE | COLOR_NAME]`

DESCRIPTION: Super simple Bash script that generates color codes.
If no option is provided, then reset code "\e[0m" is inserted, marking end of colorized text sequence.
Examples:
```
  echo "$(icc red)RED TEXT$(icc)" # [31mRED TEXT[0m
  echo "$(icc bgreen)GREEN BACKGROUND$(icc)" # [42mGREEN BACKGROUND[0m
  echo "$(icc black)$(icc byellow)BLACK ON YELLOW$(icc)$(icc)" # [30m[43mBLACK ON YELLOW[0m[0m 
```

OPTIONS:
* `CODE` - ANSI escape color code ([wiki](https://en.wikipedia.org/wiki/ANSI_escape_code#3-bit_and_4-bit))
* `COLOR_NAME` - name of color. Available names: black, red, green, yellow, blue, magenta, cyan, lgray, gray, lred, lgreen, lyellow, lblue, lmagenta, lcyan, white. Prefix "l" stands for "light". Add prefix "b" to color name if you want to get background color instead of foreground.
