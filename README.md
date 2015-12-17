# drop-in

This  program  adds, replaces or removes specially-marked segments in a text file.
Each segment is marked by a keyed, commented BEGIN and END tag used to identify it.

Running `drop-in added bar foo` on these files:
```
# File 'foo'      # File 'bar'
Foo Line 1        Bar Line 1
Foo Line 2        Bar Line 2
```
...will result in the file `foo` looking like this:
```
# File 'foo'
Foo Line 1
Foo Line 2
#BEGIN-added
#File 'bar'
Bar Line 1
Bar Line 2
#END-added

This process may be repeated multiple times to add additional named segments to the file.

Full deteails are in the manual page supplied with the program.
