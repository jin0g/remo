# remo

Automatically synchronize with the remote environment, login to an interactive queue for cluster, build containers, and enter the container as needed.

## Usage

```bash
$ remo your_command
```

### Options

- `--init`    - Create a `.remo` configuration file in the current directory.
- `--edit`    - Edit the existing `.remo` configuration file.
- `--verbose` - Enable detailed output.
- `--help`    - Display help information.

## Example

### `$ remo --init`

Initialize a Configuration.
Creates a `.remo` file in the current directory with default settings.

### `$ remo nvidia-smi`

You can check remote environments gpu configuration.

### `$ remo python your_script.py`

You can run your script on the server and container.

### `$ remo wget https://your/IP/restricted/content.html`

You can download IP restricted contents.
New files will sync from remote to local.

## Configuration File

```bash
# REMOTE: Remote server address
REMOTE="user@example.com"
# PREFIX: Command prefix (e.g., for job schedulers)
PREFIX="srun -p a100 --pty"
# CONTAINER_MODE: Container runtime (singularity or apptainer, docker in the future)
CONTAINER_MODE="apptainer"
# CONTAINER_FILE: Container definition file
CONTAINER_FILE="hello.def"
```
