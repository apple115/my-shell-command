# my-shell-command
收集一些我会使用的shell 命令

shell 要写对是一件很难的时
但是我这又一些模板，可能可以更好的写出shell

``` shell
#!/usr/bin/env bash
# Program:
#  This program shows "Hello world" ! in your screen.
# History:
# 2015/07/16 VBird First release
set -Eeuo pipefail
trap cleanup SIGINT SIGTERM ERR EXIT
cleanup() {
  trap - SIGINT SIGTERM ERR EXIT
  # script cleanup here
}

script_dir=$(cd "$(dirname "${BASH_SOURCE[0]}")" &>/dev/null && pwd -P)
```

可能后续会加上解释
