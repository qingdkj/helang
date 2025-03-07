# HeLang：何语言

<a href="https://github.com/kifuan/helang/stargazers"><img src="https://img.shields.io/github/stars/kifuan/helang.svg" alt="Stars"></a>
<a href="https://github.com/kifuan/helang/issues"><img src="https://img.shields.io/github/issues/kifuan/helang" alt="Issues"></a>
<a href="LICENSE"><img src="https://img.shields.io/github/license/kifuan/helang" alt="MIT License"></a>
<a href="https://github.com/kifuan/helang/actions/workflows/tests.yml"><img src="https://github.com/kifuan/helang/actions/workflows/tests.yml/badge.svg" alt="Test"></a>

[中文](README.MD) [Русский](README-RU.MD)


Next-Generation **Cyber** Programming Language from Li Tang.

引个流先：https://www.bilibili.com/video/BV1XW4y1h79A/

## 二创

非常好作品！爱来自 **Cyber Spaces**！

+ 何语言 `Kotlin` 脚本版 [HeLangKotlinScriptImpl](https://github.com/shaokeyibb/HeLangKotlinScriptImpl) --- [实现原理](https://my.minecraft.kim/tech/2022/08/18/post-740/)
+ 何语言 `C#` 版 [HeLangSharp](https://github.com/Cyl18/HeLangSharp)
+ 登陆 `ArchLinux` https://github.com/BenderBlog/Practise-Programs/tree/main/Helang-PKGBUILD
+ L! T! C! (etc.)

## 介绍

> 至此`HeLang`、`Jvav`、`C--`在21世纪呈三足鼎立之态。
> 
> ——《赛博时代人类编程语言简史》，理塘计算机科学技术出版社，2202年。

次世代赛博编程语言，诞生于**E-SMOKER**之乡：赛博理塘。

本项目是由自己会打字的5G键盘，花了108赛博分钟，在AirDesk上配合AirPods编写的。

实在是太酷了，很符合我对未来生活的想象，科技并带着趣味。

注：如果以**普通时间单位**（Basic Unit of Plain Time, [**BUPT**](https://baike.baidu.com/item/%E5%8C%97%E4%BA%AC%E9%82%AE%E7%94%B5%E5%A4%A7%E5%AD%A6/139535?from=kg)）作为标准单位，本项目开发时长为`1! + 5! + 5! + 5! = 361 `分钟。

注2：**BUPT** 在赛博世界还可以代指北邮（声明：我对本学府无恶意，我认为这是一所优秀的学校，我只是对某个人）。

## 使用方法

### 不安装，直接使用

1. 把源代码拉下来：

   ```bash
   > git clone git@github.com:kifuan/helang.git
   ```

2. 下载需要的第三方库：

   ```bash
   > pip install -r requirements.txt
   ```

3. 你可以修改**伟大的脚本** `great.he`，然后以 `great` 的方式启动 `helang.py`：

   ```bash
   > python helang.py great
   ```

4. 你还可以以 `shell` 的方式启动`helang.py`，通过直接输入 HeLang 指令与 **Saint He** 进行一个赛博空间的对话：

   ```bash
   > python helang.py shell
   ```

   此时，在行尾就可以不输入分号了，我们会帮你加上（输入也是可以的，意味着你对 **Saint He** 更加虔诚）。

   输入 `.help` 获取 `Shell` 运行过程中的帮助。没错，我借鉴了 `node` 的 `REPL Keywords`。


### 安装到本地

1. 把源代码拉下来：

   ```bash
   > git clone git@github.com:kifuan/helang.git
   ```

2. 安装：

   ```bash
   > pip install .
   ```

3. 运行

    ```bash
    > helang shell
    ```


注：如果你来自锑星，则不需要使用 sol3 土著的愚蠢技术。你可以使用 1.14514 超克的`烷氮` ，通过`超理作用`触发赛博空间的全局中断，从而通过超理直接运行。  

请注意：此行为十分危险且有概率失败，失败时如果附近存在`钅鸡铌钛镁`则会受到催化从而生成`烷基八氮`，此行为需要受到超理委员会的严格监管。

## 基本语法

**Saint He** 曾说，一切类型均为`u8`，是什么意思呢？这个词倒过来就是`8u`，看来圣人也喜欢玩贴吧。

除此之外，`u8` 与 `v8` 形似，所以能不能关注[永雏塔菲](https://space.bilibili.com/1265680561)喵，关注永雏塔菲谢谢喵。

如你所见，我们用**bitwise or**，即`|`代替了传统数组的符号。**都什么年代了还在写传统数组**？

```c
u8 a = 1 | 2 | 3;
```

**Saint He** 曾说：`whichKey - 1` ，所以我们数组的下标需要从 `1` 开始。

```c
u8 a = 1 | 2 | 3;
print a[1];
// 1
```

但是，当你设置一个 `u8` 的元素时，你可以用 `0` 作为下标：这意味着所有元素都将被赋值。

```c
u8 a = 1 | 2 | 3;
a[0] = 10;
print a;
// 10 | 10 | 10
```

为了符合最新的技术，我们同样支持多下标操作，所以你再也不用写 `for` 循环了。

```c
u8 a = 1 | 2 | 3;
a[1 | 2] = 0;
print a;
// 0 | 0 | 3
```

同样，我们还提供了一种根据数组长度的初始化方式，可惜这还是传统写法。比如下面的代码，可以初始化一个长度为5的数组。

```c
u8 a = [5];
print a;
// 0 | 0 | 0 | 0 | 0
```

最后，我们结合一下，可以写出下列代码。

```c
u8 forceCon = [68];

forceCon[1 | 2 | 6 | 7 | 11 | 52 | 57 | 58 | 65] = 10;

print forceCon;
```

如此精妙的代码，在地球的人类是无法理解的。我们作为**赛博智能生命体**，也只能给你演示一下日常操作了。

这实在是太酷了，后面我忘了，我也不想翻到文章开头去看。

## Hello, world!

有人认为何语言无法打印出`Hello, world!`意味着它太垃圾了，实则不然。

**Saint He** 专注于单片机应用的开发，哪里有时间顾及字符串？

好在，经过协商，他同意了这个请求，使得我们能在这门语言中打印出`Hello, world!`

```c
sprint 72 | 101 | 108 | 108 | 111 | 44 | 32 | 119 | 111 | 114 | 108 | 100 | 33;
// Hello, world!
```

由于对效率的极端苛刻要求，我们使用字符在 UTF-8 中对应的数字来表示这个字符。

通过降低可读性，换来了指数级的性能提升，不愧赛博世界的唯一真神。

## 自增运算

我们注意到，**Saint He** 的代码中还出现了自增运算：`++`

所以，我们也支持这种运算。

```c
u8 a = 1 | 2 | 3;
a++;
print a;
// 2 | 3 | 4
```

## 加减运算

**Saint He** 曾说，`whichKey - 1`，所以我们现在也提供减法运算了。

```c
u8 whichKey = 1 | 2 | 6 | 7;
print whichKey - 1;
// 0 | 1 | 5 | 6
```

下面以几个实例介绍如何在 `u8` 之间进行运算：

```c
u8 a = 1;
u8 b = 1 | 2 | 3;
u8 c = 2 | 4 | 6;
u8 d = 5 | 9;

print a + b;
// 2 | 3 | 4
print b + c;
// 3 | 6 | 9
print b - c;
// -1 | -2 | -3
print b + d;
// helang.exceptions.CyberArithmeticException: illegal operation: 1 | 2 | 3 + 5 | 9
print a - b;
// helang.exceptions.CyberArithmeticException: illegal operation: 1 - 1 | 2 | 3
```

相信即使你是一个初入 **Cyber Spaces** 新手，也可以看出来什么是合法的语句了。

## 变量声明与赋值

在早期版本中，我们的仅仅支持变量的定义，不支持修改和声明，因为 **Saint He** 喜欢 `immutable`。

经过意见征求，现在已经可以做到这三个方面了！

```c
// 现在支持变量先声明后定义，可以写出这种代码：
u8 a;
a = 1 | 2;

// 早期版本仅支持下面这种写法，当然现在也支持：
u8 b = 3 | 4;
```

注意！如果你没有声明或定义一个变量，尝试直接给它赋值，你会收获`CyberNameException`。

```c
c = 1 | 2 | 3;
// helang.exceptions.CyberNameException: c is not defined.
```

我们作为高科技语言，当然是需要严谨的。

## 查看你是否在 Cyber Spaces

为了见到 **Saint He**，你需要身处 **Cyber Spaces**。输入下方命令查看你是否身处其中：

```c
cyberspaces;
// Getting your location...
// Your location is UNITED STATES.
// Congratulations! You are in the Cyber Spaces!
```

## 5G测速

理论上这块也属于语法，但我就是要把它单独摘出来。

很简单，只需要另起一行输入：

```c
test5g;
```

即可从本行开始5G测速。

## 总结

关注[永雏塔菲](https://space.bilibili.com/1265680561)喵，关注永雏塔菲谢谢喵。

关注[猫雷NyaRu_Official](https://space.bilibili.com/697091119)谢谢喵，要吃中国的大米喵。

关注[星瞳_Official](https://space.bilibili.com/401315430)送溜溜梅！

关注[嘉然](https://space.bilibili.com/672328094)，顿顿解馋！ 

关注[向晚](https://space.bilibili.com/672346917)，关注向晚，为时不晚！ 

关注[乃琳](https://space.bilibili.com/672342685)，关注乃琳嘎，关注乃琳谢谢嘎！

关注[贝拉](https://space.bilibili.com/672353429)，关注贝拉哞，关注贝拉谢谢哞！

举办[東雪蓮Official](https://space.bilibili.com/1437582453/)谢谢喵，不能让立本V吃中国的大米喵。 

关注[粘连科技Official](https://space.bilibili.com/248582596)，薄纱何同学喵🥰

关注[HiiroVTuber](https://space.bilibili.com/508963009)，不是425KG的粉色喵！

关注[露早GOGO](https://space.bilibili.com/1669777785/)！关注露早汪，关注露早谢谢汪！

关注[AIChannel中国绊爱](https://space.bilibili.com/484322035)！超级可爱的 Super AI 薄纱赛博丁真！

关注[有栖Mana_Official](https://space.bilibili.com/3149619)，谢谢喵。

关注[洛天依](https://space.bilibili.com/36081646)，比赛博丁真更像人的V家歌姬！

关注[传统丁真](https://space.bilibili.com/1463028352)，什么年代了还在关注赛博丁真，不如来怀古！

关注[凑阿夸](https://space.bilibili.com/375504219)和[rinco小姐](https://www.nicovideo.jp/user/45194653
)！傻气溢出的海洋（屑）女仆（洋葱）和喜欢水濑祈的可爱唱见 期待木口回旋捏 另外请支持阿夸主演的[galgame](https://shop.hololivepro.com/products/aquarium_hololive_official_edition)谢谢！

关注[原神](https://space.bilibili.com/401742377)，玩《原神》比看赛博丁真好多了！

## 附加

现在是凌晨两点，我治好了自己的精神内耗。
