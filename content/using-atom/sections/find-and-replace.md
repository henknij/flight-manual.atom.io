---
title: Find and Replace
---
### Find and Replace

Finding and replacing text in your file or project is quick and easy in Atom.

* `cmd-F`: Search within a buffer
* `cmd-shift-f`: Search the entire project

If you launch either of those commands, you'll be greeted with the "Find and Replace" pane at the bottom of your screen.

![Find and replace text in the current file](../../images/find-replace-file.png)

To search within your current file you can hit `cmd-F`, type in a search string and hit enter (or `cmd-G` or the "Find Next" button) multiple times to cycle through all the matches in that file. The "Find and Replace" pane also contains buttons for toggling case sensitivity, performing regular expression matching and scoping selections.

If you type a string in the "Replace in current buffer" text box, you can replace matches with a different string. For example, if you wanted to replace every instance of the string "Scott" with the string "Dragon", you would enter those values in the two text boxes and hit the "Replace All" button to perform the replacements.

You can also find and replace throughout your entire project if you invoke the panel with `cmd-shift-F`.

![Find and replace text in your project](../../images/find-replace-project.png)

This is a great way to find out where in your project a function is called, an anchor is linked to or a specific misspelling is located. Click on the matching line to jump to that location in that file.

You can limit a search to a subset of the files in your project by entering a [glob pattern](http://en.wikipedia.org/wiki/Glob_%28programming%29) into the "File/Directory pattern" text box. When you have multiple project folders open, this feature can also be used to search in only one of those folders. For example, if you had the folders `/path1/folder1` and `/path2/folder2` open, you could enter a pattern starting with `folder1` to search only in the first folder.

Hit `escape` while focused on the Find and Replace pane to clear the pane from your workspace.

The Find and Replace functionality is implemented in the [atom/find-and-replace](https://github.com/atom/find-and-replace) package and uses the [atom/scandal](https://github.com/atom/scandal) package to do the actual searching.
