# Geany Syntax Highlighting For Pug

I have implemented quick and dirty syntax highlighting for Pug in the Geany editor.

## Installation

Copy the file `filetypes.Pug.conf` to your local config filedefs directory.

In my case, this was `~/.config/geany/filedefs`

Copy the file `filetype_extensions.conf` to your local config directory.

For me, this was `~/.config/geany`.

NB: If you already have a `filetype_extensions.conf` in there, do not overwrite it.
Instead, just add in the new settings from this one to whatever is already there.

Restart Geany, load a pug file and presto! Some kind of syntax highlighting.

It isn't very good, but I have absolutely no idea what I am doing.

Beats the default 'no syntax highlighting' in Pug files, though.

## What Is Going On Here

The `filetype_extensions.conf` file tells Geany that we have a new filetype called
'Pug' using the .pug extension, and that it is a kind of markup language.

This causes Geany to recognise Pug files.

The syntax highlighting (such as it is) is handled in `filetypes.Pug.conf`.

This is a modified copy of the existing HTML conf file. It uses the 'C' lexer (!),
the HTML tag parser, and contains two lists of pug keywords. There aren't many.

Honestly I have no idea how any of it is working, as it seems to be highlighting
other stuff than the keywords also. I just played around until something happened.

## That's Not Very Good Is It

No, not really. But I wanted to work on a project using Pug today, not work on
a syntax highlighting extension for Pug. See also 'quick and dirty'.

## TODO

Implement syntax highlighting for Pug properly.

Since the Pug syntax appears to be unlike any of the existing languages supported
by Geany, this will probably involve writing a custom lexer for it in C++.

I have absolutely no intention whatsoever of doing this, for a number of reasons,
starting with the fact that this is clearly not a great My First C++ project.

However, if you do it, please let me know.
