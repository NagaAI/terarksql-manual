## 启动脚本说明 - 读写混合

一般情况下，大部分参数保持默认即可，个别需要配置的参数如下，具体说明请查看“完整配置”：

```
#!/bin/bash

DIR="$(cd "$(dirname "$0")" && pwd)"

env TerarkZipTable_localTempDir=$DIR/terark-temp \
    TerarkZipTable_keyPrefixLen=4 \
    TerarkZipTable_offsetArrayBlockUnits=128 \
    TerarkZipTable_indexCacheRatio=0.001 \
    TerarkZipTable_extendedConfigFile=$DIR/license \
    $DIR/support-files/mysql.server start --defaults-file=$DIR/my.cnf
```