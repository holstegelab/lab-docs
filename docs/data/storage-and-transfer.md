# Storage and Transfer

## Storage tiers

### Active storage

```text
/project/holstegelab/Share/
```

### Archive or tape

Use for long-term storage and retrieval, not active analysis workflows.

Reference:
[https://servicedesk.surf.nl/wiki/spaces/WIKI/pages/29557422/dCache](https://servicedesk.surf.nl/wiki/spaces/WIKI/pages/29557422/dCache)

### ResearchDrive

Use for collaboration and small dataset sharing.

Reference:
[https://researchdrive.surf.nl/apps/files/files](https://researchdrive.surf.nl/apps/files/files)

## Transfer tools

### rsync (recommended)

```bash
rsync -avh source destination
```

### rclone

Reference:
[https://rclone.org/](https://rclone.org/)

### sshfs

Mount remote systems locally for interactive file access.

### scp

Copy individual files across hosts.
