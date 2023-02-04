## NAME
icc - Insert Color Code

## USAGE
`icc COLOR[+COLOR] WORDS...`

## DESCRIPTION
Super simple Bash script that generates color codes for provided text.

You can specify two colors by separating them with "+" - it's useful when you want to provide both
foreground and background colors.

Examples:
```
echo "$(icc red RED TEXT)" # [31mRED TEXT[0m
echo "$(icc bgreen GREEN BACKGROUND)" # [42mGREEN BACKGROUND[0m
echo "$(icc black+byellow BLACK ON YELLOW)" # [30m[43mBLACK ON YELLOW[0m[0m 
echo "$(icc 30+103 BLACK ON YELLOW)" # [30m[103mBLACK ON YELLOW[0m[0m 
```

## OPTIONS
* COLOR - color name or code.
    * Available names: black, red, green, yellow, blue, magenta, cyan, lgray, gray, lred, lgreen, lyellow, lblue, lmagenta, lcyan, white. Prefix "l" stands for "light". Add prefix "b" to color name if you want to set background color instead of foreground.
    * Available codes: https://en.wikipedia.org/wiki/ANSI_escape_code#3-bit_and_4-bit
