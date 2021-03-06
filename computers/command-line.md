<!-- TITLE: Command Line -->
<!-- SUBTITLE: A quick summary of Command Line -->

# Command Line Tips

## Work Smarter To Work Harder

Sometimes it's the little things.

### Using Aliases to Save Key Strokes

If you can't be bothered to untrain the muscle memory of using the command line instead of PowerShell or bash then at least make your life a little easier by setting up some aliases for often typed commands.  There are mine:

```bash
@echo off

DOSKEY ls=dir
DOSKEY tam=python c:\tam\tam.py $*
DOSKEY pp=python -m json.tool $*
```

_Fun Fact_ The `$*` denotes that everything after the aliaes should be passed through.

### Load them every time

1. Create a bat or cmd file
2. Put all your doskey tricks in it
3. Create a shortcut for c:\windows\system32\cmd.exe
4. In the shortcut's properties change it to `c:\windows\system32\cmd.exe  /K "C:\Users\Shawn\Dropbox (Personal)\Tools\doskey-aliases.cmd"`
5. Change **Start In** to `%HOMEDRIVE%%HOMEPATH%`
6. Save, Run