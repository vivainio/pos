# PsBookmark

Persistent bookmarks for PowerShell.

You may not be a fan of "cd bookmark" hacks that 

- Rely on expensive prompt hooks

- Don't work on windows

This PowerShell module provides cheap persistent bookmarks.

Load it up on new shell instances by:

```shell

$ notepad $PROFILE
```

Add this line to the file:


```powershell
Import-Module C:/proj/psbookmark/psbookmark.psm1
```
(or equivalent, you get the idea).

Example use:

```
$ cd c:/temp
$ set-bookmark m
$ cd c:/myapp
$ set-bookmark app
$ g m
$ g app
$ Export-Bookmarks

```

Everything saved by Export-Bookmarks will be visible in subsequent PowerShell
launces (provided that you did the Import-Module, as above).
