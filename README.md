[![MELPA](http://melpa.milkbox.net/packages/schrute-badge.svg)](http://melpa.milkbox.net/#/schrute)

![Dwight and Mose paint](http://i.imgur.com/Yp1sxel.jpg)

Dwight K. Schrute-mode or `schrute-mode` for short, is a minor global mode that will help you to remember that there is a better way to do something. By better I mean using commands like `avy-goto-line` instead of making several invocations of `next-line` in a row with either `C-<down>` or `C-n` keybindings. If your memory is like mine, you'll often forget those features are available, if you commit the mistake of taking the long route, `schrute-mode` will be there to save the day... just don't forget to configure it!.

## How to install

If this package isn't on Melpa. Just clone it somewhere and add the file path location to your `load-path`.

    (require 'schrute)

    (setf schrute-shortcuts-commands '((avy-goto-line   . (next-line previous-line))
                                       (avy-goto-word-1 . (left-char right-char))))

    (schrute-mode)

## Be aware!!

Some functions in Emacs will throw an error if they can't complete a task, this feature is part of their design, which may enter in conflict with schrute-mode functionality of "trying the command again until success". One of these commands is `next-line` which throws an error if they reach the button of the current buffer.

This major mode will tell you when a function is causing the error `"Lisp nesting exceeds ‘max-lisp-eval-depth’"` so you can fix it. See issue #1 for more information.
