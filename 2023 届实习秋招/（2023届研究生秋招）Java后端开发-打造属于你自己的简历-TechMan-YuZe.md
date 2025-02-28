## 打造属于你自己的简历

**作者介绍**

- 作者：TechMan-YuZe

- 邮箱：931624690@qq.com

- 最终去向：阿里  Java 后端开发


在我们准备找实习或者准备秋（春）招时，我们第一步需要做的就是做一份简历。无论我们平时学了多少东西，创造了哪些成绩，我们都需要通过这 1/2 页简历来全部表现自己，毫不夸张地说，简历就是我们的门面。我相信我们每个人都有自己心中理想的简历样式，因此本文主要从我个人找实习以及秋招的经历出发，给出我认识最适合做简历的方式（不一定适合你）。

### 找到适合你的简历制作方式

由于每个人的专业、经历和知识储备都不一样，没有一种方案能适合所有人，大家根据自己的情况自行选择。

#### Word 模板

因为 Word 的简单易用、容易上手等特点，相信大部分人的第一选择都是使用 Word 模板来制作简历。在一开始找实习时，一开始我也是跟大家一样，用超级简历来制作我的简历，虽然超级简历有一个免费简历模板的额度，但我相信这远远是不够的，我们在投递不同的公司时肯定不能都只用一份简历进行投递，需要对不同公司不同岗位的需求进行微调，因此使用超级简历等类 Word 模板在线简历制作工具，缺点就是很多功能需要会员，这点是我不能忍受的。当然你不介意付费，那当我没说😝。

![image-20221126204213509](https://images-yuze.oss-cn-hangzhou.aliyuncs.com/img/202211262042541.png)

第二种方式就是使用本地的 Word 模板。虽这样你的简历份数都不受限制了，但当你想按照你自己的理想的简历样式去更改 Word 模板时，你会发现，Word 模板的自由度极低，**这就是我为什么不喜欢使用 Word 模板来制作简历的最大原因，你无法通过代码随心所欲的控制所有效果**。



#### LaTex模板

LaTex 相比于 Word，很大的一个优势就是作为内容编辑者的我们无需关注简历的排版，让我们只需要关注简历的内容本身。与 Word 的问题一样，当你想实现你自己的理想的简历样式时，如果你对 LaTex 的模板机制不熟悉，你根本无从下手，这与学习 LaTex 如何写公式和制作表格完全不同，你需要做的是去修改样式源文件。

推荐一个 LaTex 简历模板：https://github.com/billryan/resume/tree/zh_CN



#### 在线 Markdown 简历制作

对使用前两者方式制作简历得过程和效果不满意后，我最终还是决定使用 Markdown 来制作我的简历，Markdown 我相信是绝大部分接触过编程人首选的文本编辑方式。目前我使用过最好的在线 Markdown 简历制作工具就是 [**木及简历**](https://www.mujicv.com/)**。**

![image-20221126204608731](https://images-yuze.oss-cn-hangzhou.aliyuncs.com/img/202211262046878.png)

推荐使用木及简历有以下这么几个原因：

1. 支持本地导入 md 文件创建简历

   ![image-20221126205252742](https://images-yuze.oss-cn-hangzhou.aliyuncs.com/img/202211262052823.png)

2. 模板丰富

3. 支持常见的衬线字体（Times New Roman 和思源宋体）和无衬线字体（苹方、思源黑体和阿里巴巴普惠体）

   ![image-20221126204655905](https://images-yuze.oss-cn-hangzhou.aliyuncs.com/img/202211262046933.png)

4. 支持矢量图标，让你的简历更加灵动

   ![image-20221126204732705](https://images-yuze.oss-cn-hangzhou.aliyuncs.com/img/202211262047790.png)

5. 智能一页（内容太多无法一页）

6. 支持 CSS 自定义样式（这点是最重要的，能够通过代码随心所欲的控制简历的样式，这也是我后续决定自己制作 Typora 主题的主要原因）

7. 支出导出 md 文件

8. 支持行内代码块（技术选型可以用来写技术栈，这点是 Word 和 LaTex 很难做到的）

**木及简历对绝大部分的人来说绝对够用了，但它也存在一些问题：**

1. **无法设置导出 PDF 的页面大小（默认是 A4 纸）**
2. **导出 PDF 时，无法设置页边距（这点在你的个人信息一行放不下时很重要）**
3. **所支持的字体有限（虽说够用，但不能设置自己想要的字体）**



#### 终极方案：Typora 主题（TechMan Resume Theme）

基于木及简历目前存在的问题以及我个人比较喜欢通过 CSS 代码来实现样式，我决定自己制作一个 Markdown 主题满足自己的需求。同时，到目前为止，这是我觉得最适合我自己的简历制作方式。

目前支持自定义 Markdown 主题的写作软件也很多，如 Typora、Obsidian 等，但 Typora 支持设置导出 PDF 页面大小和页边距是我选择它的原因，Typora 支持设置导出 PDF 页面大小和页边距的意义在于你可以导出一页很长的 PDF 从而达到所谓“简历不能超过一页”的需求，同时也能避免因为分页引发的很多问题。

![image-20221126205439069](https://images-yuze.oss-cn-hangzhou.aliyuncs.com/img/202211262054257.png)

同时 Typora 也支持自定义导出 PDF 的样式（有些 Markdown 写作软件只支持自定义预览样式，但不支持自定义导出 PDF 的样式，这就会出现你预览的时候是你想要的效果，但导出后却完全变了），只要在主题样式文件下面新增 `@media print` 样式，在其内部填入预览样式即可。

```CSS
@media print {
  .typora-export * {
      -webkit-print-color-adjust: exact;
  }
  /* 你自己的样式 */
}
```

**我心里理想的简历样式：**

1. **名字是宋体、楷体衬线字体**
2. **个人信息统一对齐**
3. **二级标题蓝色字体，背景浅蓝色，同时文本与左边界有一定的距离**
4. **技术选型使用行内代码块描述，同时行内代码块使用等宽字体**
5. **除名字和行内代码块字体外，其余统一使用同一种衬线或者无衬线字体族**

于是按照我理想的简历样式，便有了以下 TechMan Resume Theme 的效果（示例正文使用苹方字体）：

![image-20221126205609399](https://images-yuze.oss-cn-hangzhou.aliyuncs.com/img/202211262056513.png)



### TechMan Resume Theme 的使用方法

1. 安装 Typora（如果没有）

2. 下载主题压缩包（包含 CSS 主题文件以及主题所需要的字体文件）

   1. GitHub：https://github.com/TechMan-YuZe/TechMan-Resume-Theme
   2. Gitee：https://gitee.com/techman_yuze/tech-man-resume-theme
   3. 阿里云盘：https://www.aliyundrive.com/s/DYVFqshgWvU

3. 将相应的 CSS 文件和字体文件夹移动到 Typora 的主题目录下（找不到目录的可以从 Typora 的 **偏好设置 → 外观 → 打开主题文件夹** 打开相应的文件夹

   ![image-20221126205707708](https://images-yuze.oss-cn-hangzhou.aliyuncs.com/img/202211262057867.png)

   ![](https://images-yuze.oss-cn-hangzhou.aliyuncs.com/img/202211262057367.png)

4. 重启 Typora，从主题选择 TechMan Resume 即可（TechMan Resume 是无衬线字体版、TechMan Resume Serif 是衬线字体版）

   

### 基于 TechMan Resume Theme 实现你理想的简历样式

按照 CSS 文件中的注释修改你喜欢的样式即可