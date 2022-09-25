# Candidate questions of Socoding 1024 puzzle

## Q1: The Blend-in text "Blend-In"

简介：将字符串隐藏（背景和文字色调相同）在网页中，通过调整背景的颜色凸显文字，获得字符串。

## Examples: Socoding.cn



![image-20220925231845956](./assets/image-20220925231845956.png)

<center>Before</center>



![image-20220925232036142](./assets/image-20220925232036142.png)

<center>After</center>

下面给出CSS代码:

```css
html[lang]::before {
        content: "replace with that magic string";
        font: bold 10%/1 monospace; 
        position: fixed;
        left:100;
        bottom: 0;
        z-index: -1000;
        color: #111111 /* Match the color of the texts w/ background. */
    }
```

之所以在CSS上实现是避免在网页中无脑复制找到答案。

## 题面

> Socoding.cn(前面给出url，告诉答题者具体网页) background-color(这里给出提示，告诉回答者应该改背景色。)

我认为实际可在1024网页的某个位置藏字符串。这样不必再写一个页面，同时更immersive.



## Q2: Color In Hex "Color"

简介：放置多张排成一排的纯色图片(native实现亦可)，答题者通过拾色器得到对应的Hex Code， 按从左到右的顺序连接每个颜色对应的编号作为字符串。

## Examples: France Flag

![Flag_of_France_(1794–1815,_1830–1974,_2020–present)](./assets/Flag_of_France_(1794–1815,_1830–1974,_2020–present).svg)

<center>Contains 3 types of color. Subnautical, White, Blood Orange</center>

从左到右，三种颜色分别为 `#002654 #ffffff #ce1226`

则字符串应该为`011b42ffffffc0001d`

**注意**：

- 有必要规定十六进制颜色代码的格式：从最高位至最低位，分别为RGB. 即 按`#RRGGBB` 而非`#BBGGRR`

- 关于颜色空间，统一为sRGB(非Adobe RGB,P3)，避免拾色结果与标准答案不符。

## 题面

> sRGB in #RRGGBB (这其实提示的十分明显了，可以删一点。)



## Q3: JPG-RAR Merge "Duality"





