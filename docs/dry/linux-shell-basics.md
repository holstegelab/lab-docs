# Linux and Shell Basics

After login, you are working in a UNIX terminal.

## Essential commands

```bash
pwd        # show current directory
ls -lh     # list files with human-readable size
cd dir     # change directory
cd ..      # go one level up
mkdir dir  # create directory
rm file    # remove file
cp a b     # copy
mv a b     # move or rename
```

Manual pages:

```bash
man command
```

## File paths

### Absolute path

Starts from `/`:

```text
/project/holstegelab/Share/my_project/
```

### Relative path

Relative to your current directory:

```text
../data/
```

Use absolute paths in scripts to avoid ambiguity.

## Symlinks

Symlinks are pointers to files or directories and do not copy data.

Create:

```bash
ln -s /real/path/to/file link_name
```

Example:

```bash
ln -s /project/holstegelab/Share/references/hg38.fa hg38.fa
```

Inspect target:

```bash
ls -l
```

Remove symlink only:

```bash
rm link_name
```

Use symlinks to avoid duplicating large reference files.
