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


# 2. Adding text

# 3. Manipulating text

# X. Configuration

## X.1 Enter configuration

In vim, enter command-mode and type "e $MYVIMRC" to edit the configuration file.

## X.Y Colorscheme

<TODO: INSERT CONFFIGURATION FOR SETTING COLORSCHEME>

In vim, you can enter the command mode (pressing : in normal mode), type "colo " and press tab to see what colorschemes are available. Press enter to try one of them.  
