Adam's vimrc
-----

To use:

```bash
$ git clone github.com/justinredd/vimrc ~/.vim
$ cd ~/.vim
$ make install
```

Then marvel at what's up.

## Important configuration stuff

Leader is mapped to ','

## Plugins

The current list is maintained in the vimrc through vundle. Check out vimrc.

## Commands

### Surround
Details follow on the exact semantics, but first, consider the following
examples.  An asterisk (*) is used to denote the cursor position.

```
  Old text                  Command     New text ~
  "Hello *world!"           ds"         Hello world!
  [123+4*56]/2              cs])        (123+456)/2
  "Look ma, I'm *HTML!"     cs"<q>      <q>Look ma, I'm HTML!</q>
  if *x>3 {                 ysW(        if ( x>3 ) {
```
```
[ds] = Delete surrounding - use the character or a 't' for tag (ds", dst)
[cs] = Change surrounding - first what to change, then what to change to
[ys] = Takes a motion and surrounds it with the second argument, like cs
[s] = In visual mode, wraps the text with the character argument
```
