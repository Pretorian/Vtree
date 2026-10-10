# vtree

A tiny, dependency-free command-line tool that prints a visual tree of your current directory.

```
/home/you/project
├── docs
│   └── guide.md
├── src
│   ├── utils
│   │   └── helpers.py
│   └── main.py
├── README.md
├── link -> src/main.py
└── run.sh

3 directories, 6 files
```

## Install

```bash
chmod +x vtree
sudo mv vtree /usr/local/bin/
```

Requires bash 3.2+ (macOS and Linux).

## Usage

```
vtree [options] [directory]
```

| Option         | Description                                   |
| -------------- | --------------------------------------------- |
| `-L <n>`       | Descend at most `n` levels                    |
| `-a`           | Include hidden files                          |
| `-d`           | Directories only                              |
| `-I <pattern>` | Ignore matches; separate several with `\|`    |
| `-A`           | ASCII lines instead of Unicode                |
| `-n`           | No color                                      |
| `-h` / `-v`    | Help / version                                |

```bash
vtree -L 2                        # two levels deep
vtree -a -I '.git|node_modules'   # dotfiles, minus the noise
vtree -d ~/projects               # folders only
```

Run it with `./vtree` or `bash vtree`, not `sh vtree`.

## License

Copyright 2026 [Your Name]

Licensed under the [Apache License, Version 2.0](LICENSE). Free to use, modify and distribute. Provided "as is", without warranty.
