![Dwight and Mose paint](http://i.imgur.com/wgcq9Mk.jpg)

Fact: Dwight K. Schrute-mode or `schrute-mode` for short, is a minor global mode that will help you save time when you use inefficient commands on Emacs. By inefficient I mean using commands like `next-line` several times in a short period of time instead of, say, `avy`. If your memory is like mine, you'll often forget those features are available, if you commit the mistake of taking the long route, `schrute-mode` will be there to save the day... just don't forget to configure it!.

## How to install

If this package isn't on Melpa. Just clone it somewhere and add the file path location to your `load-path`.

    (require 'schrute)

    (setf schrute-shortcuts-commands '((avy-goto-line   . (next-line previous-line))
                                       (avy-goto-word-1 . (left-char right-char))))

    (schrute-mode)
