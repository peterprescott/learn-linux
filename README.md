# Learn Linux

To unleash the power of computers, you have to learn how to talk to them.

## Echoing

The most simple thing is for the computer to `echo` you.

```
echo hello
```

The computer will say (well, print) 'hello' back to you.

## Asking WHO

Try asking the computer, `whoami`? You don't need the question mark. And note
that there are no spaces. Computer language isn't normal English.

The reply you get will be the username you used to log in: for me, it's `peterprescott`.

Now ask the computer its name. This is another odd space-less sentence: `uname`?
And the computer will reply `Linux`.

## Asking WHAT

Now that we've been introduced, we can ask some more questions.

Like what is the `echo` function exactly? Well, we can ask that with
`whatis`.

```
whatis echo
```
An `echo`, we are told, will *display a line of text*. Okay, you could have
worked that out on your own. Well, since you're clever, try asking
```
whatis whatis
```

You should get the reply:
```
whatis (1)           - display one-line manual page descriptions
```

That suggests there are longer manual descriptions.

We can find them by using the `man` command. 'What is man?' (--that God be mindful
of him) is a profound question. But `whatis man` tells us that `man` is *an
interface to the on-line reference manuals*. So let's try `man echo`, and
instead of the one-line answer we got with `whatis echo`, we get more than a
whole screen of explanation of the different things we can do with the simple
echo command.

At the bottom you will see that you can *press `h` for help or `q` to quit*.
Press `q` to check it works. Then again type `man echo`, and this time press
`h`. Again there's an overwhelming amount of detail, but for the moment just
note that you can go forward one line by pressing `j` or backward one line by
pressing `k`. There are also other ways of going forward and backwards, as well
other ways of searching through the man(ual), but ignore those, quit the help
menu (`q`), and practise using `j` and `k` to move forwards and backwards along
the `man echo` page.

Learning to use those keys to move up and down instead of the arrow keys will be
very useful as we go on to text-editing in Vim, and even computer-gaming in
Rogue.

Now you know how to use `whatis` and `man`, you can use them for any Linux
command you encounter about which you want more information.

## Asking WHEN

Now we know about WHO and WHAT, we can ask WHEN and WHERE.

The way I set up [my personal Linux
configuration (use it if you like!)](https://github.com/peterprescott/.dotfiles), we can already see
the answer to these questions in the command-line status bar without asking at
all. (Or at least, the asking is through a hidden file, `.zshrc`, the zee shell
run-commands file)

First let's talk about WHEN. My command-line tells us the time, but if we ask
for the `date`, we get told the day, the date, the month, the time and timezone,
and the year. If we read the manual, we see that there are lots of ways we can
be more precise about what date/time information we want.

We can even ask things like `date -s 'next Thursday'`.

## Asking WHERE

My command-line gives us an indication of *where* we are, highlighted in blue.
It might not be obvious that that is what it's doing, if it's just giving you a
wiggle: `~`.

In Linux, the *tilde* symbol `~`, is used to signify a user's home directory (or
folder).
Mine is `/home/peterprescott`. Yours is probably `/home/` followed by your own
username. We could say `/home/$USERNAME` -- the `$` is used by the command
*shell* to represent
variables.

The Linux command to ask for the name of the directory (folder) that you're in
is more difficult to remember than the `whoami` and `whatis` commands we've learned so
far. It is just three letters, squeezed together: `pwd`. They stand for
**p**rint **w**orking **d**irectory.

## Looking Around

But you don't just want to know where you are, you want to know what else is
there.

If you type `ls` then the computer will tell you all the other files and folders
that are in the folder where you are.

Actually, that's not quite true. If there are hidden files or folders you won't
see them. Unless you ask specifically, by typing `ls -a` (a for *all*). Hidden
files have names that start with a dot, so they're *dotfiles* -- usually
configuration files that you don't want to mess around with once your system is
working how it should be.

Unless of course you like messing around with things to learn how they work the
way they should...







