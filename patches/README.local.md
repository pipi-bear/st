# Initial version

I cloned the `st/` directory from breads on penguins (https://github.com/BreadOnPenguins/st), 
which includes patches:

- alpha, changealpha
- Xresources w/ reload signal
- ligatures
- scrollback ringbuffer, with mouse
- anysize

# Patches that I added

- copyurl
- desktopentry

## Additional modifications for the patches I added

### copyurl

Based on `patches/st-copyurl-multiline-20230406-211964d.diff`, which would cause error when executing `make`:

- `term.line` is replaced by `TLINE`
> since `Term` no longer has the attribute `line`

