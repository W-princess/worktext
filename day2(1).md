# 一、HTML常见的元素

## 1.HTML结构分析

一个完整的HTML结构
```HTML
<!-- 文档（类型）声明 -->
<!DOCTYPE html>
<!-- 根元素 编写文档的配置信息 -->
<html lang="en">
</html>
<!-- 元数据 -->
  <head>
  <!-- 字符编码 -->
    <meta charset="UTF-8">
  <!-- 网页的标题 -->
    <title>Document</title>
  </head>
  <body>
  
  </body>
</html>
```

---
- `<!DOCTYPE html>`
  - HTML 文档声明，告诉浏览器当前页面是 HTML5 页面；
  -  让浏览器用 HTML5 的标准去解析识别内容；
  -  必须放在 HTML 文档的最前面，不能省略，省略了会出现兼容性问题。

---

- `<html>`
  - 表示一个HTML文档的根；
  - 有其他元素必须是此元素的后代。

- lang属性
  - 帮助翻译工具确定翻译规则
  -  帮助语音合成工具确定发音
```HTML
 <html lang="zh-CN">
 <!--简体中文-->
  </html>
 <html lang="en">
  <!--英文-->
```

---
- `<head>`
    -  规定文档相关的**配置信息**（标题，文档样式，脚本）
    
- `<meta charset="utf-8">`
    - 设置**字符编码**，不设置或者设置错误会导致乱码
    -  一般使用utf-8编码

- `<title>`
  - 网页的标题

---

- `<body>`
  - 网页的具体内容和结构，浏览器窗口中显示的部分

---

