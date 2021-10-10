---
title: Opensource-license
date: 2021-10-10 19:49:03
tags: 
- open source
- license
---

### 引言

现今软件开发不可避免的会用到开源软件，开源软件的使用则涉及到开源许可证的限制，了解遵守许可是必要的。各个许可的差异主要有是否允许修改、新增代码许可类型、是否允许商用等。 开源许可是一种法律许可，通过该许可规范了使用者如何使用开源产品以及应承担许可要求的义务。 开源一般分为开源软件、开源硬件、开源设计、开源内容，一般指开源软件。

### 现状

 [开源促进会（OSI，Open Source Initiative）]([Licenses by Name | Open Source Initiative](https://opensource.org/licenses/alphabetical))批准的大致百来种，主要有MIT、BSD、Apache、GPL等。[木兰社区](mulanos.oschina.net)制定的[木兰协议](license.coscl.org.cn)

已通过OSI认证。木兰社区尽管由官方牵头，目前公司、组织、个人参与度并不高，开源项目亦有限。以下分别是Whitesource、 Github、 Backduck 做的许可使用率的调查。

<img src="PERMISSIVE-VS-COPYLEFT-LICENSES-2016.jpg" alt="Permissive copyleft license" style="zomm:%100;"/>

<img src="github-repo-license-num-2015.png" alt="Github license" style="zomm:%100;"/>

<img src="blackduck-opensource-license-2014.png" alt="Blackduck license" style="zomm:%100;"/>

### 主要许可比较

<img src="opensource-license-comparison.png" alt="license comparison" style="zomm:%100;"/>

GPL(GNU General Public License)

GPL的出发点是代码的开源/免费使用和引用/修改/衍生代码的开源/免费使用，但不允许修改后和衍生的代码做为闭源的商业软件发布和销售。GPL协议的主要内容是只要在一个软件中使用(”使用”指类库引用，修改后的代码或者衍生代码)GPL协议的产品，则该软件产品必须也采用GPL协议，既必须也是开源和免费。这就是所谓的”传染性”。

LGPL(GNU Lesser General Public License)

LGPL是GPL的一个为主要为类库使用设计的开源协议。和GPL要求任何使用/修改/衍生之GPL类库的的软件必须采用GPL协议不同。LGPL允许商业软件通过类库引用(link)方式使用LGPL类库而不需要开源商业软件的代码。这使得采用LGPL协议的开源代码可以被商业软件作为类库引用并发布和销售。但是如果修改LGPL协议的代码或者衍生，则所有修改的代码，涉及修改部分的额外代码和衍生的代码都必须采用LGPL协议。因此LGPL协议的开源代码很适合作为第三方类库被商业软件引用，但不适合希望以LGPL协议代码为基础，通过修改和衍生的方式做二次开发的商业软件采用。

Apache Licence

Apache Licence是著名的非盈利开源组织Apache采用的协议。鼓励代码共享和尊重原作者的著作权，允许代码修改，再发布(作为开源或商业软件)。需要给代码的用户一份Apache Licence，如果你修改了代码，需要在被修改的文件中说明。在延伸的代码中(修改和有源代码衍生的代码中)需要带有原来代码中的协议，商标，专利声明和其他原来作者规定需要包含的说明。如果再发布的产品中包含一个Notice文件，则在Notice文件中需要带有Apache Licence。可以在Notice中增加自己的许可，但不可以表现为对Apache Licence构成更改。

BSD开源协议

BSD开源协议是一个给于使用者很大自由的协议。基本上使用者可以”为所欲为”，可以自由的使用，修改源代码，也可以将修改后的代码作为开源或者专有软件再发布。BSD代码鼓励代码共享，但需要尊重代码作者的著作权。如果再发布的产品中包含源代码，则在源代码中必须带有原来代码中的BSD协议。如果再发布的只是二进制类库/软件，则需要在类库/软件的文档和版权声明中包含原来代码中的BSD协议。不可以用开源代码的作者/机构名字和原来产品的名字做市场推广。

MIT(MIT)

MIT是和BSD一样宽范的许可协议，作者只想保留版权，而无任何其他了限制.也就是说，你必须在你的发行版里包含原许可协议的声明，无论你是以二进制发布的还是以源代码发布的。

### 思考

开源项目、组织有哪些
