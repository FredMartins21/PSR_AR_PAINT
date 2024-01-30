# PSR: Augmented Reality Paint
Augmented Reality Paint project for the course of Programming of Robotic Systems, 2022/2023.

Students:
- Isabel Rosário (NMec 93343)
- João Bastos (NMec 98245)

## Usage Manual

In order to try the AR Paint program, start by installing the [ScreenLight application](https://play.google.com/store/apps/details?id=com.nekobukiya.screenlight&hl=pt_PT) on your phone. After that, choose a color and run the `color_segmenter.py` script, adjusting the RGB dials in order to segment the color detection to the color you chose on the application.

Other functionalities to keep in mind when doing color segmentation:
- pressing `w` will save the current setup to a file called *limits.json* located in the current directory;
- pressing `q` will quit the program **without** saving the current setup.

Now, run the `ar_paint.py` script with the following **optional** command line arguments:
- `-j` or `--json`: provide the path to the *.json* file with the color segmentation data that is generated by the `color_segmenter.py` script; if you don't provide any path, the program will try to read from a file called *limits.json* in the project directory;
- `-usp` or `--use_shake_prevention`: a flag to indicate that you wish to use the shake detection mechanism;
- `-m` or `--mouse`: a flag to indicate that you wish to use the mouse as the pencil pointer for drawing instead of the centroid of the biggest color blob detected by the program;

The `-h` or `--help` option will give you same information on the command line arguments of `ar_paint.py` that is given here.

Other functionalities to keep in mind when drawing:
- pressing `r`, `b` or `g` will change the pencil color to red, blue or green, respectively;
- pressing `-` or `+` will decrease or increase the pencil thickness, respectively;
- pressing `c` will clear the canvas;
- pressing `w` will save the current canvas as a *.png* image in the program directory;
- pressing `s`, `e` or `o` will activate and deactivate figure mode, drawing squares/rectangles, ellipses and circles, respectively;
- pressing `space` will activate and deactivate the coloring mode, dividing the canvas into numbered zones and displaying the number/color correlation (at the end of each coloring session, the coloring accuracy will be calculated and shown);
- pressing `q` will quit the program.

