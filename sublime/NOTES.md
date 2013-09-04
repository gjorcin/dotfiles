
# Adding a command line utility for SublimeText

Use this to enable the `subl` utility to work with files and projects on the command line or as an EDITOR for unix tools such as git.

## Symlink for Ubuntu

    sudo ln -s ~/Sublime\ Text\ 3/sublime_text /usr/bin/subl

See [.desktop](./sublime.desktop) entry for a shortcut for Unity Launcher.

## OS X Command Line

**NOTE** This assumes Sublime Text is placed in 'Applications', and that ~/bin is in your path

    ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" ~/bin/subl

## Using as EDITOR

    export EDITOR='subl -w'

The `-w` flag will make `subl` wait for the file to be closed before exiting.

## Options

**NOTE** these are all accessible via `subl --help`

    Usage: subl [arguments] [files]         edit the given files
       or: subl [arguments] [directories]   open the given directories
       or: subl [arguments] -               edit stdin

    Arguments:
      --project <project>: Load the given project
      --command <command>: Run the given command
      -n or --new-window:  Open a new window
      -a or --add:         Add folders to the current window
      -w or --wait:        Wait for the files to be closed before returning
      -b or --background:  Don't activate the application
      -s or --stay:        Keep the application activated after closing the file
      -h or --help:        Show help (this message) and exit
      -v or --version:     Show version and exit

    --wait is implied if reading from stdin. Use --stay to not switch back
    to the terminal when a file is closed (only relevant if waiting for a file).

    Filenames may be given a :line or :line:column suffix to open at a specific
    location.


Please refer to [the official documentation](http://www.sublimetext.com/docs/3/osx_command_line.html) in case of snafu.