![HTML元素](https://img.onmicrosoft.cn/2022/12/14/74232fc0-2af7-402c-bb23-3af376de1b6f.png)

## 2.h1~h6,p元素

- h元素
    -  `<header>`元素通常用来做标题。
    -  `<h1>`级别最高， `<h6>`级别最低。
       <!--浏览器通过css样式区分h1~h6-->
      ![](https://img.onmicrosoft.cn/2022/12/14/521e8928-8070-4762-9f20-e122c0420133.png)

---

- p元素
  - p元素(paragraph)，段落；分段。
  - p元素在多个段落之间有一定的间距。
      <!--长段文字建议代码和文字分行写，增加可读性。-->
    ![](https://img.onmicrosoft.cn/2022/12/14/00f69305-b447-48e2-812b-0d31ac3b5e21.png)

---

## 3.img，a元素

- img元素
  - `<img>`(image)，指图像。
  - `<img>` 是一个可替换元素 (replaced element);
  
- `<img>`元素有两个常见的属性:
  - src 属性 :source 单词的缩写，表示源
    - 它包含了你想嵌入的图片的文件路径。
    
      - 网络图片：一个 URL 地址 (后续会专门讲 URL);
    
      - 本地图片：本地电脑上的图片，后续会和 html 一起部署到服务
    ![](https://img.onmicrosoft.cn/2022/12/14/be92937e-01cd-4f1f-9313-8f72370b3e6a.png)
    
  - alt 属性：不是强制性的，有两个作用
    - 当图片加载不成功 (错误的地址或者图片资源不存在)，那么会显示这段文本；
    - 屏幕阅读器会将这些描述读给需要使用阅读器的使用者听，让他们知道图像的含义；

---

- a元素
  - 在网页中我们经常需要**跳转到另外一个链接**，这个时候我们使用 **a 元素** ;
  - **HTML `<a>` ** 元素 (或称锚 (anchor) 元素):
    - 定义 超链接，用于打开新的 URL;
- a 元素有两个常见的属性:
    - href:Hypertext Reference 的简称
      - 指定要打开的 URL 地址；
      - 也可以是一个本地地址；
    - target: 该属性指定在何处显示链接的资源。
      - _self: 默认值，在当前窗口打开 URL;
      - _blank: 在一个新的窗口中打开 URL;
      - _parent：在父窗口中打开URL;
      - _top：在顶层窗口中打开URL;

---

- iframe元素

    利用iframe元素可以实现：在一个HTML文档中嵌入其他HTML文档

- frame-border属性：用于规定是否显示边框
  - 1：显示 
  - 0：不显示

---

## 4.div，span元素

- div 元素

  多个 div 元素包裹的内容会在不同的行显示；

  - 一般作为其他元素的父容器，把其他元素包住，代表一个整体
  - 用于把网页分割为多个独立的部分

---

- span 元素

  多个 span 元素包裹的内容会在同一行显示；

  - 默认情况下，跟普通文本几乎没差别
  
  - 用于区分特殊文本和普通文本，比如用来显示一些关键字
  
---

## 5.不常用元素

- **strong 元素** : 内容加粗、强调；
  - 通常加粗会使用 css 样式来完成；
  - 开发中很偶尔会使用一下；
  
- *i 元素* : 内容倾斜；
  - 通常斜体会使用 css 样式来完成；
  - 开发中偶尔会用它来做字体图标 (因为看起来像是 icon 的缩写);
  
- `code元素` : 用于显示代码
  - 偶尔会使用用来显示等宽字体；
  
- `br元素` : 换行元素

---

## 6.HTML全局属性

- 我们发现**某些属性只能设置在特定的元素**中:
  - 比如 img 元素的 `src`、a 元素的 `href`;
  
- 也有一些属性是所有 HTML 都可以设置和拥有的，这样的属性我们称之为 “全局属性 (Global Attributes)”

---

- **常见的全局属性如下:**
  - `id` : 定义唯一标识符 (ID)，该标识符在整个文档中必须是唯一的。其目的是在链接 (使用片段标识符)，脚本或样 式 (使用 CSS) 时标识元素。
  - `class` : 一个以空格分隔的元素的类名 (classes) 列表，它允许 CSS 和 Javascript 通过类选择器或者 DOM 方法来选 择和访问特定的元素；
  - `style` : 给元素添加内联样式；
  - `title` : 包含表示与其所属元素相关信息的文本。 这些信息通常可以作为提示呈现给用户，但不是必须的。

---

# 二、额外知识补充

## 1.字符实体

- HTML实体是一段以**连字号（&）开头、以分号（**
  **;）结尾的文本**（字符串）：

  - 实体常常用于显示保留字符（这些字符会被解析为 HTML 代码）和不可见的字符（如“不换行空格”）；

  - 你也可以用实体来代替其他难以用标准键盘键入的字符。

---

- **常见的字符实体**

|      |描述|实体名称|实体编号|
| ---: | :--: | :--- | :--- |
| |空格| `&nbsp;`|`&#160;`|
|<|小于号|`&lt;`|`&#60;`|
|>|大于号|`&gt;`|`&#62;`|
|&|和号|`&amp;`|`&#38;`|
|"|双引号|`&quot;`|`&#34;`|
|'|单引号|`&apos;`|`&#39;`|
|￠|分(cent)|`&cent;`|`&#162;`|
|£|镑(pound)|`&pound;`| `&#163;`|
|¥|元(yen)|`&yen;`|`&#165;`|
|€|欧元(euro)|`&euro;`|`&#8364;`|
|§|小节|`&sect;`|`&#167;`|
|©|版权(copyright)|`&copy;`|`&#169;`|
|®|注册商标|`&reg;`|`&#174;`|
|™|商标|`&trade;`|`&#8482;`|
|×|乘号|`&times;`|`&#215;`|
|÷|除号|`&divide;`|`&#247;`|

## 2.URL地址

-  **URL 代表着是统一资源定位符（***Uniform Resource Locator***）**
  - 理论上说，每个有效的 URL 都指向一个唯一的资源；
  - 这个资源可以是一个 HTML 页面，一个 CSS 文档，一幅图像，等等；
>- **标准格式**：
> `[协议类型]://[服务器地址]:[端口号]/[文件路径][文件名]?[查询]#[片段ID]`

![](https://img.onmicrosoft.cn/2022/12/14/5b47d593-8fe7-4555-ac62-8af1b6c7d387.png)

---

## 3.元素语义化

- 元素的语义化：用正确的元素做正确的事情。
- 理论上来说，所有的 HTML 元素，我们都能实现相同的事情:
- 标签语义化的好处

  - 方便代码维护；

  - 减少让开发者之间的沟通成本；

  - 能让语音合成工具正确识别网页元素的用途，以便作出正确的反应；

## 4.SEO优化

- **搜索引擎优化**（英语：search engine optimization，缩写为SEO）是通过了解搜索引擎的运作规则来调整网站，以及提高网站在有关搜索引擎内排名的方式。

  [![img](https://img.onmicrosoft.cn/2022/12/13/f1894225-2f29-49ed-8199-62c6b0f9546a.png)](https://img.onmicrosoft.cn/2022/12/13/f1894225-2f29-49ed-8199-62c6b0f9546a.png)

## 5.字符编码

- 计算机是干什么的？
  - 计算机一开始发明出来时是用来解决数字计算问题的，后来人们发现，计算机还可以做更多的事，例如文本处理。
  - 但计算机其实挺笨的，它只 “认识” 010110111000… 这样由 0 和 1 两个数字组成的二进制数字；
  - 这是因为计算机的底层硬件实现就是用电路的开和闭两种状态来表示 0 和 1 两个数字的。
  - 因此，计算机只可以直接存储和处理二进制数字。
- 为了在计算机上也**能表示、存储和处理像文字、符号等等之类的字符**，就必须将这些**字符转换成二进制**数字。
  - 当然，肯定不是我们想怎么转换就怎么转换，否则就会造成同一段二进制数字在不同计算机上显示出来的字符不一样的情况，因此必须得定一个统一的、标准的转换规则
- 字符编码的发展历史可以阅读我的简书一篇文章:https://www.jianshu.com/p/899e749be47c

[![img](https://img.onmicrosoft.cn/2022/12/13/b78e0f0e-74cb-4503-9b54-7e4319ec038f.png)](https://img.onmicrosoft.cn/2022/12/13/b78e0f0e-74cb-4503-9b54-7e4319ec038f.png)

---
>输入法设置：中文时使用英文标点。
><!--提高编写效率。-->

---