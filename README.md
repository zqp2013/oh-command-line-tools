```
HARMONY_TOOLS_DIR=~/oh/command-line-tools ant -f harmony-build.xml AIPlayApp
```

### 打包、切分
```
tar -cJf 6.1.0.830.tar.xz command-line-tools/
split -b 80m 6.1.0.830.tar.xz part_
```

### 合并、解包
```
cat part_* > bigfile.tar.xz
rm -rf part_*
tar -xJf bigfile.tar.xz
```
