# Akamai CLI for Purge

Akamai CLI for Purge allows you to purge cached content from the Edge using
FastPurge (CCUv3).

FastPurge will typically invalidate (recommended), or delete cached content in
under five seconds.

## Install

To install, use [Akamai CLI](https://github.com/akamai/cli):

```
akamai get purge
```

You may also use this as a stand-alone command by simply downloading the
[latest release binary](https://github.com/akamai/cli-purge/releases)
for your system, or by cloning this repository and compiling it yourself.

### Compiling from Source

If you want to compile it from source, you will need Go 1.7 or later, and the [Glide](https://glide.sh) package manager installed:

1. Fetch the package:  
  `go get github.com/akamai/cli-purge`
2. Change to the package directory:  
  `cd $GOPATH/src/github.com/akamai/cli-purge`
3. Install dependencies using Glide:  
  `glide install`
4. Compile the binary:  
  - Linux/macOS/*nix: `go build -o akamai-purge`
  - Windows: `go build -o akamai-purge.exe`
5. Move the binary (`akamai-purge` or `akamai-purge.exe`) in to your `PATH`

## Usage

```
akamai-purge [global flags] command [--cpcode] [URLs/CPCodes...]
```

You may specify URLs/CPCodes as a list of arguments, or pipe in a newline-delimited list via STDIN

## Commands
- `invalidate` — Invalidate content
- `delete` — Delete content
- `list` — List commands
- `help` — Shows a list of commands or help for one command

## Global Flags
- `--edgerc value` — Location of the credentials file (default: "/Users/dshafik") [$AKAMAI_EDGERC]
- `--section value` — Section of the credentials file (default: "default") [$AKAMAI_EDGERC_SECTION]
- `--help`, `-h` — show help
- `--version`, `-v` — print the version
