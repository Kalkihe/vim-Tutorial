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

    h         # move left
    j         # move down
    k         # move up
    l         # mode right

## 2.1 Movement using words

    w         # move to the start of the next word
    e         # move to the end of the next word
    b         # move to the beginning of the next word

    \*        # move to the next occurence of the word that's currently under your cursor
    #         # move to the previous occurenc of the word that's currently under your cursor

## 2.2 Movement in the current line

    0         # move to the beginning of the current line
    $         # move to the end of the current line

## 2.3 Movement over several lines

    gg        # move to first line
    G         # move to last line
    <NUM>G    # move to the line with the number = <NUM> (give a number instead of <NUM>)


# 3. Searching

## 3.1 Finding characters

    fx        # find the character x in the current line
    <NUM>fx   # find the <NUM>th occurence of character x in the current line

## 3.2 Searching text

To search a word or more words, press / in normal mode and then type what you're searching for. If you performed that, you can press n (N) to find the next (previous) occurence of text that matches your search pattern. You can also use regular expressions as search pattern.
    
# 4. Manipulation

## 4.1 Select text

Press v to enter visual mode. In visual mode, you can select text using the keys given in chapter 2. It will always navigate from where your cursor is when you press v to the point you navigate to.

## 4.2 Manipulation of your selection

If you selected and highlighted text using the method of chapter 4.1, you have the following options:

    y         # copy the selection
    d         # cut the selection
    p         # paste text replacing the selection
    x         # delete text

## 4.3 Manipulation without preceded selection

You can manipulate characters or lines without selecting them in advance. 

    x         # delete character thats currently under the cursor
    r<CHAR>   # replace character thats currently under the cursor <CHAR>
    R         # start to write overwritting written text
    yy        # copy current line
    pp        # paste into current position
    dd        # cut current line

You can combine y, d and p with movement keys to handle a specified number of lines. For example:

    d3j       # cut the current line and three lines after it

## 4.4 Undoing, redoing, repeating

The commands in chapter 4 can be repeated, made undone or redone.

    .         # repeat last command
    u         # undo last command
    CTRL+r    # redo last command

# 5. Adding text

With the following keys, you enter insert mode. In insert mode, you are free to write whatever you want. You can get back to normal mode for example to navigate via pressing ESC.

  i           # start to insert text behind the current cursor position
  o           # add a new line after the current line and start to insert text there
  O           # add a new line before the current line and start to insert text there

# 6. Configuration

Vim can be configured in several ways, there are many options. 

## 6.1 Enter configuration

In vim, enter command-mode pressing : and type "e $MYVIMRC" to edit the configuration file. Put your configuration here and save the file with :w.  This file will be read every time vim starts. Since there are many options, further research may be neccessary. You can find my configuration [here](/Example_Files/vimrc). This file contains my preffered settings with explanations. You can either paste it when you are editing $MYVIMRC or you can download the file, rename it to .vimrc and place it in your home folder.

## 6.2 Trying out preferences

You can try every setting in vim directly. Just press : to enter command mode, enter set and the setting you want to set. If you want to unset something, do the same and put a 'no' before the name of the setting. For example

    :set number    # display line numbers
    :set nonumber  # don't display line numbers

### 6.2.1 Colorscheme

This works also for colorschemes. Simply enter the command mode (pressing : in normal mode), type "colo " and press tab to see what colorschemes are available. Press enter to try one of them. For exmaple

    :colo desert  # set colorscheme desert

# 7. Using vim for programming

When you're not using an IDE, you can write your source code with vim. Make sure to put 'syntax on' in your configuration to enable syntax highlighting. 

When you are using an IDE, you don't have to be mad. There are many plugins for all big IDEs out there that make the source code editors in them behave like vim. Just look for them.
