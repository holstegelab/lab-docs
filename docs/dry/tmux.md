# tmux Session Management

Use `tmux` to keep long-running shell sessions alive across disconnects.

Start a new session:

```bash
tmux
```

Detach from session:

`Ctrl+b` then `d`

Reattach:

```bash
tmux attach
```

Quick cheatsheet:
[https://www.themoderncoder.com/uploads/simple-tmux-cheatsheet.jpg](https://www.themoderncoder.com/uploads/simple-tmux-cheatsheet.jpg)

Rule:
Never run long commands without `tmux` or a Slurm job allocation.
