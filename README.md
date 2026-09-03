# GoCrypter Builder

![GoCrypter](screenshot.png)

A lightweight Windows GUI tool that wraps your `.exe` inside a native Go loader, encrypts the payload, and produces a single self-contained executable.

## Download


## What it does

- Picks up any 32-bit or 64-bit PE file you supply.
- Encrypts it with AES and embeds the result inside a Go-compiled stub.
- The output loader decrypts the payload in memory and runs it on the target machine.
- Optional persistence via Scheduled Task, optional Defender exclusion, optional PowerShell command, optional extra payload.

## Requirements

- Windows 10 / 11
- **Go (Golang) must be installed** for the builder to compile the loader. Grab it from https://go.dev/dl/ or use the installer shipped under the `install/` folder of this repo.

## Quick start

1. Install Go and make sure `go version` works from any terminal.
2. Launch `CrypterBuilder.exe`.
3. Pick your input `.exe`, choose an output folder, click **Build Loader**.
4. The compiled loader is written next to the builder with a random 8-character filename.

## Important

Do **NOT** upload the resulting loader to VirusTotal or any other online scanner. These services forward samples to antivirus vendors, which will burn the stub within hours. Test locally only.

## Disclaimer

This project is published for educational and research purposes only.
