# Short vim-Tutorial

This tutorial serves the needs of my ePortfolio-Presentation in the lecture 'Software Engineering' in wintersemester 2018/19. Due to that fact, this tutorial does not call itself complete. 

# 1. Basics

To start vim, simply type vim into the standard console of your system:

    vim

This will open a new file. To edit an already existing file, type the one of the following (depending on your system) into your console:

    vim /path/to/file.txt
    vim C:\path\to\file.txt

To save a file, open the command mode using : and then give a simple w. After this, press Enter.

    :w

To save a file under a new name, do as above and give a filename before pressing Enter.

    :w /path/to/new/file.txt

To edit an already existing file when vim is already opened, open the command mode using :, type e and enter the path to the file. Then press Enter.

    :e /path/to/already/existing/file.txt

To exit vim, enter command mode using :, then type q and press Enter

    :q

To exit not saving performed changes, add an !.

    :q!

# 2. Movement

In normal mode, there are several ways to move your cursor in your text. When you start vim, you're in normal mode. You can also get there from insert or command mode pressing ESC.

    h     # move left
    j     # move down
    k     # move up
    l     # mode right

## 2.1 Movement using words

    w     # move to the start of the next word
    e     # move to the end of the next word
    b     # move to the beginning of the next word

    \*     # move to the next occurence of the word that's currently under your cursor
    #     # move to the previous occurenc of the word that's currently under your cursor

## 2.2 Movement in the current line

    0     # move to the beginning of the current line
    $     # move to the end of the current line

## 2.3 Movement over several lines

    gg    # move to first line
    G     # move to last line
    xG    # move to the line with the number = x (give a number instead of x)


# 3. Manipulating text

# X. Configuration

## X.1 Enter configuration

In vim, enter command-mode and type "e $MYVIMRC" to edit the configuration file.

## X.Y Colorscheme

<TODO: INSERT CONFFIGURATION FOR SETTING COLORSCHEME>

In vim, you can enter the command mode (pressing : in normal mode), type "colo " and press tab to see what colorschemes are available. Press enter to try one of them.  
