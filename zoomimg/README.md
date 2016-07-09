
## 1.缩小图片 (本目录)
把需要缩小的图片放入此目录,执行如下命令来缩小图片

``` shell
convert -resize 40%x40% ./*.png   small.png
```


## 2.文件批量命名 （ reanme目录下）

```
     for var in `ls`; do mv -f "$var" `echo "$var" |sed 's/^............./quanmin/'`; done
```
其中 ………….每个点代替字符数，这里有十个点，就是把前10个字符替换为quanmin。

## 3.使用tinypng进行压缩  （small图片放到tinypng_python目录下）


curl --user api:s2buWr-AhtLZQLaNx9Uj2-O4J68nAKGO \
     --data-binary @small.png -i https://api.tinify.com/shrink

得到返回json之后 使用 wget 命令下载这个文件

