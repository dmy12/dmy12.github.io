
_未分类_

---

### 搭建个人博客

这个博客是基于Github Pages和docsify搭建的，主要用来存档和讲废话，估计更新频率不高。所以希望：
* 博客简洁清爽
* 搭建过程不需要安装其它我平常不用的东西，如`Node.js`，`npm`，`docsify cli`等。

以下是遵从上面两个原则的搭建过程：

1. docsify

	用docsify主要是因为Github提供的theme我都不喜欢，自己又不会写，搜索了一圈之后觉得docsify够简洁也够美观，于是决定试一试docsify。

	* 官网：[docsify](https://docsify.js.org/)。
	* 示例和插件：[Awesome docsify](https://docsify.js.org/#/awesome)
	* 配置docsify文件

		主要改`index.html`。
		
		这一步遇到的坑是`coverpage`和`sidebar`。因为我什么都没安装，自然无法生成`.nojekyll`，所以文件名以下划线开头的文件读取有点问题。
		
		解决方法：
		```css
		window.$docsify = {
		    coverpage: 'coverpage.md',
		    loadSidebar: 'sidebar.md',
		},
		```

		用到的一些插件：
		* Katex(_这个要放在`docsify.min.js`前_), 搜索, 字数统计, 图片放大,一键复制代码

2. Github Pages

	* 新建一个GitHub Repository。Repository name = username.github.io

	* 在Settings->GitHub Pages里设置（非必须）
	> Your GitHub Pages site is currently being built from the `/docs` folder in the master branch.

3. 本地预览网站
	```py
	python -m http.server 3000
	```
	可通过`http://localhost:3000/`进行本地预览。

	为了方便本地预览，我设置了不用缓存。
	```css
	requestHeaders: {
	    'cache-control': 'max-age=0',
	},
	```

4. 把改好的docsify文件上传到Github repository
	
	[My Blog](/)




_全程操作下来花了大半天的时间，主要是sidebar不显示的坑，不走弯路的话应该很快能搞定。_

---

### git小技巧

- 删除提交历史

	看着乱糟糟的commits history烦死，很有必要删除历史记录。

	[GitHub - Delete commits history with git commands](https://gist.github.com/heiswayi/350e2afda8cece810c0f6116dadbe651)

	```
	git checkout --orphan TEMP_BRANCH # Check out to a temporary branch:
	git add -A # Add all the files:
	git commit -am "Initial commit" # Commit the changes:
	git branch -D master # Delete the old branch:
	git branch -m master # Rename the temporary branch to master:
	git push -f origin master # Finally, force update to our repository:
	```
- 单独上传本地修改的文件

	```
	git status
	git add -u
	git status
	git commit -m "update"
	git branch --set-upstream-to=origin master
	git pull
	git push
	```
___

### 自定义锚(Anchor)和页内跳转

页内跳转方式一：

跳转到某个标题：
[跳转到“Katex数学公式”](#Katex数学公式)
```markdown
[跳转到“Katex数学公式”](#Katex数学公式)
```

页内跳转方式二：

自定义锚点并[跳转](#anchor1)
```markdown
<!--定义锚点-->
<span id="anchor1">End
<!--跳转-->
[跳转到anchor1](#anchor1)
```
_注：锚点id里有大写字母的时候似乎会跳转不成功。_

___
### 字体设置

<!--中文字体：SimHei, SimSun, NSimSun, FangSong, KaiTi, FangSong_GB2312, KaiTi_GB2312, STXihei, STHeiti, STKaiti, STSong, STFangsong-->

```html
<p style="font-family:STFangsong; font-size:17px; color:lightgreen;">
试一下字体：一二三四五六七八九十
</p>
<font color="blue">颜色</font>
```
<p style="font-family:STXihei; font-size:17px;">
试一下细黑：一二三四五六七八九十
</p>
<p style="font-family:STHeiti; font-size:17px;">
试一下黑体：一二三四五六七八九十
</p>
<p style="font-family:STKaiti; font-size:17px;">
试一下楷体：一二三四五六七八九十
</p>
<p style="font-family:STSong; font-size:17px;">
试一下宋体：一二三四五六七八九十
</p>
<p style="font-family:STFangsong; font-size:17px; color:lightgreen; ">
试一下字体：一二三四五六七八九十
</p>

顺便也试一下颜色
<span>
<font color="red">红<font color="orange">橙<font color="yellow">黄<font color="green">绿<font color="darkgreen">青<font color="blue">蓝<font color="purple">紫</font></font></font></font></font></font></font>
</span>

_测试结果：电脑上字体正常显示，手机上似乎都是默认字体。_

___
### Katex数学公式



```Katex

$k \geq 5$

$$
\begin{pmatrix}
   a & b \\
   c & d
\end{pmatrix}
$$

$$
    A=\left(\begin{array}{ccccc}
        9 & 1 & 1 & 4 \\
        1 & 9 & 4 & 1 \\
        1 & 4 & 9 & 1 \\
        4 & 1 & 1 & 9
    \end{array}\right), \;
    b = \left(\begin{array}{c}
    1 \\ 1 \\ 1\\ 1
    \end{array}\right),\;
    x_0 = \left(\begin{array}{c}
    1 \\ 0 \\ 0 \\ 0
    \end{array}\right).
$$

```
$k \geq 5$

$$
\begin{pmatrix}
   a & b \\
   c & d
\end{pmatrix}
$$

$$
    A=\left(\begin{array}{ccccc}
        9 & 1 & 1 & 4 \\
        1 & 9 & 4 & 1 \\
        1 & 4 & 9 & 1 \\
        4 & 1 & 1 & 9
    \end{array}\right), \;
    b = \left(\begin{array}{c}
    1 \\ 1 \\ 1\\ 1
    \end{array}\right),\;
    x_0 = \left(\begin{array}{c}
    1 \\ 0 \\ 0 \\ 0
    \end{array}\right).
$$

_测试结果：电脑上正常显示，手机上可以显示但是公式太长的话会有部分看不到。_

___

<span id="anchor1">End