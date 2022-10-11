# `sh-print-nanos-now`

A simple Bash function to print the epoch time in floating-point format.

Depending on what's available on the system, uses `gdate` on macOS
(if installed, e.g., `brew install coreutils`), or `date` on Linux/GNU,
or a simple Python command otherwise.

## Overview

This project is an extremely simple Bash function. It exists solely so
the author can avoid copy-pasting the same nine lines of code between
different projects.

## Usage

Source the file and call the function it defines, or call the file directly.

E.g.,:

  ```shell
  $ . sh-print-nanos-now
  $ sh-print-nanos-now
  FIXME
  ```

Or:

  ```shell
  $ path/to/sh-print-nanos-now
  FIXME
  ```

## Installation

The author recommends cloning the repository and wiring its `bin/` to `PATH`.

You can also create a symlink to the executable from a location already
on `PATH`, such as possibly `~/.local/bin`.

Or you could clone the project and run the program directly to evaluate
it first, before deciding how you want to wire it.

Alternatively, you might find that using a shell package manager, such as
[`bkpg`](https://github.com/bpkg/bpkg),
is more appropriate for your needs, e.g.,
`bpkg install -g landonb/sh-print-nanos-now`.

### Makefile install

The included `Makefile` can also be used to help install.

- E.g., you could clone this project somewhere and
  then run a `sudo make install` to install it globally:

  ```shell
  git clone https://github.com/landonb/sh-print-nanos-now.git
  cd sh-print-nanos-now
  # Install to /usr/local/bin
  sudo make install
  ```

- Or specify a `PREFIX` to install anywhere else, such as locally, e.g.,

  ```shell
  # Install to $USER/.local/bin
  PREFIX=~/.local/bin make install
  ```

  And then ensure that the target directory is on the user's `PATH` variable.

  You could, for example, add the following to `~/.bashrc`:

  ```shell
  export PATH=$PATH:$HOME/.local/bin
  ```

### Manual install

If you clone the project and want the command to be callable in
your shell, remember to ensure that it can be found on `PATH`, e.g.,

  ```shell
  git clone https://github.com/landonb/sh-print-nanos-now.git
  export PATH=$PATH:/path/to/sh-print-nanos-now/bin
  ```

### Usage

  ```shell
  sh-print-nanos-now
  ```

Enjoy!

