Adam's vimrc
-----

To use, want to do this:

```bash
$ git clone github.com/adamhjk/adam-vim ~/.vim
$ cd ~/.vim
$ make install
```

Then marvel at what's up.

## Important configuration stuff

Leader is mapped to ','

## Plugins

The current list is maintained in the vimrc through vundle. Check out vimrc.

## Commands

### Tags
```
[:TlistOpen] Opens the tag list window
[:TlistToggle] Toggle the tag list window
```
### Surround
Details follow on the exact semantics, but first, consider the following
examples.  An asterisk (*) is used to denote the cursor position.

```
  Old text                  Command     New text ~
  "Hello *world!"           ds"         Hello world!
  [123+4*56]/2              cs])        (123+456)/2
  "Look ma, I'm *HTML!"     cs"<q>      <q>Look ma, I'm HTML!</q>
  if *x>3 {                 ysW(        if ( x>3 ) {
  my $str = *whee!;         vlllls'     my $str = 'whee!';
```
```
[ds] = Delete surrounding - use the character or a 't' for tag (ds", dst)
[cs] = Change surrounding - first what to change, then what to change to
[ys] = Takes a motion and surrounds it with the second argument, like cs
[s] = In visual mode, wraps the text with the character argument
```

### NERD_commenter
```
[,cc] = Comment the current line, or selected text in visual mode
[,c ] = Toggle the comment
[,ci] = Toggles the set of lines individually (like "c ", but assumes each line may have different settings)
[,cs] = Comment Sexily - up close to the start of each line
[,cA] = Append a comment to the end of the line
[,cl] = Comment and align on the left side
[,cb] = Comment and align on both sides
[,cu] = Uncomment the selected lines
```
### Textile
```
[,rp] = :TextilePreview - render textile to a temp file, open in browser
[,rt] = :TextileRenderTab - render textile to a new tab
[,rf] = :TextileREdnerFile - render to a file
```
### Keymaps
```
[,d] = Toggle NERDtree
[,t] = Command-T
[,l] = TListToggle 
```

