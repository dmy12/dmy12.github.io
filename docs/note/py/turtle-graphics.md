
_turtle 海龟绘图_

---

```py
from turtle import *
```
与绘图无关，与存图有关：
```py
canvas = getscreen().getcanvas()
canvas.postscript(file='turtle_graphic_example' + '.eps')
```
`.eps`转`.jpeg`:
```py
from PIL import Image
img = Image.open(filename+'.eps')
img.load(scale=4)
quality_val = 95
img.save(filename+'.jpeg','JPEG', quality=quality_val)
```
___

试一下bgcolor和random:

<img src="https://user-images.githubusercontent.com/64673363/90334267-f434a700-dffe-11ea-9d6e-eb29310dd0dd.jpeg" width="50%">

___

螺旋

<img src="https://user-images.githubusercontent.com/64673363/90337739-133f3300-e017-11ea-9cb6-e20cdd15a782.jpeg" width="45%"> <img src="https://user-images.githubusercontent.com/64673363/90337741-176b5080-e017-11ea-8df2-1d5a6a9d2570.jpeg" width="45%">

___

几个简单图形：

<img src="https://user-images.githubusercontent.com/64673363/90338237-c52c2e80-e01a-11ea-8f7f-b6bb567a4c57.jpeg" width="30%"> <img src="https://user-images.githubusercontent.com/64673363/90338238-c8bfb580-e01a-11ea-83d8-f26fc9243699.jpeg" width="30%">
<img src="https://user-images.githubusercontent.com/64673363/90338240-c9f0e280-e01a-11ea-866d-b06ce3fb8b9d.jpeg" width="30%">

___

实物模仿，我的抱枕

<img src="https://user-images.githubusercontent.com/64673363/90334261-f0a12000-dffe-11ea-980a-14d4bb647928.jpeg" width="30%"> <img src="https://user-images.githubusercontent.com/64673363/90334266-f39c1080-dffe-11ea-9192-ee9ef76c6ab6.jpeg" width="30%">
<img src="https://user-images.githubusercontent.com/64673363/90334268-f4cd3d80-dffe-11ea-926a-1c83d598dd68.jpeg" width="30%">

___

八卦

<img src="https://user-images.githubusercontent.com/64673363/90336835-061f4580-e011-11ea-817d-c80ae407e48a.jpeg" width="45%"> <img src="https://user-images.githubusercontent.com/64673363/90336844-11727100-e011-11ea-97c7-fabe513745aa.gif" width="45%">

___

心形

<img src="https://user-images.githubusercontent.com/64673363/90337514-98c1e380-e015-11ea-96af-41574cf3f91c.jpeg" width="45%">

___

画别的东西画错了偶然画出来的

<img src="https://user-images.githubusercontent.com/64673363/90412654-f458a380-e0df-11ea-911a-ff4bb3b7719d.jpeg" width="40%">

___

花

<img src="https://user-images.githubusercontent.com/64673363/96329531-7170ac80-1080-11eb-859d-42361fe885dd.jpeg" width="45%">


___

___


###### References:

<div id="refer-1"></div>

[1] [turtle --- 海龟绘图](https://docs.python.org/zh-cn/3/library/turtle.html)
