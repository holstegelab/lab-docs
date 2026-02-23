# Start Here

This page is the shortest path to getting productive on lab infrastructure.

## 1. Access Spider (SURF)

Spider documentation:
[https://doc.spider.surfsara.nl/en/latest/Pages/getting_started.html](https://doc.spider.surfsara.nl/en/latest/Pages/getting_started.html)

Login command:

```bash
ssh holstegelab-username@spider.surfsara.nl
```

## 2. Understand the execution model

- Use login nodes for light operations only.
- Submit compute-heavy work through Slurm.
- Keep long-running interactive work in `tmux` and/or a Slurm interactive session.

## 3. First commands after login

```bash
pwd
ls -lh
sinfo
squeue -u $USER
```

## 4. Non-negotiable rules

- Never run heavy jobs on a login node.
- Never store human raw genomic data on personal laptops.
- Never use consumer cloud storage for controlled data.
- Keep project directories structured and reproducible.

## 5. Next pages

- `Dry lab -> Spider and Slurm`
- `Dry lab -> Linux and Shell Basics`
- `Data management -> Project Structure`
