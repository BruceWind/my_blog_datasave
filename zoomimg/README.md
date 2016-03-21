把需要缩小的图片放入此目录
## 1.缩小图片 
执行如下命令来缩小图片

``` shell
convert -resize 60%x60% ./*.JPG   small.jpg
```

## 2.文件批量命名

```
     for var in `ls`; do mv -f "$var" `echo "$var" |sed 's/^............./quanmin/'`; done
```
其中 ………….每个点代替字符数，这里有十个点，就是把前10个字符替换为quanmin。

## 3.使用tinypng进行压缩

另外一个shell命令，是想通过tinypng来压缩图片，只是目前这个shell命令还在编写中。
