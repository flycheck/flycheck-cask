flycheck-cask
=============

Make Flycheck use Cask packages in [Cask][] projects.

A *Cask project* is denoted by the existence of a `Cask` file at the top of the
source code tree.  For Emacs Lisp files in such projects, this extension enables
`flycheck-emacs-lisp-initialize-packages` and set
`flycheck-emacs-lisp-package-user-dir` so that Flycheck picks up the
dependencies of the project when checking Emacs Lisp files.

Installation
------------

As usual, from [MELPA](http://melpa.milkbox.net) and
[Marmalade](http://marmalade-repo.org/).

In your [`Cask`][cask] file:

```lisp
(source melpa)

(depends-on "flycheck-cask")
```

In your `init.el`:

```lisp
(eval-after-load 'flycheck
  '(add-hook 'flycheck-mode-hook #'flycheck-cask-setup))
```

Usage
-----

Just use Flycheck as usual in Cask projects.

Customization
-------------

- `M-x customize-group RET flycheck-cask`

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

See [COPYING](https://github.com/flycheck/flycheck-cask/blob/master/COPYING) for
details.

[cask]: https://github.com/cask/cask
