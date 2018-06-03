.. title: grep searches for PATTERN.
.. slug: grep-searches-for-pattern
.. date: 2018-05-25 11:28:01 UTC+07:00
.. tags: linux
.. category: software
.. link: 
.. description: 
.. type: text



grep searches for PATTERN in each FILE. A FILE of “-” stands for standard input. If no FILE is given, recursive searches examine the working  directory, and nonrecursive searches read standard input. By default, grep prints the matching lines.::

	grep -rnw '/path/to/somewhere/' -e 'pattern'

+ -r or -R  is recursive,
+ -n is line number, and
+ -w stands for match the whole word.
+ -l (lower-case L) can be added to just give the file name of matching files.

Along with these, --exclude, --include, --exclude-dir flags could be used for efficient searching.

+ This will only search through those files which have .c or .h extensions::

	grep --include=\*.{c,h} -rnw '/path/to/somewhere/' -e "pattern"

+ This will exclude searching all the files ending with .o extension::

	grep --exclude=*.o -rnw '/path/to/somewhere/' -e "pattern"

+ For directories it's possible to exclude a particular directory(ies) through --exclude-dirDocuments parameter. For example, this will exclude the dirs dir1/, dir2/ and all of them matching .dst/::

	grep --exclude-dir={dir1,dir2,*.dst} -rnw '/path/to/somewhere/' -e "pattern"

For more options check man grep.

|

References
----------
`rakib_ <https://stackoverflow.com/questions/16956810/how-do-i-find-all-files-containing-specific-text-on-linux>`_

