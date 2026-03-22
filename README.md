# <img src="./misc/river-shifttags-repo.png" width="24"/> fork of [river-shifttags](https://gitlab.com/akumar-xyz/river-shifttags)

A small utility for the river-classic Wayland compositor to rotate the focused
tags. Useful for focusing next/prev tag, or rotating the whole tagmask if
multiple tags are in focus.

# Installation

```sh
$ make
$ sudo make install
```

# Usage

To rotate the currently focused once to the right
```sh
river-shifttags
```

To rotate the currently focused once to the left
```sh
river-shifttags --shifts -1
```

To rotate a different number of tags
```sh
river-shifttags --num-tags 16
```

Use the `--occupied` flag to skip unoccupied tags while shifting
```sh
river-shifttags --shifts -1 --occupied
```

Use the `--unoccupied` flag to skip occupied tags while shifting
```sh
river-shifttags --shifts -1 --unoccupied
```

## Example configuration

```sh
map="riverctl map"
mod=Mod4

$map normal $mod apostrophe                 spawn "river-shifttags --occupied"
$map normal $mod semicolon                  spawn "river-shifttags --occupied --shift -1"
$map normal ${mod}+Shift apostrophe         spawn "river-shifttags"
$map normal ${mod}+Shift semicolon          spawn "river-shifttags --shift -1"
$map normal ${mod}+Control apostrophe       spawn "river-shifttags --unoccupied"
$map normal ${mod}+Control semicolon        spawn "river-shifttags --unoccupied --shift -1"
```

# Contributing

Please feel free to submit a merge request if you find something to improve in
the code. Come across an issue? please report it. 

tl;dr contributions welcome.


# License

GPLv3
