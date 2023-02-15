
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [markdown语法笔记(VScode)](#-markdown语法笔记vscode-)
  - [1.0 标题设置：](#-10-标题设置-)
  - [2.0 代码插入：](#-20-代码插入-)
  - [3.0  插入图片及图注：](#-30--插入图片及图注-)
    - [3.1 插入图片](#-31-插入图片-)
    - [3.2 图注](#-32-图注-)
    - [3.3 示例](#-33-示例-)
  - [4.0 文字效果](#-40-文字效果-)
    - [4.1 斜体](#-41-斜体-)
    - [4.2 粗体](#-42-粗体-)
    - [4.3 加粗斜体](#-43-加粗斜体-)
    - [4.4 删除线](#-44-删除线-)
  - [5.0 超链接](#-50-超链接-)
  - [6.0 注脚](#-60-注脚-)
  - [7.0 列表](#-70-列表-)
    - [7.1 无序列表](#-71-无序列表-)
    - [7.2 有序列表](#-72-有序列表-)
    - [7.3 定义型列表](#-73-定义型列表-)
    - [7.4 引用型列表](#-74-引用型列表-)
    - [7.5 代码块的引用](#-75-代码块的引用-)
    - [7.6 特殊情况](#-76-特殊情况-)
  - [8.0 引用](#-80-引用-)
  - [9.0 表格](#-90-表格-)
  - [10.0 公式](#-100-公式-)
    - [10.1 行内公式](#-101-行内公式-)
    - [10.2 整行公式](#-102-整行公式-)
  - [11.0 流程图的绘制](#-110-流程图的绘制-)
  - [12.0 分割线](#-120-分割线-)
  - [13.0 文字效果](#-130-文字效果-)
  - [14.0 关于MarkDown的快捷使用和简化](#-140-关于markdown的快捷使用和简化-)

<!-- /code_chunk_output -->

# markdown语法笔记(VScode)
  ## 0.0 所需的插件

  - Markdown All in one
  - Markdown PDF
  - Markdown Preview Github Styling
  - Markdown Preview Enhanced
  
## 1.0 标题设置：
```markdown{.line-numbers}
  1.#       一级标题
  2.##      二级标题
  3.###     三级标题
  4.####    四级标题
  5.#####   五级标题
  6.######  六级标题
  注：[TOC]自动生成目录

  在VSocde下利用插件Markdown Preview Enhanced（MPE）-->Markdown Preview Enhanced: Create Toc
  在光标处自动生成目录
```
## 2.0 代码插入：
```markdown{.line-numbers}
1.
  使用"code"如下效果：
    ```lang{.line-numbers}//添加序号
    code```
  自动添加序号：
    首先ctrl+shift+p,在命令面板输入user snippets新建全局代码:

    "creat to line number code": {
		"prefix": "code",
		"body": [
			"```${1:lang}{.line-numbers}",
			"${2:code}",
			"```",
			"${0}"
		],
		"description": "code block"
	  },

2.
    ```
    代码段
    ···
```
## 3.0  插入图片及图注：
### 3.1 插入图片
```markdown{.line-numbers}
  1.![Alt text](图片链接 "optional title")
      插入本地图片-->填入本地图片位置路径（与.md文件在同一文件夹下)

  2.<image src="image/imageName.png">
  example：
    <div align="center">[letf，center，right]              //图片的位置
    <image src="image/suis.png" width="" height="100"/>    //设置图片大小
    </div>
```
### 3.2 图注
```markdown{.line-numbers}
  <center>
  <image src="image/suis.png" width="30%"/>
  &emsp;&emsp;&emsp;
  <image src="image/ex.jpg" width="30%" />
    <br/>
图注：
第一种方式：
  <div style="color:write; border-bottom: 1px solid #d9d9d9;
      display: inline-block;
      padding: 2px;">填入图注内容</div> 
  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 
  <div style="color:red; border-bottom: 1px solid #d9d9d9;
      display: inline-block;
      padding: 2px;">填入图注内容</div>
  </center>
  <br/>
注：&emsp; 调整间距，插入空白

第二种方式：
  <font color="AAAAAA">002.jpg</font>
```
### 3.3 示例

  <center>
  第一种方式
  </center>

  <center>
  <image src="image/suis.png" width="30%"/>
  &emsp;&emsp;&emsp;
  <image src="image/ex.jpg" width="30%" />
  <br/>
  <div style="color:write; border-bottom: 1px solid #d9d9d9;
      display: inline-block;
      padding: 2px;">png1</div>
    &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
    &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
  <div style="color:red; border-bottom: 1px solid #d9d9d9;
      display: inline-block;
      padding: 1px;">jpg1</div>
  </center>
  <br/>

 <center>
  第二种方式
  </center>

  <center>
  <image src="image/suis.png" width="30%"/>
  &emsp;&emsp;&emsp;
  <image src="image/ex.jpg" width="30%" />
  <br/>
    <font color="yellow">1.png</font>
    &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
    &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
    <font color="blue">2.jpg</font>
  </center>
  <br/>

## 4.0 文字效果
### 4.1 斜体
  ```markdown{.line-numbers}
  *斜体* 或 _斜体_
  ```
  *斜体*
### 4.2 粗体
  ```markdown{.line-numbers}
  **粗体**
  ```
  **粗体**
  
### 4.3 加粗斜体
  ```markdown{.line-numbers}
  ***加粗斜体***
  ```
  ***加粗斜体***
### 4.4 删除线
  ```markdown{.line-numbers}
  ~~删除~~
  ```
  ~~删除线~~

## 5.0 超链接
  ```markdown{.line-numbers}
  1.<https://github.com/>
  2.[title](link)

  注：title非必要
      link链接地址
  ```
  超链接：
  <https://github.com/>
  锚点：
  [github](https://github.com/) 
## 6.0 注脚
  ```markdown{.line-numbers}
  [^1]:添加注脚
  ```
  使用注脚[^1]

  [^1]:注脚出现在文章的末尾，

## 7.0 列表
### 7.1 无序列表
```markdown{.line-numbers}
  用*，+，-表示无序列表
  - text1
  - text2
   
```
  - text1
  - text2

### 7.2 有序列表
```markdown{.line-numbers}
  直接用数字+英文句点
  1. text1
  2. text2
```
  1. text1
  2. text2
  
### 7.3 定义型列表
  定义型列表由名词与解释组成。
  一行写上定义，紧跟一行写上解释。
  解释的写法:紧跟一个缩进(Tab)

  ```markdown{.line-numbers}
  名词
:    解释

  ```
  名词
:    解释

### 7.4 引用型列表
  ```markdown{.line-numbers}
  - 把大象装入冰箱
    > 1.打开冰箱
    > 2.放入大象
    > 3.关门
  ```
  - 把大象装入冰箱
    > 1.打开冰箱
    > 2.放入大象
    > 3.关门
### 7.5 代码块的引用
  ```markdown{.line-numbers}
  <代码块>
  ```
### 7.6 特殊情况
  **在行首部出现数字-句点-空白时，需加入反斜杠**

## 8.0 引用

## 9.0 表格
  ```Markdown{.line-numbers}
  
  居左
  | text1 | text2 | text3 |
  | ----- | ----- | ----- |
  | text  | text  | text  |

  居中
  | text1 | text2 | text3 |
  | :---: | :---: | :---: |
  居右
  | text1 | text2 | text3 |
  | ----: | ----: | ----: |

  单元内文字换行使用<br>
  | text1 | text2     | text3        |
  | ----- | --------- | ------------ |
  | text  | text TEXT | text<br>TEXT |
  ```
  居左
  | text1 | text2     | text3        |
  | ----- | --------- | ------------ |
  | text  | text TEXT | text<br>TEXT |
  居中
  | text1 | text2 | text3 |
  | :---: | :---: | :---: |
  居右
  | text1 | text2 | text3 |
  | ----: | ----: | ----: |


## 10.0 公式
### 10.1 行内公式
  ```markdown{.line-numbers}
  $E=mc^2$ 
  ```
  $E=mc^2$ 

### 10.2 整行公式
  ```markdown{.line-numbers}
  $$E=mc^2$$
  ```
  $$E=mc^2$$

## 11.0 流程图的绘制
  ~~在反复尝试之后并没有绘制出流程图后发现~~**Markdown制作流程图较为抽象和繁琐，建议使用幕布等软件进行绘制流程图，然后插入图片**



## 12.0 分割线
  ```markdown{.line-numbers}
  * * *
  ***
  *****
  - - -
  ---------------------------------------
  ```
  * * *
  上下有两条分割线
  * * *
## 13.0 文字效果
  ### 13.1 文字位置
  ```Markdown{.line-numbers}
  <div align = center>
  文字居中
  </div>
  注：left（左),center（中）,right（右）
  ```
  <div align = center>
  文字居中
  </div>
  
  ### 文字字体，颜色和尺寸
  ```markdown{.line-numbers}
  使用font标签
  1. face->字体
  2. color->颜色,可用字母如red，black，blue，yellow等，也可用十六进制表示比如#0000ff
  3. size->尺寸,大小1-7，默认3

  例如
  <font face="楷体">楷体</font>
  <font face="隶书">隶书</font>
  <font face="宋体">宋体</font>
  <font color=red size=7 face="黑体">我是红色，宋体，大小是7</font>
  <font color=#074197 size=1>我的颜色是#074197，大小是1</font>
  ```
  <font face="楷体">楷体</font>
  <font face="隶书">隶书</font>
  <font face="宋体">宋体</font>
  
  <font color=red size=7 face="黑体">我是红色，宋体，大小是7</font>
  <font color=#074197 size=1>我的颜色是#074197，大小是1</font>
  


## 14.0 关于MarkDown的快捷使用和简化
  在诸如制表，插入图片，代码块等功能时比较浪费时间，为了提高使用效率可以全局代码编写如下代码
  ```json{.line-numbers}
    //插入代码
	"code block": {
		"prefix": "code",
		"body": [
			"```${1:lang}{.line-numbers}",
			"${2:code}",
			"```",
			"${0}"
		],
		"description": "code block"
	},
    //表格
	"Insert a simple table with text left": {
		"prefix": "tab",
		"body": [
			"|   |   |   |",
			"| - | - | - |",
			"|   |   |   |"
		],
		"description": "Insert a simple table with text  left"
	},
  ```































