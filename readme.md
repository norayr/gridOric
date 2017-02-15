gridOric
========

gridOric is a small fun program for Oric Atmos or Pravetz-8D, which I have been written for  [MiniGame Compo 2003](http://web.archive.org/web/20080512084434/http://starbase.globalpc.net/minidir/index.main.html) - it participated in 4kb competition.

![gridoric](http://norayr.am/RetroComputing/Oric/gridoric/screenshot.png)

The program helps to create a good cryptographic [grille](https://en.wikipedia.org/wiki/Grille_(cryptography)). Then the created grille can be used to write and read encrypted texts. Grille as well as encrypted texts can be saved on tape.

Story
=====
When I was a kid, I loved short stories about Sherlock Holmes. After I have read "The Adventure of the Dancing Men" by Sir Arthur Conan Doyle, by using the same technique, I was able to decrypt and read old texts found in the notebooks of one of my old relatives. My mother was not happy about that, and to distract me from that, she said there are more advanced encryption methods and suggested to read Mathias Sandorf by Jules Verne to learn about them.

The grille from the book is very good one. It was not easy for me to design equally good grid to use with my friends at school. Back then, in early nineties I was not able to program something like this to help me to create a good grid.

Then years after, I wanted to represent Oric community at MiniGame Compo, and have been written this program. It has two modes - grille designer mode, and text encryption mode. I was not able to fit the decrypting part in to the required 4k output file. Though now I believe it is quite possible. (:

Running
=======
To load the program in the [xeuphoric](http://www.teaser.fr/~amajorel/xeuphoric/) emulator type:
```
CLOAD "GRID.TAP"
```

or 

```
CLOAD "GRID"
```

if you use modern xeuphoric.

Program will start automatically.

Usage
=====

Choose a task from menu:
1) Create new grid - This option allows to create a grid (something like a key) for encrypting and decrypting texts.

Example grid MATIAS which comes with the software is a grid from Jules Verne's 'Mathias Sandorf' book and looks like:

```
#O#O#O
####O#
##O###
#O##O#
#####O
###O##
```

This is an excellent grid: when you turn it around for 4 times, and write a text in the holes, then the resulting text will cover the whole square. And after the rotation the empty cells of the grid will never overlap with the cell on the paper where the letter have been already written.

To  place a hole on a grid you must press 'SPACE'. Use arrow keys to move around. Pressing space bar again will undo the placement of the empty cell there.

Other options:

2) Load grid - Load existing already created grid from the tape.
3) Save grid - Save created grid from the memory to the tape.
4) Edit grid. You can edit grid, which was saved before. It may be incomplete.
5) Write text - using the grid you can write texts just like you do on the paper. You type letters, and they appear in the right grid holes, then grid gets turned 90 degrees clockwise, you see more empty cells and type letters again. When there's no more space the grid turnes again. Until you fill the whole grid.

If you have made a mistake, just press 'BACKSPACE' or 'LEFT ARROW'.
Press any key when once empty cells are filled with letters and you need to turn the grid by 90 degrees again.

Then you can save encrypted text to the tape. This text can be decrypted with the grid, it was encrypted with.

6) Read text. Load it from tape. U can read encrypted text only if you have corresponding grid (key).
7) quit the program.

