---
title: Grammar
---
### Grammar

The "grammar" of a buffer is what language Atom thinks that file content is. Types of grammars would be Java or Markdown. We looked at this a bit when we created some snippets in link:/using-atom/sections/snippets[Snippets].

If you load up a file, Atom does a little work to try to figure out what type of file it is. Largely this is accomplished by looking at its file extension (`.md` is generally a Markdown file, etc), though sometimes it has to inspect the content a bit to figure it out if it's ambiguous.

If you load up a file and Atom can't determine a grammar for the file, it will default to 'Plain Text', which is the simplest one. If it does default to 'Plain Text' or miscategorize a file, or if for any reason you wish to change the active grammar of a file, you can pull up the Grammar selector with `ctrl-shift-L`.

![Grammar selector](../../images/grammar.png)

Once the grammar of a file is changed manually, Atom will remember that until you set it back to auto-detect or choose a different grammar manually.

The Grammar selector functionality is implemented in the [atom/grammar-selector](https://github.com/atom/grammar-selector) package.
