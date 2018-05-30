<!-- TITLE: Command Line -->
<!-- SUBTITLE: A quick summary of Command Line -->

# Command Line Tips
## Using Aliases to Save Key Strokes

```bash
DOSKEY ls=dir
```

### Load them every time

1. Create a bat or cmd file
2. Put all your doskey tricks in it
3. Create a shortcut for c:\windows\system32\cmd.exe
4. In the shortcut's properties change it to `c:\windows\system32\cmd.exe  /K "C:\Users\Shawn\Dropbox (Personal)\Tools\doskey-aliases.cmd"`
5. Change **Start In** to `%HOMEDRIVE%%HOMEPATH%`
6. Save, Run