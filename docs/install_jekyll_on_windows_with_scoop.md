# Install jekyll on Windows with [scoop](https://scoop.sh/)
Make sure PowerShell 5 (or later, include PowerShell Core) and .NET Framework 4.5 (or later) are installed.
Then run (no admin rights needed):

```shell
Set-ExecutionPolicy RemoteSigned -scope CurrentUser

iwr -useb get.scoop.sh | iex
```

And install packages:
```shell
scoop install psutils git-with-openssh
scoop bucket add extras
scoop bucket add versions
scoop install ruby26 msys2
```

After installing the packages, setup the MSYS2 and MINGW development toolchain.
```shell
ridk install
```
(Choose option 3)

Install bundler jekyll
```shell
gem install bundler jekyll
```
