# ExcelCompareTool
### 工具是用shell脚本，和python写的，目的旨在对excel进行差异比较，因为在git项目中的excel差异是看不出来的（二进制），两次导出来再用比较工具比较，也是挺繁琐的一个步骤，所以写了一个工具，直接通过不同的commitid，进行差异对比，在非excel的差异中，一般都是文本，所以可以直接看出来，所以就对差异文件中的文本文件不做处理了

## 使用方法
1. 将脚本放到git项目的根目录下
2. 切到合适的分支
3. 运行`shell`目录下的`checkout_diff_files`脚本
4. 按照提示输入`commit id`
5. 得出差异文件结果`result.txt`

## 必不可少的东西
1. 安装python 笔者是安装的`python 3`
2. 安装python的模块 `xlrd` `numpy`
3. 如果表格是中文命名，命令行工具(bash)没有设置显示成中文，最好改一下设置
   设置链接：https://blog.csdn.net/u012145252/article/details/81775362

## 实现思路
1. 在git仓库下面获取两个commit之间的差异文件
2. 将差异文件放到本地
3. 解压差异文件
4. 本地还原被比较的文件
5. 调用python脚本对比excel
6. 将差异对比结果txt
7. (ps 如果1-4已经可以做完，也可以直接用成熟的比对工具（beyondCompare）比较)

## 实例：
+ shell脚本调用
