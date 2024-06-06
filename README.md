# hdeb

hdeb is a simple Bash script that simplifies the process of downloading and installing `.deb` packages from a remote URL. It provides a convenient way to fetch and install packages directly from the command line.

## Features

- Downloads `.deb` packages from a specified URL using `curl`
- Automatically installs the downloaded package using `dpkg`
- Cleans up by removing the downloaded `.deb` file after installation
- Supports silent mode with a progress bar for `curl` downloads
- Offers an optional `-k` flag to bypass SSL certificate verification

## Usage

```bash
hdeb <deb_url> [-k]
```

- `<deb_url>`: The URL of the `.deb` package to download and install.
- `-k` (optional): Bypasses SSL certificate verification for `curl` downloads.

### Examples

Download and install a `.deb` package:

```bash
hdeb 'http://example.com/package_1.0_amd64.deb'
```

Download and install a `.deb` package with SSL certificate verification bypassed:

```bash
hdeb 'https://example.com/package_1.0_amd64.deb' -k
```

## Requirements

- Bash shell
- `curl` command-line tool
- `dpkg` package manager

## Installation

### One-Line Installation

```bash
curl -sSL https://github.com/Anankke/hdeb/raw/master/hdeb -o /tmp/hdeb && sudo mv /tmp/hdeb /usr/local/bin/hdeb && sudo chmod +x /usr/local/bin/hdeb
```

### Manual Installation

1. Download the `hdeb` script.
2. Make the script executable using the following command:

```bash
chmod +x hdeb
```

3. Move the script to a directory in your system's `PATH` (e.g., `/usr/local/bin`) to make it accessible from anywhere:

```bash
sudo mv hdeb /usr/local/bin/
```

Now you can use the `hdeb` command from anywhere in your terminal to easily download and install `.deb` packages from remote URLs.
