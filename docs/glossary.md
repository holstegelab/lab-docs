# Glossary

- **Spider**: SURF HPC platform used by the lab.
- **Slurm**: workload manager and job scheduler used on Spider.
- **Login node**: entry node for light commands, editing, and job submission.
- **Compute node**: node where actual compute jobs run.
- **Batch job**: non-interactive job submitted with `sbatch`.
- **Interactive job**: shell allocated through Slurm, usually with `srun --pty`.
- **Conda/Mamba environment**: isolated software environment per project.
- **Apptainer/Singularity**: container runtime for reproducible execution on HPC.
- **Symlink**: filesystem pointer to another path, created with `ln -s`.
- **MaxRSS**: peak memory usage reported by Slurm accounting tools.
