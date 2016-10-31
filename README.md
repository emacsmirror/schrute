[![MELPA](http://melpa.milkbox.net/packages/schrute-badge.svg)](http://melpa.milkbox.net/#/schrute)

![Dwight and Mose paint](http://i.imgur.com/Yp1sxel.jpg)

Dwight K. Schrute-mode or `schrute-mode` for short, is a minor global mode that will help you to remember that there is a better way to do something. By better I mean using commands like `avy-goto-line` instead of making several invocations of `next-line` in a row with either `C-<down>` or `C-n` keybindings. If your memory is like mine, you'll often forget those features are available, if you commit the mistake of taking the long route, `schrute-mode` will be there to save the day... just don't forget to configure it!.

## How to install

If this package isn't on Melpa. Just clone it somewhere and add the file path location to your `load-path`.

    (require 'schrute)

    (setf schrute-shortcuts-commands '((avy-goto-line   . (next-line previous-line))
                                       (avy-goto-word-1 . (left-char right-char))))

    (schrute-mode)
