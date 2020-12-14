# Notes 

A fork of notes that organize the files in a different way (~/notes/year/moth/day.txt)

### Text is amazing for notes because:

- You can use `grep` and friends to search through it later
- Even with notes dating back from 2001, I'm only using 1.5mb of disk space
- It's really easy to back up and sync to other devices using Drop Box or similar tools

Since it's unstructured text you can use this tool for whatever type of note
taking you want. You can keep track of general thoughts, create a diary or make
plan files similar to what John Carmack did [for a number of
years](https://github.com/ESWAT/john-carmack-plan-archive).

I personally use it as a scattered brain dump. Even with things being very
unstructured (and even untagged) I can usually `grep` out anything I want
within a few seconds.

### Your notes are organized by auto-dated files

Let's say it's December 25th, 2019. If you were to run `notes hello world` it
would create a `2019-12.txt` file in your `NOTES_DIRECTORY` (this is
something you can configure). It would then append `hello world` to the end of
the file.

If you run `notes something else` on the next day it will still append to the
same file and continue appending to that file until the next months hits. For
example, on January 1st 2020 any `notes` commands will append to a
`2020-01.txt` file.

There's other things you can do such as piping input to it, or running the
script without any arguments to open the file in your configured `EDITOR` but
let's first go over installing it before we get to that.

### What is this script not good for?

Depending on how you work, it's probably not ideal for grouping up a bunch of
extended thoughts about a specific topic.

For example, if you were planning to write a book and you spent 3 months
gathering info about what you're writing about then you would end up with a
bunch of isolated date formatted files that was mixed in with everything else.

In those cases, I recommend you make a new script called `book` which basically
does what this script does except it always dumps everything to 1 specific file
of your choosing which isn't dated. That's what I do to help plan my
[video courses](https://nickjanetakis.com/courses/).

## Usage Examples

There's 3 ways of using this script:

- `notes something you want to jot down`
  - Appends whatever arguments you add as text into the dated file

- `xclip -o | notes`
  - Pipes and appends anything (in this case your clipboard's contents) into the dated file

- `notes`
  - Opens the dated file in your configured `EDITOR`

That's really all there is to it. With the above 3 ways of adding notes you'll
find yourself adding all sorts of different types of notes with very little
friction. I encourage you to check out [just how short the source
code](https://github.com/nickjj/notes/blob/master/notes) is.
