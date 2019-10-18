# zip_path_traversal
java生成包含../目录的压缩包

## 使用
`java -jar generateZip.jar parm1 parm2 parm3`

//第一个参数是需要压缩的源路径；第二个参数是压缩文件的目的路径，这边需要将压缩的文件名字加上去;第三个参数为zip压缩包中的目录命名

## Example
`java -jar generateZip.jar "D:\\dir1\\dir2\\dir3\\test.txt"  "D:\\dir1\\dir2\\dir3\\test.zip" "../../"`

在D:\\dir1\\dir2\\dir3\\生成目录结构为../../test.txt的test.zip压缩包，该压缩包解压会跳到D:\\dir1\\test.txt
