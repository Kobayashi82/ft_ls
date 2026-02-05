<div align="center">

![System & Kernel](https://img.shields.io/badge/System-brown?style=for-the-badge)
![Filesystem](https://img.shields.io/badge/Filesystem-Directory-blue?style=for-the-badge)
![C Language](https://img.shields.io/badge/Language-C-red?style=for-the-badge)

*A reimplementation of the classic ls command*

</div>

<div align="center">
  <img src="/ft_ls.png">
</div>

# ft_ls

[README en Espanol](README_es.md)

`ft_ls` is a from-scratch implementation of the Unix `ls` command. This project focuses on directory traversal, file metadata, sorting, and output formatting while matching the system `ls` behavior as closely as possible.

### What is ls?

`ls` is the standard utility to:

- List files and directories.
- Inspect permissions, sizes, owners, and timestamps.
- Sort and filter entries.
- Traverse directories recursively.

### Technical flow

1. Parse flags and input paths.
2. Read directory entries with `opendir` and `readdir`.
3. Collect metadata with `stat` or `lstat`.
4. Sort entries by name or time.
5. Format output (long format, hidden files, reverse order).
6. If `-R` is set, recurse into subdirectories.

## 🔧 Installation

```bash
git clone https://github.com/Kobayashi82/ft_ls.git
cd ft_ls
make
```

## 🖥️ Usage

```bash
./ft_ls [options] [file ...]
```

### Options
| Option | Category  | Description                          |
|--------|-----------|--------------------------------------|
| `-a`   | Listing   | Include hidden entries (dotfiles)    |
| `-R`   | Listing   | Recursively list subdirectories      |
| `-t`   | Sorting   | Sort by modification time            |
| `-u`   | Sorting   | Use access time for sorting          |
| `-r`   | Sorting   | Reverse sort order                   |
| `-f`   | Sorting   | Do not sort; enable `-a`             |
| `-l`   | Display   | Long listing format                  |
| `-g`   | Display   | Long format without owner            |
| `-d`   | Display   | List directories themselves          |

### Examples

```bash
./ft_ls
./ft_ls -la
./ft_ls -lrt src
./ft_ls -R .
```

## 📄 License

This project is licensed under the WTFPL – [Do What the Fuck You Want to Public License](http://www.wtfpl.net/about/).

---

<div align="center">

**📂 Developed as part of the 42 School curriculum 📂**

*"See your system as it really is"*

</div>
