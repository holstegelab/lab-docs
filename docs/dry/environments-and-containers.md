# Environments and Containers

Use isolated runtime environments for reproducibility.

## Conda and Mamba

Documentation:
- [https://docs.conda.io/](https://docs.conda.io/)
- [https://mamba.readthedocs.io/](https://mamba.readthedocs.io/)

`mamba` is a faster implementation of conda dependency resolution.

Create environment:

```bash
mamba create -n myenv python=3.11
```

Activate:

```bash
conda activate myenv
```

Export full environment:

```bash
conda env export > environment.yml
```

Export only explicitly installed tools:

```bash
conda env --from-history export > environment.yml
```

Recreate:

```bash
mamba env create -f environment.yml
```

Best practices:

- One environment per project
- Store `environment.yml` in the project repository
- Do not install tooling into `base`

## Apptainer and Singularity

Documentation:
[https://apptainer.org/docs/](https://apptainer.org/docs/)

Run container:

```bash
apptainer exec container.sif tool --help
```

Older command:

```bash
singularity exec container.sif tool --help
```

Bind project directory:

```bash
apptainer exec --bind /project container.sif tool
```

Store shared containers in:

```text
/project/holstegelab/Share/containers/
```
