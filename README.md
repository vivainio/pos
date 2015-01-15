# PsBookmark

Persistent bookmarks for PowerShell.

You may not be a fan of "cd bookmark" hacks that 

- Rely on expensive prompt hooks

- Don't work on windows

This PowerShell module provides cheap persistent bookmarks.

Load it up on new shell instances by adding it to your launch profile:

```shell

$ notepad $PROFILE
```

Add this line to the file:


```powershell
Import-Module C:/proj/psbookmark/psbookmark.psm1
```
(or equivalent, you get the idea).

Example use:

```powershell
$ cd c:\temp
$ Set-Bokmark t
$ cd c:\myapp
$ Set-Bookmark app
$ g t
$ g app
$ g

Name	value
----	-----
t       c:\temp
app     c:\myapp


$ Export-Bookmarks

```

Everything saved by Export-Bookmarks will be visible in subsequent PowerShell
launches (provided that you did the Import-Module, as above).
