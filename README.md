This Python script can generate mazes of arbitrary size and output them as png images using pypng. It can generate a 1000x1000 pixel maze in about 1 second on my hardware.

To generate the maze, Prim's algorithm is applied to a randomly-weighted lattice graph to produce a minimum-cost spanning tree. Alternatively, the program can generate a random spanning tree; this mode is faster and uses much less memory.

### Requirements

Python 2 and [pypng](https://code.google.com/p/pypng/downloads/list). The easiest way to set up pypng is to simply copy png.py to the same directory as mazes.py.

### Usage

    $ python mazes.py -h
    usage: mazes.py [-h] [--prims | --random] -s size size [-o filename]
    
    Generate a maze with one of two algorithms.
    
    optional arguments:
      -h, --help    show this help message and exit
      --prims       Use Prim's algorithm
      --random      Produce a random spanning tree
      -s size size  The maze's size, width then height in cells
      -o filename

 ### Sample maze

 ![Sample maze](http://i.imgur.com/rsjyy.png)