# TinyTeX releases for Windows, macOS, and Linux

<a href="https://yihui.org/tinytex/"><img src="https://yihui.org/images/logo-tinytex.png" alt="tinytex logo" align="right" width="200px" /></a>

TinyTeX is a lightweight, cross-platform, portable, and easy-to-maintain LaTeX distribution based on TeX Live. You may see the Github repo (https://github.com/yihui/tinytex) and project homepage (https://yihui.org/tinytex/) for more info.

## Releases

The binary packages of TinyTeX are published (monthly) to the Github Releases of this repository: https://github.com/yihui/tinytex-releases/releases Each release contains three versions of TinyTeX:

- `TinyTeX-0.*` contains the `infraonly` scheme of TeX Live, without any LaTeX packages.

- `TinyTeX-1.*` contains [about 60 LaTeX packages](https://github.com/yihui/tinytex/blob/master/tools/pkgs-custom.txt) enough to compile common R Markdown documents (which was the original motivation of the TinyTeX project).

- `TinyTeX.*` contains [more LaTeX packages](https://github.com/yihui/tinytex/blob/master/tools/pkgs-yihui.txt) requested by the community.

The `zip` packages are for Windows. The `tgz` packages are for macOS. The `tar.gz` packages are for Linux.

## Chocolatey package

You may install TinyTeX as [a Chocolatey package](https://chocolatey.org/packages/tinytex). First, you would need to install the [Chocolatey Package Manager](https://chocolatey.org/install) if it has not already been installed. Next type in the following command to install TinyTeX:

```powershell
choco install tinytex
```

This will install TinyTeX and make the TeX Live package manager, `tlmgr` available on PATH.

To uninstall TinyTeX, use the command:

```powershell
choco uninstall tinytex
```

## Scoop packages

Scoop is another package manager for Windows. You need to install [_scoop_](https://scoop-docs.now.sh/docs/getting-started/Quick-Start.html) first to use it from powershell.

Apps for _scoop_ are available through "buckets". For now, TinyTeX binary packages are not available in the default **main** or **extras** buckets that comes with a new installation of _scoop_, but through the scoop bucket **r-bucket** at https://github.com/cderv/r-bucket/ with other R-related tools.

You need first to add this bucket
```powershell 
scoop bucket add r-bucket https://github.com/cderv/r-bucket.git
```

Then you can install **one of** the binaries: 

* Recommanded installation of `TinyTeX.zip`
```powershell
scoop install TinyTeX
```

* Minimal installation (infra-only) of `TinyTeX-0.zip`
```powershell
scoop install TinyTeX-min
```

* Full installation (more packages) of `TinyTeX-1.zip`
```powershell
scoop install TinyTeX-min
```

This will install TinyTeX and make the TeX Live package manager, `tlmgr` available on PATH.

Only one of this installation can work at the same time, so you won't be able to install one on an other. This will fail gracefully:

```powershell
❯ scoop install TinyTeX-min
Installing 'TinyTeX-min' (2020.09) [64bit]
Starting download ...
Download: (OK):download completed.
Checking hash of TinyTeX-0.zip ... ok.
Extracting TinyTeX-0.zip ... done.
Running pre-install script...
--> Another TinyTeX already found. Cancelling current installation...
Uninstalling 'TinyTeX-min' (2020.09).
'TinyTeX-min' was uninstalled.
Exception: You already have Tinytex installed. Run scoop uninstall Tinytex if you want to use TinyTeX-min.
```

To uninstall :
```powershell
scoop uninstall TinyTeX
# or 
scoop uninstall TinyTeX-min
# or 
scoop uninstall TinyTeX-full
```