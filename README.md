# zip_path_traversal
java生成包含../目录的压缩包
## 使用
java -jar generateZip.jar parm1 parm2 parm3
parm1为被压缩的文件
parm2为生成压缩文件的路径
parm3为添加的跨目录符号，如../../../sss/
## Example
java -jar generateZip.jar "D:\\dir1\\dir2\\dir3\\test.txt"  "D:\\dir1\\dir2\\dir3\\test.zip" "../../"
会在D:\\dir1\\dir2\\dir3\\生成目录结构为../../test.txt的test.zip压缩包，该压缩包解压会跳到D:\\dir1\\test.txt
