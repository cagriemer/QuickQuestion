# Quick Question

[Pretty version](http://ttscoff.github.com/QuickQuestion/)

Written by Brett Terpstra for Mac OS in mind
I have modified it for my operating system Ubuntu

### Installation ###

**Command line**
: Put the `qq` script into a folder in your path and make it executable with `chmod a+x /path/to/qq`. Edit the script to set the location of your notes folder and the extension you use. You may want to set a different preferred "question" prefix if you already have one (or don't want filenames that need constant escaping).

### Usage ###

**Command line**
: Add questions and answers using `qq -a "Question" "Answer"`, e.g. `qq "What is the answer to life, the universe and everything?" "42"`. If `-a` is specified without any additional arguments, `qq` will enter interactive mode and ask you for the question and the answer individually, accepting input from STDIN.
: Ask a question using `qq fragmented question`, e.g. `qq meaning universe`. See the [Querying](#querying) section for more information on composing fragmented queries.

### Composing questions ###

Ask yourself what question the search for this answer began with. Will that be the question you ask again when you've forgotten the answer a year (or month) later? Think about how you, personally, would phrase the question and shape it around keywords that you're pretty sure you would repeat.

Keep your questions in a natural language format, but avoid contractions and use "who, when, where, what, how and why" as much as possible. These words make it easy to sort out different types of questions about the same subject.

### Querying ###

When querying, only use operative terms to get the best results. "Where did I leave my glasses" will return poor results if the question you labeled it with was "Where did I put my glasses". Instead, query "Where*" and you'll find the note instantly.

Running `qq -l` at the command line will list all of the questions in your archive. This can be handy for using with `grep` to parse out pieces of questions that you couldn't find otherwise.

### Copy to clipboard ###

If your answer includes a command, url or other piece that you probably want to grab, you can surround it with @copy(part to copy) and the contents of the tag will be copied to the clipboard when the question is answered.

### Auto-open related urls ###

If you add one or more @open() tags, the contents will be passed to the `firefox` command with the `-new-window` option. You can use this to add related urls to the query. It's not a perfect system because if you ask a broad question and get 20 answers, each with one or more urls, they'll all open. But it's handy once in a while.

### Redacting answers ###

From the command line you can use the `-e` argument to open the first result for the following query in the editor you specified in the configuration (`nano` by default). It expects a command-line tool, not an OS X application name. Most editors have these available.

### TODO ###

* meta tags part needs to be refactored.
