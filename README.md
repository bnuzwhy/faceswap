# deepfakes_faceswap
<p align="center">
  <a href="https://faceswap.dev"><img src="https://i.imgur.com/zHvjHnb.png"></img></a>
<br />FaceSwap is a tool that utilizes deep learning to recognize and swap faces in pictures and videos.
</p>

![Screenshots](https://i.imgur.com/nWHFLDf.jpg)

<p align="center">
  <a href="https://www.youtube.com/watch?v=r1jng79a5xc"><img src="https://img.youtube.com/vi/r1jng79a5xc/0.jpg"></img></a>
<br />Jennifer Lawrence/Steve Buscemi FaceSwap using the Villain model
</p>

Make sure you check out [INSTALL.md](INSTALL.md) before getting started.

- [deepfakes_faceswap](#deepfakesfaceswap)
- [Manifesto](#Manifesto)
  - [FaceSwap has ethical uses.](#FaceSwap-has-ethical-uses)
- [How To setup and run the project](#How-To-setup-and-run-the-project)
- [Overview](#Overview)
  - [Extract](#Extract)
  - [Train](#Train)
  - [Convert](#Convert)
  - [GUI](#GUI)
- [General notes:](#General-notes)
- [Help I need support!](#Help-I-need-support)
  - [Discord Server](#Discord-Server)
  - [FaceSwap Forum](#FaceSwap-Forum)
- [Donate](#Donate)
  - [@torzdf](#torzdf)
  - [@andenixa](#andenixa)
  - [@kvrooman](#kvrooman)
- [How to contribute](#How-to-contribute)
  - [For people interested in the generative models](#For-people-interested-in-the-generative-models)
  - [For devs](#For-devs)
  - [For non-dev advanced users](#For-non-dev-advanced-users)
  - [For end-users](#For-end-users)
  - [For haters](#For-haters)
- [About github.com/deepfakes](#About-githubcomdeepfakes)
  - [What is this repo?](#What-is-this-repo)
  - [Why this repo?](#Why-this-repo)
  - [Why is it named 'deepfakes' if it is not /u/deepfakes?](#Why-is-it-named-deepfakes-if-it-is-not-udeepfakes)
  - [What if /u/deepfakes feels bad about that?](#What-if-udeepfakes-feels-bad-about-that)
- [About machine learning](#About-machine-learning)
  - [How does a computer know how to recognize/shape faces? How does machine learning work? What is a neural network?](#How-does-a-computer-know-how-to-recognizeshape-faces-How-does-machine-learning-work-What-is-a-neural-network)

# Manifesto

## FaceSwap has ethical uses.

When faceswapping was first developed and published, the technology was groundbreaking, it was a huge step in AI development. It was also completely ignored outside of academia because the code was confusing and fragmentary. It required a thorough understanding of complicated AI techniques and took a lot of effort to figure it out. Until one individual brought it together into a single, cohesive collection. It ran, it worked, and as is so often the way with new technology emerging on the internet, it was immediately used to create inappropriate content. Despite the inappropriate uses the software was given originally, it was the first AI code that anyone could download, run and learn by experimentation without having a Ph.D. in math, computer theory, psychology, and more. Before "deepfakes" these techniques were like black magic, only practiced by those who could understand all of the inner workings as described in esoteric and endlessly complicated books and papers.

"Deepfakes" changed all that and anyone could participate in AI development. To us, developers, the release of this code opened up a fantastic learning opportunity. It allowed us to build on ideas developed by others, collaborate with a variety of skilled coders, experiment with AI whilst learning new skills and ultimately contribute towards an emerging technology which will only see more mainstream use as it progresses.

Are there some out there doing horrible things with similar software? Yes. And because of this, the developers have been following strict ethical standards. Many of us don't even use it to create videos, we just tinker with the code to see what it does. Sadly, the media concentrates only on the unethical uses of this software. That is, unfortunately, the nature of how it was first exposed to the public, but it is not representative of why it was created, how we use it now, or what we see in its future. Like any technology, it can be used for good or it can be abused. It is our intention to develop FaceSwap in a way that its potential for abuse is minimized whilst maximizing its potential as a tool for learning, experimenting and, yes, for legitimate faceswapping.

We are not trying to denigrate celebrities or to demean anyone. We are programmers, we are engineers, we are Hollywood VFX artists, we are activists, we are hobbyists, we are human beings. To this end, we feel that it's time to come out with a standard statement of what this software is and isn't as far as us developers are concerned.

- FaceSwap is not for creating inappropriate content.
- FaceSwap is not for changing faces without consent or with the intent of hiding its use.
- FaceSwap is not for any illicit, unethical, or questionable purposes.
- FaceSwap exists to experiment and discover AI techniques, for social or political commentary, for movies, and for any number of ethical and reasonable uses.

We are very troubled by the fact that FaceSwap can be used for unethical and disreputable things. However, we support the development of tools and techniques that can be used ethically as well as provide education and experience in AI for anyone who wants to learn it hands-on. We will take a zero tolerance approach to anyone using this software for any unethical purposes and will actively discourage any such uses.

# How To setup and run the project
FaceSwap is a Python program that will run on multiple Operating Systems including Windows, Linux, and MacOS.

See [INSTALL.md](INSTALL.md) for full installation instructions. You will need a modern GPU with CUDA support for best performance. AMD GPUs are partially supported.

# Overview
The project has multiple entry points. You will have to:
 - Gather photos and/or videos
 - **Extract** faces from your raw photos
 - **Train** a model on the faces extracted from the photos/videos
 - **Convert** your sources with the model

Check out [USAGE.md](USAGE.md) for more detailed instructions.

## Extract
From your setup folder, run `python faceswap.py extract`. This will take photos from `src` folder and extract faces into `extract` folder.

## Train
From your setup folder, run `python faceswap.py train`. This will take photos from two folders containing pictures of both faces and train a model that will be saved inside the `models` folder.

## Convert
From your setup folder, run `python faceswap.py convert`. This will take photos from `original` folder and apply new faces into `modified` folder.

## GUI
Alternatively, you can run the GUI by running `python faceswap.py gui`

# General notes:
- All of the scripts mentioned have `-h`/`--help` options with arguments that they will accept. You're smart, you can figure out how this works, right?!

NB: there is a conversion tool for video. This can be accessed by running `python tools.py effmpeg -h`. Alternatively, you can use [ffmpeg](https://www.ffmpeg.org) to convert video into photos, process images, and convert images back to the video.


**Some tips:**

Reusing existing models will train much faster than starting from nothing.
If there is not enough training data, start with someone who looks similar, then switch the data.

# Help I need support!
## Discord Server
Your best bet is to join the [FaceSwap Discord server](https://discord.gg/FC54sYg) where there are plenty of users willing to help. Please note that, like this repo, this is a SFW Server!

## FaceSwap Forum
Alternatively, you can post questions in the [FaceSwap Forum](https://faceswap.dev/forum). Please do not post general support questions in this repo as they are liable to be deleted without response.

# Donate
The developers work tirelessly to improve and develop FaceSwap. Many hours have been put in to provide the software as it is today, but this is an extremely time-consuming process with no financial reward. If you enjoy using the software, please consider donating to the devs, so they can spend more time implementing improvements.

## @torzdf
 There is very little FaceSwap code that hasn't been touched by torzdf. He is responsible for implementing the GUI, FAN aligner, MTCNN detector and porting the Villain, DFL-H128 and DFaker models to FaceSwap, as well as significantly improving many areas of the code.

**Bitcoin:** 385a1r9tyZpt5LyZcNk1FALTxC8ZHta7yq

**Ethereum:** 0x18CBbff5fA7C78de7B949A2b0160A0d1bd649f80

**Paypal:** [![torzdf](https://www.paypalobjects.com/en_GB/i/btn/btn_donate_SM.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=JZ8PP3YE9J62L)

## @andenixa
Creator of the Unbalanced and OHR models, as well as expanding various capabilities within the training process. Andenixa is currently working on new models and will take requests for donations.

**Paypal:** [![andenixa](https://www.paypalobjects.com/en_GB/i/btn/btn_donate_SM.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=NRVLQYGS6NWTU)

## @kvrooman
Responsible for consolidating the converters, adding a lot of code to fix model stability issues, and helping significantly towards making the training process more modular, kvrooman continues to be a very active contributor.

**Ethereum:** 0x18CBbff5fA7C78de7B949A2b0160A0d1bd649f80

# How to contribute

## For people interested in the generative models
 - Go to the 'faceswap-model' to discuss/suggest/commit alternatives to the current algorithm.

## For devs
 - Read this README entirely
 - Fork the repo
 - Play with it
 - Check issues with the 'dev' tag
 - For devs more interested in computer vision and openCV, look at issues with the 'opencv' tag. Also feel free to add your own alternatives/improvements

## For non-dev advanced users
 - Read this README entirely
 - Clone the repo
 - Play with it
 - Check issues with the 'advuser' tag
 - Also go to the '[faceswap Forum](https://faceswap.dev/forum)' and help others.

## For end-users
 - Get the code here and play with it if you can
 - You can also go to the [faceswap Forum](https://faceswap.dev/forum) and help or get help from others.
 - Be patient. This is a relatively new technology for developers as well. Much effort is already being put into making this program easy to use for the average user. It just takes time!
 - **Notice** Any issue related to running the code has to be opened in the [faceswap Forum](https://faceswap.dev/forum)!

## For haters
Sorry, no time for that.

# About github.com/deepfakes

## What is this repo?
It is a community repository for active users.

## Why this repo?
The joshua-wu repo seems not active. Simple bugs like missing _http://_ in front of urls have not been solved since days.

## Why is it named 'deepfakes' if it is not /u/deepfakes?
 1. Because a typosquat would have happened sooner or later as project grows
 2. Because we wanted to recognize the original author
 3. Because it will better federate contributors and users

## What if /u/deepfakes feels bad about that?
This is a friendly typosquat, and it is fully dedicated to the project. If /u/deepfakes wants to take over this repo/user and drive the project, he is welcomed to do so (Raise an issue, and he will be contacted on Reddit). Please do not send /u/deepfakes messages for help with the code you find here.

# About machine learning

## How does a computer know how to recognize/shape faces? How does machine learning work? What is a neural network?
It's complicated. Here's a good video that makes the process understandable:
[![How Machines Learn](https://img.youtube.com/vi/R9OHn5ZF4Uo/0.jpg)](https://www.youtube.com/watch?v=R9OHn5ZF4Uo)

Here's a slightly more in depth video that tries to explain the basic functioning of a neural network:
[![How Machines Learn](https://img.youtube.com/vi/aircAruvnKk/0.jpg)](https://www.youtube.com/watch?v=aircAruvnKk)

tl;dr: training data + trial and error

2017年12月，一个名为“DeepFakes”的用户在Reddit上发布了一个“假视频”，视频中的艺人其实是后期加上的，但是看起来几乎毫无破绽。他利用了深度学习和AI新技术，在成人电影中把演员的脸替换成某个艺人的脸，从而制作成了这个看上去以假乱真的视频。

从视频发布以后的好几个星期，网络上不断有人发表文章和报道，抨击这一“换脸”技术，称这种技术将会对社会产生很多负面的影响。比如说，这个“换脸”技术会给很多无辜清白的人（像那些无故出现在成人电影中的艺人）造成困扰；“假视频”会加剧虚假新闻的散播，进而将大大损坏视频作为证据的可信度。

确实，心怀不轨的人会利用这项技术做危害社会的事情。但是我们不能够因此完全否定这项技术的价值，我们应该好好思考，如何把它用上正道，发挥它的积极作用。

所以，在这篇文章中，我将会介绍这项AI换脸技术的功能和原理，并且阐述其有发展前途的应用领域。

首先我们要先清楚什么是DeepFakes？它能够做什么？

什么是DeepFakes？

DeepFakes实际上是一种人脸交换技术，顾名思义，也就是在图像或视频中把一张脸替换成另一张脸。事实上，人脸交换技术在电影制作领域已经不是个新鲜词了，但是之前电影视频中的人脸交换非常复杂，专业的视频剪辑师和CGI专家需要花费大量时间和精力才能完成视频中的人脸交换。

DeepFakes的出现可以说是人脸交换技术的一个突破。利用DeepFakes技术，你只需要一个GPU和一些训练数据，就能够制作出以假乱真的换脸视频。

这可以说是一个非常了不起的突破了，因为你只需要把上百张人物的样图输入至一个算法，就能完成人脸交换，制作出非常逼真的视频效果。就算你是个对视频剪辑一窍不通的外行，也能做到这样。

DeepFakes的出现还意味着我们可以在视频中进行大规模的“换脸”。我们大多数人都曾经把自己的照片上传到网络上，因此，我们大多数人的脸都能够轻易地被替换到一些视频中，成为视频的“主角”。不得不说，这是件非常可怕的事情，但这也并不那么值得恐慌，毕竟我们大家早已接受了“照骗”（照片造假）。

“面部定制”已经不是什么新鲜事了：在《星球大战》中，CGI（计算机图像生成）技术根据一名女演员的脸塑造了年轻时期的Carrie Fisher的形象。女演员脸上的点是用来进行精准的面部绘制的。，

DeepFakes能够让你在没有任何技巧的情况下完成这样的“面部定制”，但DeepFakes可不是“面部定制”。

DeepFakes究竟能做些什么？

在讨论如何使用DeepFakes之前，我想先解决这样的问题：DeepFakes究竟能够做些什么？它的技术原理是什么？

为了了解其工作原理，我选了Jimmy Fallon和John Oliver主持的节目视频作为分析案例。Jimmy Fallon和John Oliver是两位非常受欢迎的晚间节目主持人，网络上有大量他们的节目视频。这些视频的亮度变化差不多，主持人在视频中的动作和姿势也很相似，这些相似性有利于降低分析的受干扰程度。但视频同时又存在大量的变化（例如主持人嘴唇的变化），这样又能够保证分析的趣味性。

很幸运，我找到了一个包含了原始DeepFakes编码和很多DeepFakes改进版编码的GitHub。这个GitHub使用起来相当简单，但是目前还处于训练数据收集和准备的阶段。

为了让我们的分析实验更简单，我写了一个能够直接在YouTube视频上运行的脚本，这样一来，数据的收集和预处理工作就变得轻松多了，视频转换也只需一步就能完成。点击此处查看我的GitHub报告，看看我是如何轻松地制作下面这个视频的（我还分享了我的模型数据）。

简单来说，这个脚本需要你给需要进行人脸交换的人各自准备一个YouTube视频集，然后运行命令来对视频进行预处理（从YouTube下载视频、提取各个视频的帧、找出视频中的人脸）和训练，并将其转换为音频和可调整大小的选项等。

从Jimmy Fallon到John Oliver的“换脸”结果

下面的视频是经过了大约30000张（Jimmy和Oliver每人各约15000张）图片的模型训练制作完成的，我从6-8个时长分别在3-5分钟的YouTube视频中过滤掉了那些不含Jimmy和Oliver的脸的帧，留下了含有他们的脸的一些帧——每个视频每秒大约20帧。以上这些操作全部都是自动完成的，我只是提供了一个YouTube视频集。

在NVIDIA GTX 1080 TI的GPU上训练的总时长大约是72小时。训练时间主要与训练的GPU有关，而下载视频并将其划分成帧的时间与I/O相关，这两步是可以同时进行的。

尽管我截取到的Jimmy和Oliver的人脸图片有几万张，但是达成完美的人脸交换大概只需300张图片。我选择“视频截人脸”的方式是因为，视频中出现的人脸很多，从视频中截取人脸图片非常方便，但如果在网上找这么多人脸图片可就麻烦得多了。

为了避免GIF动画的文件过大，下面的这张图片被设置成了低分辨率。下面的YouTube视频分辨率更高、声音更大。

&utm_medium=embed&utm_campaign=Embeds&utm_term=https%3A%2F%2Fwww.kdnuggets.com%2F2018%2F03%2Fexploring-deepfakes.html

视频中的Oliver正在演唱Iggy Azalea的《fancy》，视频中虽然有麦克风的干扰，但算法最后呈现的效果还算不错。

&utm_medium=embed&utm_campaign=Embeds&utm_term=https%3A%2F%2Fwww.kdnuggets.com%2F2018%2F03%2Fexploring-deepfakes.html

这个视频是Oliver正在主持“吉米秀”（Jimmy主持的晚间节目）。我们发现视频中Oliver的脸上多了一副眼镜，但他的头发和脸型基本没有影响，整个视频看上去非常自然和谐，几乎看不出换脸的痕迹。

到目前为止，DeepFakes还没到完美的程度，但其呈现出的效果已经相当令人满意了。关键是我事先并没有对视频做过任何改动，全是算法的功劳——算法通过观察大量的图片数据，学会制作出这样以假乱真的换脸视频。你一定也觉得非常神奇吧？那么接下来，让我们一起看看DeepFakes究竟是怎么做到的。

DeepFakes的技术原理

DeepFakes的核心是一个“自动编码器”，这个“自动编码器”实际上是一个深度神经网络，它能够接收数据输入，并将其压缩成一个小的编码，然后从这个编码中重新生成原始的输入数据。

在这个标准的自动编码器设置中，网络将尝试学习创建一个编码，从中网络能够重新生成输入的原始图片。只要有足够多的图像数据，网络就能学会创建这种编码。

DeepFakes让一个编码器把一个人脸压缩成一个代码和两个解码器，一个将其还原成人物A（Fallon），另一个还原成人物B（Oliver）。下面的图能够帮助你理解：

在这个案例中，使用的编码器是一样的，但是Fallon和Oliver的解码器是不同的。在训练的过程中，输入的人脸会被扭曲，从而模拟一个“我们希望得到这样的人脸”的概念。

下面我将介绍算法训练的三个步骤：

1. 首先，我们给编码器输入了一张Jimmy扭曲脸的图片，并尝试用解码器A来重新还原他的脸，这就使得解码器A必须要学会在纷繁复杂的图片中识别并且还原出Jimmy的脸。

2. 然后，把Oliver扭曲脸的图片输入至同一个编码器，并用解码器B来还原Oliver的脸。

3. 我们不断重复上面的操作，直到两个解码器能够分别还原出两个人的脸，同时编码器也能够学会通过抓取人脸关键信息，从而分辨出Jimmy和Oliver的脸。

等到以上的训练步骤都完成以后，我们就能把一张Jimmy的照片输入至编码器，然后直接把代码传输至解码器B，将Jimmy的脸换成Oliver的脸。

这就是我们通过训练模型完成换脸的全过程。解码器获取了Jimmy的脸部信息，然后把信息交给解码器B，这时候解码器B会作出这样的反应：“这又是一条干扰信息，这不是Oliver的脸，那么我就把你换成Oliver吧。”

一条算法仅通过观察许多图片就能够再次生成、还原这些图片，这听起来挺不可思议的，但DeepFakes确确实实做到了，而且效果还相当不错。
