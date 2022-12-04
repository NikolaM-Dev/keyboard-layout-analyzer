<h1 align="center">
<img
    src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/misc/transparent.png"
    height="30"
    width="0px"
  />
keyboard-layout-analyzer ⌨
<img
    src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/misc/transparent.png"
    height="30"
    width="0px"
  />
</h3>

<p align="center">
  <a href="https://github.com/NikolaM-Dev/keyboard-layout-analyzer/stargazers">
    <img
      src="https://img.shields.io/github/stars/NikolaM-Dev/keyboard-layout-analyzer?colorA=363a4f&colorB=b7bdf8&style=for-the-badge"
    />
  </a>
  <a href="https://github.com/NikolaM-Dev/keyboard-layout-analyzer/issues">
    <img
      src="https://img.shields.io/github/issues/NikolaM-Dev/keyboard-layout-analyzer?colorA=363a4f&colorB=ff9e64&style=for-the-badge"
    />
  </a>
  <a href="https://github.com/NikolaM-Dev/keyboard-layout-analyzer/contributors">
    <img
      src="https://img.shields.io/github/contributors/NikolaM-Dev/keyboard-layout-analyzer?colorA=363a4f&colorB=9ece6a&style=for-the-badge"
    />
  </a>
</p>

&nbsp;

Calculates the number of finger movements required to type something using
different keyboard layouts.

I was obsessed with different keyboard layouts. Like everyone else, I wanted to
find the ULTIMATE keyboard layout. Well, It's not that easy, so I wrote an
application which takes multiple lines of characters and calculate the finger
movements to that is required to type it.

Supported keyboard layouts are

- QWERTY
- DVORAK
- HALMAK
- WORKMAN
- COLEMAK
- COLEMAK DH
- RSTLNE

## How to Interpret

- **Finger Movements _(Lower the better)_** - User has to move the finger to
  press the key.
- **Same Finger Usage _(Lower the better)_** - Same finger usage to type
  different.
  letters ("lo" in "hello" with QWERTY).
- **No Movement _(Higher the better)_** - Move finger movement needed to type
  these letters because the finger should be on the letter when touch typing.

## Sample Output 1

**Command:** `echo hello | keyboard-layout-analyzer`

Following are the results for for typing "hello".

| CATEGORY              | QWERTY | DVORAK | HALMAK | WORKMAN | COLEMAK | COLEMAK DH | RSTLNE |
| --------------------- | -----: | -----: | -----: | ------: | ------: | ---------: | -----: |
| Finger Movements      |      3 |      2 |      2 |       2 |       3 |          3 |      3 |
| Same Finger Usage     |      1 |      0 |      0 |       0 |       0 |          0 |      0 |
| No Movement           |      2 |      3 |      3 |       3 |       2 |          2 |      2 |
| Up Movement           |      2 |      2 |      2 |       0 |       2 |          2 |      0 |
| Down Movement         |      0 |      0 |      0 |       2 |       0 |          1 |      0 |
| Right Movement        |      0 |      0 |      0 |       0 |       0 |          0 |      2 |
| Left Movement         |      1 |      0 |      0 |       0 |       1 |          0 |      1 |
| Top Right Movement    |      0 |      0 |      0 |       0 |       0 |          0 |      0 |
| Top Left Movement     |      0 |      0 |      0 |       0 |       0 |          0 |      0 |
| Bottom Right Movement |      0 |      0 |      0 |       0 |       0 |          0 |      0 |
| Bottom Left Movement  |      0 |      0 |      0 |       0 |       0 |          0 |      0 |

## Sample Output 2

**Command:** `cat /<path>/**/*.go | keyboard-layout-analyzer`

Following are the results for one of my Go & TS projects.

### [Cobra 🐍](https://github.com/spf13/cobra)

```sh
echo ./**/*.go | keyboard-layout-analyzer
```

