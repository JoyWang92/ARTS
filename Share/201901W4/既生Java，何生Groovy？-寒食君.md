# 既生Java，何生Groovy？

这周接手了组里一个旧项目，javadoc显示是从2017年开始编写的。@author显示是一位前端员工的名字，他在我入职前已离职，好像是去了腾讯。

我十分好奇，为什么前端人员的名字会出现在后台代码里？问了下X叔，告知可能是当时该同学正在转后端，然后人手不够，就由他来写了。

上面都是题外话。

项目是用groovy写的，我之前没有接触过groovy，但是作为和java一样运行在jvm上的语言，阅读二者代码不会有障碍。在格式方面groovy提供了更多的语法糖，让开发者能够更加愉悦地编写。

但是作为维护者，则恰恰相反。比如，groovy用到了动态类型，这对于维护者阅读理解和调试都增加了一定的难度。

下面我想从两方面谈起，一是既生java，何生groovy？二者有什么区别？二是在开发前，关于语言选型的问题。

Java自1995年诞生以来，遇到过几次重大波折，但都一一化解，并且一路高歌猛进，成为当前具有不二地位的老大哥。那么既然老大哥有着众多拥趸，那么千秋万代，岂不美哉？

但是，有人的地方就有江湖，语言也是，尤其以PHP信徒最为猖獗，这是后话。

groovy诞生于2004年，是一种JVM上的替代语言，这里的替代不能理解为取代，而是一种对原有语言的完善和补充。所以说，groovy的诞生不是为了革命，而是一种改良。

groovy的语法与java很相似，基本上只要你会java，你就能读懂groovy。但是其理念是源于smalltalk和ruby，所以groovy更像是一门胶水语言。

groovy最大的特点是支持动态类型，相较于java，它更简洁，表达能力也更强，具体特性可以搜索了解，这里暂不赘述。短期来看，它可以缩短你的开发周期，提升你的效率，但是长期来看，可能会导致一些问题，比如我现在维护就很吃力，一部分原因也是因为我菜。

那么大家可能会萌生这样一个问题：对于这二者，在开发时如何选用呢？

首先是技术选型，这是架构师的任务，学问比较高深。而我们作为个人开发者或者是初级工程师，没有达到这样的技术视野。所以在开发除工作以外的自己的小项目时，可以尽量去自我培养这一种能力。在语言选型上，有人说，超过200行代码的项目都不应该使用动态类型，虽然有一点夸张，但是有一些道理的，俗话说：“动态类型一时爽，代码重构火葬场”。

我认为，对于个人开发或者2-3人小团队合作，而且不用长期维护的项目，写法自由松散，追求速度是高效的。此时，Python、Ruby、Groovy这类的语言手到擒来，好不快活。但是对于中大型项目，时间跨度较长的，还是应该范式优先，即使Java有那么一点笨重。

