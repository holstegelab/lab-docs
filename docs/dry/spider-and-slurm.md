# Spider and Slurm

## Spider overview

Spider documentation:
[https://doc.spider.surfsara.nl/en/latest/Pages/getting_started.html](https://doc.spider.surfsara.nl/en/latest/Pages/getting_started.html)

Login:

```bash
ssh holstegelab-username@spider.surfsara.nl
```

Spider uses Slurm scheduler, shared project storage, and compute nodes.
Do not run heavy jobs on login nodes.

## Slurm references

- General docs: [https://slurm.schedmd.com/documentation.html](https://slurm.schedmd.com/documentation.html)
- Spider-specific docs: [https://doc.spider.surfsara.nl/en/latest/Pages/slurm.html](https://doc.spider.surfsara.nl/en/latest/Pages/slurm.html)

## Check available resources

```bash
sinfo
squeue -u $USER
```

## Interactive job for testing

```bash
srun --pty --cpus-per-task=4 --mem=16G --time=02:00:00 bash
```

## Batch job example

Create `job.sh`:

```bash
#!/bin/bash
#SBATCH --job-name=test
#SBATCH --cpus-per-task=8
#SBATCH --mem=32G
#SBATCH --time=12:00:00
#SBATCH --output=logs/%x_%j.out

source ~/.bashrc
conda activate myenv
python script.py
```

Submit:

```bash
sbatch job.sh
```

Check memory usage after completion:

```bash
sacct -j JOBID --format=JobID,MaxRSS,Elapsed
```
