# ACGA Codelike

![image](https://github.com/Allegheny-Code-Colf-Association/acga-codelike/assets/1552764/ef99bbe4-f376-47fb-b52f-87dc8ccde055)

A fork of the 2D, array-based [codelike language](https://github.com/dospunk/codelike) with added commands to expand the range of the language to complete
code golf challenges.

## Using this repository

This repository uses the [Apache Maven](https://maven.apache.org/) build system. The `pom.xml` file in the root directory of the repository points
to the `src/test/resources/main.txt` file as its starting point.

## Notes

- When reading a source file, the interpreter will always start at the top left corner and will be going down.
- `Y` coordinates increase going down, `X` coordinates increase going left
- Please note that tabs only count as one character; make sure to use spaces
- If you get a `j` error first thing when running but your file does not start with a j, it means that the file could not be found
- turn on debugging mode by changing the [`debugging` boolean at the beginning of the Main.java file](https://github.com/Allegheny-Code-Colf-Association/acga-codelike/blob/master/src/main/java/com/interpreter/acga-codelike/Main.java#L16) to true

## Commands

|Command |Functionality |
|:-------|:-------------|
|`-`     |Continue horizontally |
|`\|`     |Continue vertically   |
|`\`     |Continue up-left or down-right |
|`/`     |Continue down-left or up-right |
|`+`     |Increment top value on the stack and continue |
|`_`     |Decrement top value on the stack and continue |
|`>`    |If moving to the left, will continue up-left if the top value on the stack is greater than `0`, or down-left if it is less than zero |
|`<`     |If moving to the right, will continue up-right if the top value on the stack is greater than `0`, or down-right if it is less than zero |
|`^`     |If moving to the down, will continue down-right if the top value on the stack is greater than `0`, or down-left if it is less than zero |
|`*`     |Pop the top two values from the stack, multiply them, and push the result to the stack |
|`a`     |Pop the top two values from the stack, add them, and push the result to the stack |
|`b`     |Print the top value from the stack |
|`c`     |Change direction: scan clockwise and continue |
|`d`     |Pop the top two values from the stack, divide the top by the second, and push the result rounded down to the stack |
|`f`     |Discard the top value from the stack |
|`j`     |Take the top two values from the stack as coordinates (top val = `x`, second val = `y`) and go to those coordinates in the grid |
|`n`     |Push a `0` onto the stack |
|`o`     |Change direction: scan counter-clockwise and continue |
|`p`     |Print the ASCII character corresponding to the top value on the stack |
|`r`     |Reverses the direction |
|`v`     |Print the number of values in the stack |
|`z`     |Copy the number `n` positions down in the stack where `n` is the current top value of the stack |
|`s`     |Pop the top two values from the stack, subtract them, and push the result to the stack |
|`u`     |Push a number from user input to the stack |
|`e`     |End the program |
