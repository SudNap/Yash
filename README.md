# YASH — Yet Another SHell

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Version](https://img.shields.io/badge/version-D.0.0.1-yellow)
![Status](https://img.shields.io/badge/status-prototype-orange)
![Platform](https://img.shields.io/badge/platform-Termux_·_Linux_·_macOS_·_BSD-lightgrey)
![License](https://img.shields.io/badge/mit-license-inactive)

> [!WARNING]
> Early development build. Not a production shell. Test in a disposable directory.

---

## Overview

| Field | Value |
|:---|:---|
| Name | YASH — Yet Another SHell |
| Version | D.0.0.1 |
| Language | Python 3 |
| Targets | Termux, Linux, macOS, BSD |
| Status | Development prototype |
| License | Not specified |

---

## Install

| Step | Command |
|:---:|:---|
| 1 | `python3 --version` |
| 2 | `mkdir -p ~/.yash/work` |
| 3 | `cp -r yashlib ~/.yash/work/` |
| 4 | `mkdir -p ~/.yash/work/bin` |
| 5 | `cp bin/yash ~/.yash/work/bin/yash` |
| 6 | `chmod +x ~/.yash/work/bin/yash` |

```sh
python3 --version
mkdir -p ~/.yash/work
# extract archive, then from its directory:
cp -r yashlib ~/.yash/work/
mkdir -p ~/.yash/work/bin
cp bin/yash ~/.yash/work/bin/yash
chmod +x ~/.yash/work/bin/yash
```

Add to PATH:

```sh
export PATH="$HOME/.yash/work/bin:$PATH"
```

> [!NOTE]
> Do not replace your system PATH. Start with `yash`.

---

## Features

| Feature | Detail |
|:---|:---|
| Prompt | `localhost>username_>` · root: `root_>` |
| Config | `~/.config/yash/config.java` (`key = "value"`) |
| Profiles | `~/.config/yash/profiles/` · `yash profile NAME` + restart |
| Reload | `yash reload` / `reload` — config and aliases |
| Aliases | `~/.yash/yalias.txt` · `yalias ll <"ls" -la>` |
| Variables | `{NAME}` expansion |
| Command lookup | `{PATH2} command` · no PATH fallback |
| Separators | `:&` conditional · `\` pipeline · `#` background · `@` comment |
| Tab completion | Python readline where available |
| Logs | `~/.yash/logs/` · rotation into `.tar.gz` |

---

## Command Reference

| Token | Meaning |
|:---:|:---|
| `:&` | Conditional command separator |
| `\` | Pipeline |
| `#` | Run command in background (trailing) |
| `@` | Start a comment |
| `{NAME}` | Variable expansion |
| `{PATH2}` | Explicit command lookup path |

---

## Prototype Limits

> [!IMPORTANT]
> Early build. Read limits before running.

<details>
<summary>Full list</summary>

| # | Limit |
|:---:|:---|
| 1 | Not a production shell |
| 2 | Updater is a placeholder — no server/repo configured |
| 3 | Tab completion depends on platform `readline` |
| 4 | Pipeline parsing is basic; complex quoting, redirection, job control, shell scripting, full POSIX not implemented |
| 5 | `#` is background marker — use `@` for comments |
| 6 | Launches external commands with normal permissions — test in a disposable directory |

</details>

---

Badge · badges 5 · tables 6
