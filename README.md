[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-green.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![MELPA](https://melpa.org/packages/flycheck-cask-badge.svg)](https://melpa.org/#/flycheck-cask)
[![MELPA Stable](https://stable.melpa.org/packages/flycheck-cask-badge.svg)](https://stable.melpa.org/#/flycheck-cask)

flycheck-cask
=============

Make [Flycheck][] use [Cask][] packages in [Cask][] projects.

A *Cask project* is denoted by the existence of a `Cask` file at the top of the
source code tree.  For Emacs Lisp files in such projects, this extension enables
`flycheck-emacs-lisp-initialize-packages` and set
`flycheck-emacs-lisp-package-user-dir` so that Flycheck picks up the
dependencies of the project when checking Emacs Lisp files.

Installation
------------

As usual, from [MELPA][] and [MELPA Stable][].

In your [`Cask`][cask] file:

```cl
(source gnu)
(source melpa)

(depends-on "flycheck-cask")
```

In your `init.el`:

```cl
(eval-after-load 'flycheck
  '(add-hook 'flycheck-mode-hook #'flycheck-cask-setup))
```

Usage
-----

Just use Flycheck as usual in Cask projects.

Customization
-------------

- <kbd>M-x customize-group RET flycheck-cask</kbd>

License
-------

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program.  If not, see http://www.gnu.org/licenses/.

See [`COPYING`][copying] for details.

[Flycheck]: https://github.com/flycheck/flycheck
[Cask]: https://github.com/cask/cask
[MELPA]: http://melpa.milkbox.net
[MELPA Stable]: http://melpa-stable.milkbox.net
[COPYING]: https://github.com/flycheck/flycheck-cask/blob/master/COPYING