| CATEGORY              | QWERTY | DVORAK | HALMAK | WORKMAN | COLEMAK | COLEMAK DH | RSTLNE |
| --------------------- | -----: | -----: | -----: | ------: | ------: | ---------: | -----: |
| Finger Movements      | 219910 | 140040 | 131738 |  131738 |  116510 |     116510 | 116510 |
| Same Finger Usage     |  28271 |  16186 |  17488 |   15702 |   10908 |      10908 |  26711 |
| No Movement           |  73112 | 152982 | 161284 |  161284 |  176512 |     176512 | 176512 |
| Up Movement           | 117046 |  71832 |  65862 |   67919 |   48016 |      48016 |  48157 |
| Down Movement         |  34993 |  20103 |  56720 |   45710 |   34993 |      39694 |  44086 |
| Right Movement        |   8996 |  18477 |      0 |    8996 |   12878 |       8996 |  13762 |
| Left Movement         |   7267 |  12878 |      0 |    1708 |    7267 |      12399 |   7267 |
| Top Right Movement    |  26063 |   1708 |    160 |    3078 |    8996 |       3078 |    160 |
| Top Left Movement     |   1708 |   9580 |      0 |     257 |     257 |        257 |      0 |
| Bottom Right Movement |   3078 |   2384 |      0 |    3045 |    3078 |       3045 |      0 |
| Bottom Left Movement  |  20759 |   3078 |   8996 |    1025 |    1025 |       1025 |   3078 |

### [Nest 😼](https://github.com/nestjs/nest)

```sh
echo ./**/*.ts | keyboard-layout-analyzer
```

| CATEGORY              | QWERTY | DVORAK | HALMAK | WORKMAN | COLEMAK | COLEMAK DH | RSTLNE |
| --------------------- | -----: | -----: | -----: | ------: | ------: | ---------: | -----: |
| Finger Movements      |  47599 |  29233 |  26471 |   26471 |   21747 |      21747 |  21747 |
| Same Finger Usage     |   5324 |   2050 |   4509 |    1995 |    2101 |       2101 |   5267 |
| No Movement           |  17928 |  36294 |  39056 |   39056 |   43780 |      43780 |  43780 |
| Up Movement           |  27181 |  17773 |  11017 |   12555 |    8444 |       8444 |   8505 |
| Down Movement         |   8219 |   4408 |  13669 |    9876 |    8219 |       7617 |   9991 |
| Right Movement        |   1703 |   3833 |      0 |    1703 |    1332 |       1703 |   2277 |
| Left Movement         |    665 |   1332 |      0 |     333 |     665 |       1979 |    665 |
| Top Right Movement    |   6076 |    333 |     82 |     227 |    1703 |        227 |     82 |
| Top Left Movement     |    333 |    855 |      0 |     151 |     151 |        151 |      0 |
| Bottom Right Movement |    227 |    472 |      0 |     620 |     227 |        620 |      0 |
| Bottom Left Movement  |   3195 |    227 |   1703 |    1006 |    1006 |       1006 |    227 |

## Prerequisites

- Rust

## Install

- Build and install

```sh
cargo install --path .
```

- Make sure the cargo bin is in PATH environment variable.

```sh
export PATH=$PATH:~/.cargo/bin
```

## How to Use

- Pipe the content to `keyboard-layout-analyzer`.

```sh
echo hello | keyboard-layout-analyzer
```

- Pipe file content to `keyboard-layout-analyzer`.

```sh
cat text.txt | keyboard-layout-analyzer
```

- Pipe entire project `keyboard-layout-analyzer`.

```sh
cat <path>/**/*.txt | keyboard-layout-analyzer
```

&nbsp;

<p align="center">
  <img
    src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/footers/gray0_ctp_on_line.svg?sanitize=true" />
</p>
<p align="center">
  Copyright &copy; 2021-present
  <a href="https://github.com/s1n7ax" target="_blank">
    <strong>S1n7ax</strong>
  </a>
</p>
<p align="center">
  <a href="https://github.com/NikolaM-Dev/keyboard-layout-analyzer/blob/main/LICENSE">
    <img
      src="https://img.shields.io/static/v1.svg?style=for-the-badge&label=License&message=MIT&logoColor=d9e0ee&colorA=363a4f&colorB=b7bdf8" />
  </a>
</p>
