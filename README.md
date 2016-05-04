
# Bash Color Tools

bash-color-tools was created to solve a two problems that there were
no simple existing solutions for:

### Bash Prompt Color Themes
* I wanted an easy way to modify, set, and save Color Bash Prompt
  setups. The standard 8 colors are simply ugly, so being able to have
  hundreds of colors to choose from was a must. Plus, being able to
  easily and simply change the colors at will, ideally by X Color
  Name, or a standard hex or decimal value would also be great.

### Color Echo command
* I wanted an easy to use full-color echo command for use in scripts
  that worked just like echo, but could output in full color - not
  just the boring 8 colors that most HOW-TOs would teach you how to
  generate. And it had to insulate me from those horrible escape
  codes! Ideally, it could output those codes un-evaluated, for
  setting into variables if desired, say to put into the $PS1
  variable.

I tried a few python color prompt scripts first. They looked pretty
cool, but the lag was unbearable. It needed it to be lightweight and
fast. It definitely shouldn't need to load another separate script
interpreter to execute it. It simply had to be in clean, tight bash to
give the lowest latency script performance possible.


So, this is exactly what bash-color-tools sets out to provide:

### 'prompt'
* A full-color Bash Prompt theme framework that's easily customizable,
  and uses theme plugins to allow you to easily change the colors of
  every prompt string element, extend existing themes, or even create
  your own themes by starting off with the provided theme template and
  going from there. There's instructions in the examples directory to
  help you with that. Provides the ability to quickly toggle between
  the different themes. Also allows low-color mode themes for the
  Linux Terminal. If you create a cool theme, let me know and I'll add
  it in.

### 'face'
* A full-color echo-like command with all the semantics of echo, plus
  extensions for background and forground color designation, and can
  even output raw escape coded strings if you need them (which, as it
  turns out, prompt does).

### '_face'
* A sourceable library for your scripts, so all invocations of face
  come from memory, rather than running the command off disk.


## Standard Color Bash Prompt Themes:

* 'progit' is the default theme, and provides a very full-featured git
  status dashboard when inside a repository, and the date/time and
  current system load data when in a regular directory. It
  automatically 'fuzzy-truncates' (adjustable length and fuzzyness
  values) both the current dir path and the branch names to keep the
  prompt at a resonable length. The git dashboard shows the number of
  untracked files, index vs. tree status, merge status, commit status,
  etc., and the branch field will indicate if the remote is out of
  sync with your current tree. When your tree is up to date, it shows
  the current branch, and the standard time/date and system load
  header. This is quite possibly the most extensive git info in any
  prompt anywhere, while still being very fast and unobtrusive.

* 'git' is progit's predecessor, and not quite as fully featured. It
  does provide the basics though, and is a bit faster if you have a
  low powered machine.

* 'giles' is an homage to Giles Orr, the original Bash Prompt Howto
  author.

* 'vms' is an homage to the VMS Operating System I used so many years
  ago.


## Screenshots

![prompt image 1](/screenshots/screenshot-1.png?raw=true "Inside an up to date repo")

![prompt image 2](/screenshots/screenshot-2.png?raw=true "Untracked file added to repo")

![prompt image 3](/screenshots/screenshot-3.png?raw=true "Files staged")

![prompt image 4](/screenshots/screenshot-4.png?raw=true "Push puts remote in sync")

![prompt image 5](/screenshots/screenshot-5.png?raw=true "Git commit")

![prompt image 6](/screenshots/screenshot-6.png?raw=true "less -R shows 'face' palletes")

![prompt image 7](/screenshots/screenshot-7.png?raw=true "face pallette 1")

![prompt image 8](/screenshots/screenshot-8.png?raw=true "face pallette 2")

![prompt image 9](/screenshots/screenshot-9.png?raw=true "face pallette 3")

![prompt image 10](/screenshots/screenshot-10.png?raw=true "Using face to echo color strings")

![prompt image 11](/screenshots/screenshot-11.png?raw=true "Showing all of the color definition methods")


Manpage

Tested on Linux and Mac OSX (after installing bash v4.x)
