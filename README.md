# ceagle {#ceagle}

Ceagle 使用手册

**Table of contents**

[欢迎](#301259762840345-_topic_Newtopic) 4

[概览](#301259762840345-_topic_Newtopic1) 7

[关于](#301259762840345-_topic_Newtopic3) 10

[系统需求](#301259762840345-_topic_Newtopic2) 13

[新功能](#301259762840345-_topic_Newtopic8) 16

[版本介绍](#301259762840345-_topic_Newtopic6) 19

[最终用户协议](#301259762840345-_topic_Newtopic7) 22

[如何购买](#301259762840345-_topic_Newtopic9) 26

[获取帮助](#301259762840345-_topic_Newtopic5) 29

[快速开始](#301259762840345-_topic_Newtopic12) 32

[网页版](#301259762840345-_topic_Newtopic33) 34

[如何启动](#301259762840345-_topic_Newtopic38) 37

[新建项目](#301259762840345-_topic_Newtopic39) 40

[添加属性](#301259762840345-_topic_Newtopic40) 43

[开始验证](#301259762840345-_topic_Newtopic41) 46

[验证结果](#301259762840345-_topic_Newtopic42) 49

[命令行版](#301259762840345-_topic_Newtopic28) 52

[如何安装](#301259762840345-_topic_Newtopic31) 55

[如何启动](#301259762840345-_topic_Newtopic32) 58

[添加属性](#301259762840345-_topic_Newtopic34) 61

[开始验证](#301259762840345-_topic_Newtopic35) 64

[验证结果](#301259762840345-_topic_Newtopic36) 67

[网页版](#301259762840345-_topic_Newtopic4) 70

[注册登陆](#301259762840345-_topic_Newtopic43) 73

[代码上传](#301259762840345-_topic_Newtopic44) 76

[偏好设置](#301259762840345-_topic_Newtopic45) 79

[验证操作](#301259762840345-_topic_Newtopic46) 82

[命令行版](#301259762840345-_topic_Newtopic14) 85

[通用参数](#301259762840345-_topic_Newtopic16) 88

[验证引擎参数](#301259762840345-_topic_Newtopic17) 91

[SMT引擎参数](#301259762840345-_topic_SMT) 94

[基本功能](#301259762840345-_topic_Newtopic25) 97

[添加约束](#301259762840345-_topic_Newtopic26) 100

[添加属性](#301259762840345-_topic_Newtopic27) 103

[通用属性](#301259762840345-_topic_Newtopic11) 106

[assert](#301259762840345-_topic_assert) 109

[代码可达性](#301259762840345-_topic_Newtopic29) 112

[开始验证](#301259762840345-_topic_Newtopic30) 115

[验证结果](#301259762840345-_topic_Newtopic15) 118

[高级功能](#301259762840345-_topic_Newtopic13) 121

[学会使用高级功能](#301259762840345-_topic_Newtopic47) 124

[选择验证引擎](#301259762840345-_topic_Newtopic48) 127

[DFS引擎](#301259762840345-_topic_DFS1) 130

[抽象精化](#301259762840345-_topic_Newtopic10) 133

[组合验证](#301259762840345-_topic_Newtopic50) 136

[重写引擎](#301259762840345-_topic_Newtopic51) 139

[选择约束求解器](#301259762840345-_topic_Newtopic18) 142

[Z3](#301259762840345-_topic_Z3) 145

[dReal](#301259762840345-_topic_dReal) 148

[MathSAT](#301259762840345-_topic_MathSAT) 151

[CVC4](#301259762840345-_topic_CVC4) 154

[FAQ](#301259762840345-_topic_FAQ1) 157

[开始使用](#301259762840345-_topic_Newtopic56) 160

[使用Ceagle对我的电脑有什么要求吗？](#301259762840345-_topic_Ceagle1) 163

[网页版和命令行版有什么区别？](#301259762840345-_topic_Newtopic57) 166

[Ceagle可以验证什么类型的程序？](#301259762840345-_topic_Ceagle2) 169

[Ceagle可以验证什么类型的属性？](#301259762840345-_topic_Ceagle3) 172

[我可以免费使用吗？](#301259762840345-_topic_Newtopic58) 175

[我可以从哪里获得帮助？](#301259762840345-_topic_Newtopic59) 178

[基本功能](#301259762840345-_topic_Newtopic60) 181

[在验证过程中Ceagle没有响应](#301259762840345-_topic_Ceagle4) 184

[遇到unknown的验证结果我该怎么办？](#301259762840345-_topic_unknown) 187

[高级功能](#301259762840345-_topic_Newtopic61) 190

[什么时候我应该使用抽象精化选项？](#301259762840345-_topic_Newtopic62) 193

[什么时候我应该使用组合验证选项？](#301259762840345-_topic_Newtopic63) 196

[路径优先策略与实时求解策略有什么区别？](#301259762840345-_topic_Newtopic64) 199

[我应该如何选择不同的约束求解器？](#301259762840345-_topic_Newtopic65) 202

[其它](#301259762840345-_topic_Newtopic66) 205

[附录：错误代码](#301259762840345-_topic_Newtopic37) 208

**欢迎**

Ceagle是一个简单易用且功能强大的C语言程序验证工具，可以帮助软件工程师判定assert语句的正确性，也可以发现程序中的内存溢出、数组越界、野指针等问题，亦可以用来分析代码的可达性。

Ceagle同时提供网页版和命令行版两个版本，方便不同需求、不同平台的用户使用。

本使用手册旨在帮助新用户快速掌握Ceagle，也可以帮助老用户进阶使用。

新用户

*   阅读[概览](#301259762840345-_topic_Newtopic1)来了解Ceagle的不同版本和系统配置需求
*   通过[快速开始](#301259762840345-_topic_Newtopic12)来熟悉C语言程序的验证流程。

老用户

*   阅读[新功能](#301259762840345-_topic_Newtopic8)来了解新版本的主要功能更新
*   通过[快速开始](#301259762840345-_topic_Newtopic12)来熟悉新版本的验证流程。

_Created with the Personal Edition of HelpNDoc:_ [_Free CHM Help documentation generator_](http://www.helpndoc.com)

**概览**

*   [关于](#301259762840345-_topic_Newtopic3)
*   [系统需求](#301259762840345-_topic_Newtopic2)
*   [新功能](#301259762840345-_topic_Newtopic8)
*   [版本介绍](#301259762840345-_topic_Newtopic6)
*   [最终用户协议](#301259762840345-_topic_Newtopic7)
*   [如何购买](#301259762840345-_topic_Newtopic9)
*   [获取帮助](#301259762840345-_topic_Newtopic5)

_Created with the Personal Edition of HelpNDoc:_ [_Free EBook and documentation generator_](http://www.helpndoc.com)

**关于**

Ceagle是一个简单易用且功能强大的C语言程序验证工具，可以帮助软件工程师判定assert语句的正确性，也可以发现程序中的内存溢出、数组越界、野指针等问题，亦可以用来分析特定代码的可达性。

Ceagle同时提供网页版和命令行版两个版本，方便不同需求、不同平台的用户使用。

_Created with the Personal Edition of HelpNDoc:_ [_Free HTML Help documentation generator_](http://www.helpndoc.com)

**系统需求**

**网页版**推荐系统配置需求：

*   Windows XP或更高版本，Mac OS X 10.5或更高版本，或其它支持浏览器的操作系统
*   Internet Explorer 8、9、10或更高版本，Firefox，Chrome或Safari
*   1024 x 768或更高分辨率的显示器
*   512MB内存或更高
*   局域网或因特网连接

**命令行版**会在本地运行验证程序，对系统配置要求较高，推荐系统配置需求：

*   Linux 32位或64位操作系统
*   双核2.0GHz的处理或更高
*   8GB内存或更高

低于推荐系统配置的环境不能保证验证效果或使用体验。

_Created with the Personal Edition of HelpNDoc:_ [_Generate EPub eBooks with ease_](http://www.helpndoc.com/create-epub-ebooks)

**新功能**

暂无。

_Created with the Personal Edition of HelpNDoc:_ [_Single source CHM, PDF, DOC and HTML Help creation_](http://www.helpndoc.com/help-authoring-tool)

**版本介绍**

**网页版**支持程序文件或项目的上传、在线新建、在线编辑、在线验证、验证结果下载等功能，需要用户注册使用，且为每个账户提供在线的程序文件、项目、验证记录云存储。

**命令行版**仅支持Linux系统，可以对程序、验证工具、验证结果、验证中间文件有全面的访问权限，提供丰富的定制化接口，推荐高级用户使用。

_Created with the Personal Edition of HelpNDoc:_ [_Free EPub and documentation generator_](http://www.helpndoc.com)

**最终用户协议**

**IMPORTANT:** THIS SOFTWARE END USER LICENSE AGREEMENT (“EULA”) IS A LEGAL AGREEMENT BETWEEN YOU AND 清华大学. READ IT CAREFULLY BEFORE COMPLETING THE INSTALLATION PROCESS AND USING THE SOFTWARE. IT PROVIDES A LICENSE TO USE THE SOFTWARE AND CONTAINS WARRANTY INFORMATION AND LIABILITY DISCLAIMERS. BY INSTALLING AND USING THE SOFTWARE, YOU ARE CONFIRMING YOUR ACCEPTANCE OF THE SOFTWARE AND AGREEING TO BECOME BOUND BY THE TERMS OF THIS AGREEMENT. IF YOU DO NOT AGREE TO BE BOUND BY THESE TERMS, THEN SELECT THE "CANCEL" BUTTON. DO NOT INSTALL THE SOFTWARE AND RETURN THE SOFTWARE TO YOUR PLACE OF PURCHASE FOR A FULL REFUND.

THIS EULA SHALL APPLY ONLY TO THE SOFTWARE SUPPLIED BY 清华大学 HEREWITH REGARDLESS OF WHETHER OTHER SOFTWARE IS REFERRED TO OR DESCRIBED HEREIN.

DEFINITIONS

(a) "Ceagle" and "Software" refers to 清华大学's Ceagle program, in each case, supplied by 清华大学 herewith, and corresponding documentation, associated media, and online or electronic documentation.

(b) "清华大学" means 清华大学.

(c) "Free Version" or "Freeware Version" or "Freeware Edition" or "Personal Edition" means a free version of the Software for personal use only, so identified, to be used only for non-profit projects. The Free Version is fully functional, without restrictions of any kind but may contain messages in the end product stating that they have been created using the Free Version of the Software.

(d) "Registered Version" means a version which has been bought to 清华大学.

(e) "Educational Version" means a version which has been bought to 清华大学 by an educational institution and may only be provided to students and employees of the institution. The Educational Version may have limited functionalities and/or usage restrictions.

LIABILITY DISCLAIMER

THE Ceagle PROGRAM IS DISTRIBUTED "AS IS". NO WARRANTY OF ANY KIND IS EXPRESSED OR IMPLIED. YOU USE IT AT YOUR OWN RISK. NEITHER THE AUTHORS NOR 清华大学 WILL BE LIABLE FOR DATA LOSS, DAMAGES AND LOSS OF PROFITS OR ANY OTHER KIND OF LOSS WHILE USING OR MISUSING THIS SOFTWARE.

RESTRICTIONS

You may not use, copy, emulate, clone, rent, lease, sell, modify, decompile, disassemble, otherwise reverse engineer, or transfer any version of the Software, or any subset of it, except as provided for in this agreement. Any such unauthorized use shall result in immediate and automatic termination of this license and may result in criminal and/or civil prosecution.

FOR Ceagle FREE VERSION ONLY

(a) Any Help File or associated intermediate files generated by Ceagle Free Version MUST NOT be used for, or in relation with, any commercial or business purpose, whether "for profit" or "not for profit". Any work performed or produced as a result of use of this Software cannot be performed or produced for the benefit of other parties for a fee, compensation or any other reimbursement or remuneration.

(b) The Ceagle Free version may be freely distributed, with exceptions noted below, provided the distribution package is not modified in ANY WAY.

(c) The Ceagle Free version may not be distributed inside of any other software package without written permission of 清华大学.

(d) The Ceagle Free version allows the user to publish its work according to the license agreement, but nor 清华大学 nor any member of the company can be held liable for the content of the publication.

FOR Ceagle REGISTERED VERSION ONLY

(a) Single-User (per seat) Licenses: You may install and use the Software on a single computer to design, develop, and test the Software's output. Installation on a second computer, such as a laptop and a desktop computer, is permitted if it is guaranteed that you are the exclusive user of both computers.

(b) Multiple-User (floating) Licenses: You may install and use the enclosed Software on a server to design, develop, and test the Software's output. Use of the Software is limited by the number of floating licenses owned. Only one user per floating license owned may use the software at the same time.

(c) The Ceagle Registered version allows the registered user to publish its work according to the license agreement, but nor 清华大学 nor any member of the company can be held liable for the content of the publication.

(d) The Ceagle Registered version guaranties to the registered user free updates for a whole version cycle and for at least 12 (twelve) months.

FOR Ceagle EDUCATIONAL VERSION ONLY

(a) You may install and use the Software on a single computer; OR install and store the Software on a storage device, such as a network server, used only to install the Software on your other computers over an internal network, provided you have a license for each separate computer on which the Software is installed and run. A license for the Software may not be shared, installed or used concurrently on different computers.

(b) The Software may be used on a single computer solely for individual and personal "technology enthusiast" purposes, personal education and study (including educational-related research), or administrative use in support of the educational institution. It may not be used for any commercial or business purpose, whether "for profit" or "not for profit." Any work performed or produced as a result of use of this Software cannot be performed or produced for the benefit of other parties for a fee, compensation or any other reimbursement or remuneration.

(c) The Ceagle Educational version allows the registered user to publish its work according to the license agreement, but nor 清华大学 nor any member of the company can be held liable for the content of the publication.

(d) The Ceagle Educational version guaranties to the registered user free updates for a whole version cycle and for at least 12 (twelve) months.

TERMS

This license is effective until terminated. You may terminate it by destroying the program, the documentation and copies thereof. This license will also terminate if you fail to comply with any terms or conditions of this agreement. You agree upon such termination to destroy all copies of the program and of the documentation, or return them to the author.

OTHER RIGHTS AND RESTRICTIONS

All other rights and restrictions not specifically granted in this license are reserved by authors.

_Created with the Personal Edition of HelpNDoc:_ [_Free EPub producer_](http://www.helpndoc.com/create-epub-ebooks)

**如何购买**

Ceagle为全球用户提供购买渠道，线上、线下均可，支持信用卡、支票、PayPal、支付宝等各类支付方式，支持如美元、欧元、人民币、日元等各国货币。

一旦支持完成，您将立刻收到安装和使用Ceagle的详细指南。

如需了解订购Ceagle的更多信息，您可以启动浏览器并访问Ceagle的商店页面：[http://sts.thss.tsinghua.edu.cn/ceagle/store](http://sts.thss.tsinghua.edu.cn/ceagle/store)。

_Created with the Personal Edition of HelpNDoc:_ [_Free EBook and documentation generator_](http://www.helpndoc.com)

**获取帮助**

本使用手册既可以在网上阅读，也可以从安装好的Ceagle网页版、命令行版中离线阅读。同时，您亦可以从Ceagle官方网站（[http://sts.thss.tsinghua.edu.cn/ceagle/help](http://sts.thss.tsinghua.edu.cn/ceagle/help)）中获取该使用手册最新版本的不同格式。

离线帮助

离线的使用手册是安装好的Ceagle网页版、命令行版的一部分。

要在**网线版**中打开使用手册，请在键盘上敲击F1按键，或鼠标点击右上角的帮助按钮。

要在**命令行版**中打开使用手册，请使用命令ceagle --help。

在线帮助

如需在线访问Ceagle的最新使用手册，可以启动浏览器并访问Ceagle的商店页面：[http://sts.thss.tsinghua.edu.cn/ceagle/help/documentation/index.html](http://sts.thss.tsinghua.edu.cn/ceagle/help/documentation/index.html)。

打印帮助

您亦可以下载并打印Ceagle使用手册的PDF或者Word版本，下载地址是：[http://sts.thss.tsinghua.edu.cn/ceagle/help](http://sts.thss.tsinghua.edu.cn/ceagle/help)。

_Created with the Personal Edition of HelpNDoc:_ [_Free EBook and documentation generator_](http://www.helpndoc.com)

**快速开始**

_Created with the Personal Edition of HelpNDoc:_ [_What is a Help Authoring tool?_](http://www.helpauthoringsoftware.com)

**网页版**

*   如何启动
*   新建项目
*   添加属性
*   开始验证
*   验证结果

_Created with the Personal Edition of HelpNDoc:_ [_Easily create Web Help sites_](http://www.helpndoc.com/feature-tour)

**如何启动**

*   打开网页浏览器
*   访问Ceagle网页版页面：[http://sts.thss.tsinghua.edu.cn/ceagle/online/](http://sts.thss.tsinghua.edu.cn/ceagle/online/)
*   （老用户可跳过这一步骤）点击注册按钮，填写相关信息，完成注册，并跳过下一步
*   点击登陆按钮，输入用户名、密码进行登陆
*   登陆成功后，Ceagle网页版页面，启动完成

_Created with the Personal Edition of HelpNDoc:_ [_Generate EPub eBooks with ease_](http://www.helpndoc.com/create-epub-ebooks)

**新建项目**

通过手动添加的方式新建项目

*   在左侧项目导航中，右击鼠标，选择“新建项目”
*   在弹出窗口中，填写项目名称
*   在左侧项目导航中，鼠标右击项目名称，选择“新建文件”或“新建文件夹”
*   新建项目的创建流程，通过以上步骤实现

通过上传代码的方式新建项目

*   鼠标点击页面左上角的“上传”按钮
*   通过“选择文件”按钮或拖拽的方式，上传本地代码文件
*   新建项目的创建流程，通过以上步骤实现

_Created with the Personal Edition of HelpNDoc:_ [_Easily create EPub books_](http://www.helpndoc.com/feature-tour)

**添加属性**

*   在左侧项目导航中，点击某一代码文件
*   文件内容将以可编辑的方式，出现在页面中部的代码池中
*   在右侧属性选择栏中，系统自动扫描出代码中的属性
*   点击每条属性，页面中部的代码池，随即将光标定位到对应位置

_Created with the Personal Edition of HelpNDoc:_ [_Full-featured Documentation generator_](http://www.helpndoc.com)

**开始验证**

*   在右侧属性选择栏中，点击某一属性最右侧的验证按钮
*   系统将根据用户选择的属性，对项目代码进行验证
*   在中部日志栏中，系统将给出验证过程中的系统日志，可供查看
*   在右侧反例路径栏中，系统将给出验证属性的反例路径，可供查看

_Created with the Personal Edition of HelpNDoc:_ [_Write eBooks for the Kindle_](http://www.helpndoc.com/feature-tour/create-ebooks-for-amazon-kindle)

**验证结果**

*   点击右侧反例路径栏中的+号，展开反例路径信息
*   查看验证结果

_Created with the Personal Edition of HelpNDoc:_ [_Easily create EBooks_](http://www.helpndoc.com/feature-tour)

**命令行版**

*   如何安装
*   如何启动
*   添加属性
*   开始验证
*   验证结果

_Created with the Personal Edition of HelpNDoc:_ [_News and information about help authoring tools and software_](http://www.helpauthoringsoftware.com)

**如何安装**

*   打开网页浏览器
*   访问Ceagle首页：[http://sts.thss.tsinghua.edu.cn/ceagle](http://sts.thss.tsinghua.edu.cn/ceagle)
*   点击下载按钮，下载ceagle-1.0.zip
*   下载完成后，解压缩下载的压缩包
*   将解压后的目录添加到系统的PATH中，例如：
    *   压缩包的路径是/home/user/ceagle
    *   编辑用户的~/.bashrc文件
    *   在其中加入export PATH=$PATH:/home/user/ceagle
*   验证安装：在命令行中输入ceagle --version，输出Ceagle的命令行帮助则安装成功

_Created with the Personal Edition of HelpNDoc:_ [_Write eBooks for the Kindle_](http://www.helpndoc.com/feature-tour/create-ebooks-for-amazon-kindle)

**如何启动**

*   假设目标验证文件为 example.c，在命令行中输入ceagle example.c即可进行验证
*   假设目标验证项目路径为~/projects/example，在命令行中输入ceagle ~/projects/example/即可进行验证

_Created with the Personal Edition of HelpNDoc:_ [_Free Web Help generator_](http://www.helpndoc.com)

**添加属性**

添加属性有如下方法：

*   修改源代码：在源代码中加入assert(condition)，Ceagle会在验证到该行代码时检查condition是否为真
*   修改源代码：在源代码中加入一个C语言标签ERROR，Ceagle会验证ERROR是否可达
*   通过参数指定代码行：例如在运行时加入--line=15，Ceagle会验证第15行是否可达

_Created with the Personal Edition of HelpNDoc:_ [_Write eBooks for the Kindle_](http://www.helpndoc.com/feature-tour/create-ebooks-for-amazon-kindle)

**开始验证**

*   默认参数下，Ceagle在验证过程中不会有任何输出，所以在验证过程中请耐心等待
*   如需看到所有输出，可以使用--verbose选项

_Created with the Personal Edition of HelpNDoc:_ [_Produce electronic books easily_](http://www.helpndoc.com/create-epub-ebooks)

**验证结果**

*   当程序满足属性时，Ceagle输出TRUE
*   当程序不满足属性时，Ceagle输出FALSE，并会生成example.c.ce反例文件
    *   反例文件格式请参阅[http://sv-comp.sosy-lab.org/2016/witnesses/](http://sv-comp.sosy-lab.org/2016/witnesses/)
*   当出现异常时，Ceagle输出UNKNOWN并给出异常的原因

_Created with the Personal Edition of HelpNDoc:_ [_Full-featured EPub generator_](http://www.helpndoc.com/create-epub-ebooks)

**网页版**

Ceagle网页版的操作界面如下图所示。该界面中包含了项目浏览、代码编辑、属性查看、属性验证、反例路径查看、验证日志查看、代码上传等主要功能。

1\. 项目浏览

*   项目结构浏览：系统提供树状项目结构，用户可以浏览和查看各级文件夹和文件
*   项目的新建和删除：用户可以在左侧项目导航栏，进行项目的新建和删除操作
*   文件的新建和删除：用户可以在左侧项目导航栏，在特定项目位置，对文件和文件夹进行新建和删除操作
*   项目导出：用户可以将特定项目导出，保存到本地

2\. 代码编辑

*   代码编辑：用户可以对打开的代码文件进行编辑
*   代码手动保存：用户可以通过键盘快捷键Ctrl+S（Mac用户为Command+S），对当前代码进行手动保存
*   代码自动保存：切换代码文件时，系统将对前一代码文件进行自动保存

3\. 属性选择

*   自动扫描：系统将自动扫描当前代码文件中的验证属性，并列举在右侧”属性选择“栏中
*   属性定位：用户可以通过点击某一属性，定位到其位于代码文件中的位置
*   属性验证：用户可以对某一属性进行验证

4\. 反例路径

*   路径查看：系统将验证结果列举在右侧”反例路径“栏中，用户可以浏览和查看详细结果

5\. 验证日志

*   日志打印：系统将验证日志输出在中部”日志“栏中，用户可以查看

_Created with the Personal Edition of HelpNDoc:_ [_Free help authoring tool_](http://www.helpndoc.com/help-authoring-tool)

**注册登陆**

*   进入Ceagle网页版界面后，（老用户可跳过这一步骤）点击注册按钮，填写相关信息，完成注册，并跳过下一步
*   点击登陆按钮，输入用户名、密码进行登陆
*   登陆成功后，Ceagle网页版页面，启动完成

_Created with the Personal Edition of HelpNDoc:_ [_Full-featured Documentation generator_](http://www.helpndoc.com)

**代码上传**

*   点击页面左上角的上传按钮

*   代码上传
    *   选择上传：点击“选择文件”按钮， 选择代码压缩包进行上传
    *   拖拽上传：拖拽文件到中间指定的区域，进行项目的上传

*   上传成功后，新的项目将出现在左侧项目导航栏中

_Created with the Personal Edition of HelpNDoc:_ [_Full-featured EPub generator_](http://www.helpndoc.com/create-epub-ebooks)

**偏好设置**

*   点击左上角的设置按钮
*   选择代码池风格、代码字体大小等偏好设置
*   按用户自身喜好，进行设置并确认

_Created with the Personal Edition of HelpNDoc:_ [_Benefits of a Help Authoring Tool_](http://www.helpauthoringsoftware.com)

**验证操作**

添加属性

*   在左侧项目导航中，点击某一代码文件
*   文件内容将以可编辑的方式，出现在页面中部的代码池中
*   在右侧属性选择栏中，系统自动扫描出代码中的属性
*   点击每条属性，页面中部的代码池，随即将光标定位到对应位置

进行验证

*   在右侧属性选择栏中，点击某一属性最右侧的验证按钮
*   系统将根据用户选择的属性，对项目代码进行验证
*   在中部日志栏中，系统将给出验证过程中的系统日志，可供查看
*   在右侧反例路径栏中，系统将给出验证属性的反例路径，可供查看

_Created with the Personal Edition of HelpNDoc:_ [_Easily create Web Help sites_](http://www.helpndoc.com/feature-tour)

**命令行版**

_Created with the Personal Edition of HelpNDoc:_ [_Easily create EPub books_](http://www.helpndoc.com/feature-tour)

**通用参数**

通用参数：

*   --help, -h：显示帮助
*   --version：显示版本
*   --verbose：显示详细的日志
*   --line：指定插入可达性标签的位置，可以指定多次
*   --time,-t=900：指定时间限制，单位为秒

_Created with the Personal Edition of HelpNDoc:_ [_News and information about help authoring tools and software_](http://www.helpauthoringsoftware.com)

**验证引擎参数**

验证引擎参数：

*   --engine=dfs：指定验证引擎，可以选择dfs引擎或rewrite引擎
*   --advisor=simple：当使用dfs引擎时，指定Advisor的算法，可以选择naive、simple、absref、compositional等算法及其组合
*   --bmc=200：当使用naive或simple算法时，指定bmc展开的深度
*   --predicate：当使用absref算法时，手动指定初始谓词

_Created with the Personal Edition of HelpNDoc:_ [_Free CHM Help documentation generator_](http://www.helpndoc.com)

**SMT引擎参数**

SMT引擎参数用来指定求解所用的smt引擎

*   --smt=z3：默认为z3，可选的引擎包括：z3，dReal，mathsat，CVC4，需要注意的是有的引擎可能有局限，对于某些类型的程序完全无法使用

_Created with the Personal Edition of HelpNDoc:_ [_Write eBooks for the Kindle_](http://www.helpndoc.com/feature-tour/create-ebooks-for-amazon-kindle)

**基本功能**

了解Ceagle的基本功能涉及的概念，包括添加一条约束、声明验证属性、配置验证参数、验证结果的构成。关于以上部分功能在**网页版**和**命令行版**中的具体操作请参阅[网页版](#301259762840345-_topic_Newtopic33)和命令行版。

*   添加约束
*   添加属性
    *   通用属性
    *   assert
    *   代码可达性
*   开始验证
*   验证结果

_Created with the Personal Edition of HelpNDoc:_ [_Free help authoring tool_](http://www.helpndoc.com/help-authoring-tool)

**添加约束**

约束是指在程序运行到某个位置时，包含一个或多个变量的布尔表达式取值为真。对于待验证的C程序，如果需要假设变量的取值在运行到某个位置时满足某些条件，则可以在该位置插入一条约束。

Ceagle使用C语言的方式声明约束。如果要使用约束功能，请在待验证的C程序中插入一个返回值为空、参数仅包含一个int类型参数的外部函数声明，并在Ceagle中将约束声明函数名称设定为该函数名。当需要插入约束时，按照C语言的方式构建布尔表达式并以此为参数调用约束声明函数。Ceagle会自动识别这些函数调用并建立约束。

**注意！**由于C语言没有bool类型，构建出的布尔表达式的值实际上是一个取值为0或1的int类型，对应的约束为表达式值等于1。

下图给出了一个使用约束的例子，在Ceagle中设定约束声明函数为assume后，Ceagle会识别出在程序第5行插入的约束。

应用约束的场合，如果属性不成立，那么一定存在一条程序执行路径，其上所有的约束描述的变量取值条件都满足，并且这条路径会导致属性不成立；反之，如果属性成立，那么不存在这样一条程序执行路径。在上面的例子中，使用约束前安全属性不成立，但使用后安全属性成立。

_Created with the Personal Edition of HelpNDoc:_ [_Free EPub and documentation generator_](http://www.helpndoc.com)

**添加属性**

了解Ceagle支持验证的属性，包括内存安全、程序终止性、assert语句声明的安全属性、代码可达性等。

有关设定验证属性的具体操作，请分别参阅网页版[添加属性](#301259762840345-_topic_Newtopic40)和命令行版添加属性。

*   通用属性
*   assert
*   代码可达性

_Created with the Personal Edition of HelpNDoc:_ [_Full-featured Documentation generator_](http://www.helpndoc.com)

**通用属性**

Ceagle支持验证内存安全和程序终止性两类通用属性。

内存安全属性要求程序中不存在：无效的内存释放；指针访问越界；没有指针指向但未释放的内存。

程序终止性属性要求程序中不存在一条无限长度的执行路径。

要向验证任务添加一条通用属性，请分别参阅网页版[添加属性](#301259762840345-_topic_Newtopic40)和命令行版添加属性中介绍的具体操作

_Created with the Personal Edition of HelpNDoc:_ [_Full-featured Kindle eBooks generator_](http://www.helpndoc.com/feature-tour/create-ebooks-for-amazon-kindle)

**assert**

Ceagle支持验证使用C语言中的assert函数声明的安全属性。关于assert函数的使用请参阅C语言的文档和帮助。

Ceagle默认向验证任务添加assert安全属性，如果需要不考虑assert安全属性并忽略所有的assert语句，请对Ceagle进行设置。

具体操作请分别参阅网页版[添加属性](#301259762840345-_topic_Newtopic40)和命令行版添加属性。

_Created with the Personal Edition of HelpNDoc:_ [_Easy EPub and documentation editor_](http://www.helpndoc.com)

**代码可达性**

Ceagle支持验证程序中的某行代码是否可达，要使用这一功能，请指定需要验证可达性的代码，然后在Ceagle中向验证任务添加代码可达性属性。指定需要验证可达性的代码的方式包括插入C语言标签、给出行号或直接在程序代码中选择（仅限**网页版**）。

具体操作请分别参阅网页版[添加属性](#301259762840345-_topic_Newtopic40)和命令行版添加属性。

_Created with the Personal Edition of HelpNDoc:_ [_Create help files for the Qt Help Framework_](http://www.helpndoc.com/feature-tour/create-help-files-for-the-qt-help-framework)

**开始验证**

开始验证前，请确保各项设定符合验证任务。

具体设定请分别参阅网页版[开始验证](#301259762840345-_topic_Newtopic41)和命令行版开始验证。

_Created with the Personal Edition of HelpNDoc:_ [_iPhone web sites made easy_](http://www.helpndoc.com/feature-tour/iphone-website-generation)

**验证结果**

Ceagle提供丰富的信息以展示完整的验证结果。在**网页版**和**命令行版**中这些信息的展示存在一些细节上的差别，具体内容请分别参阅网页版[验证结果](#301259762840345-_topic_Newtopic42)和命令行版验证结果。

*   验证结论：Ceagle对给定属性进行验证的结果。验证结论可能的情况有**TRUE**、**FALSE**和**UNKNOWN**。属性成立的情形结论为**TRUE**。属性不成立的情形结论为**FALSE**。程序中存在不支持的特性，或者受限于程序的复杂性和验证引擎的计算能力而不能有效的判断属性成立与否的情形，Ceagle将给出**UNKNOWN**作为验证结论。
*   反例：验证结论为**FALSE**的情形，Ceagle会给出一条导致属性不成立的程序执行路径作为反例。在**网页版**中反例将直接展示在程序代码中，在**命令行版**中反例会以源代码中的行号展示。
*   运行信息：开发者可以选择查看Ceagle完成验证任务消耗的时间和资源以及验证过程的中间信息。
*   多属性验证：当验证任务包含多条属性时，Ceagle会针对每个属性给出结果信息，并以表格形式整理提供。

_Created with the Personal Edition of HelpNDoc:_ [_Free iPhone documentation generator_](http://www.helpndoc.com/feature-tour/iphone-website-generation)

**高级功能**

Ceagle为高级用户提供了强大的可配置性。用户可以根据需求，灵活选择不同的验证引擎、搜索策略以及约束求解器，得到关于目标程序的更为精确的验证结果。

_Created with the Personal Edition of HelpNDoc:_ [_Easy EPub and documentation editor_](http://www.helpndoc.com)

**学会使用高级功能**

在使用Ceagle的过程中，往往会在验证的环节遇到验证时间过长或提示无法验证的情况。这是由于Ceagle所采用的技术不能适用于所有类型的目标程序以及所有类型的验证属性。严格来说，目前不存在一种验证技术可以适用于所有类型的目标程序以及所有类型的验证属性。

Ceagle默认基于DFS引擎、采用Z3求解器对目标程序及属性进行验证，但同时提供了重写引擎，以及诸如dReal、CVC4等其它同样优秀的约束求解器可供配置。根据目标程序、验证属性的不同，选用不同的验证引擎，甚至配置更合适的搜索策略，才能获得更精确的验证结果以及更高的验证效率。

_Created with the Personal Edition of HelpNDoc:_ [_Full-featured Documentation generator_](http://www.helpndoc.com)

**选择验证引擎**

Ceagle后台采用了两个验证引擎：

*   DFS引擎
*   重写引擎

_Created with the Personal Edition of HelpNDoc:_ [_Free Kindle producer_](http://www.helpndoc.com/feature-tour/create-ebooks-for-amazon-kindle)

**DFS引擎**

DFS引擎采用LLVM IR作为目标程序的表示方式，利用深度优先搜索（DFS）算法遍历目标程序的状态空间，并调用约束求解器判断该目标程序是否满足待验证属性。

Ceagle默认采用DFS引擎进行验证，若要显式指定其使用DFS引擎，用法如下：

*   网页版

// 网页版用法

*   命令行版

ceagle --engine=dfs example.c

详细使用方法请参阅[验证引擎参数](#301259762840345-_topic_Newtopic17)。

在此基础上，针对大型目标程序（或状态空间太大的目标程序），Ceagle提供以下技术提高验证效率：

*   抽象精化
*   组合验证

_Created with the Personal Edition of HelpNDoc:_ [_Free HTML Help documentation generator_](http://www.helpndoc.com)

抽象精化

抽象精化（Abstraction and Refinement）是一种缩減状态空间的技术。当目标程序的状态空间太大，使得Ceagle的DFS引擎搜索时间过长时，可以考虑采用抽象精化技术对状态空间进行削减，以达到提高验证效率的目的。

要注意的是，使用抽象精化技术并不能保证整体验证时间减少，这是由于状态空间削减的过程同样需要花费一定的时间。

用法如下：

*   网页版

// 网页版用法

*   命令行版

ceagle --advisor=absref example.c

详细使用方法请参阅[验证引擎参数](#301259762840345-_topic_Newtopic17)。

_Created with the Personal Edition of HelpNDoc:_ [_Free PDF documentation generator_](http://www.helpndoc.com)

组合验证

组合验证（Compositional Verification）也是一种解决目标程序状态空间爆炸问题的技术。组合验证技术基于分治思想，将大型目标程序及待验证属性划分为若干子模块以及各个子模块上对应的待验证属性，对各子模快分别进行验证，最后将各子模块的验证结果综合得到原目标程序的验证结果。上述过程由Ceagle后台自动完成。

组合验证的用法如下：

*   网页版

// 网页版用法

*   命令行版

ceagle --advisor=compositional example.c

详细使用方法请参阅[验证引擎参数](#301259762840345-_topic_Newtopic17)。

_Created with the Personal Edition of HelpNDoc:_ [_Full-featured Help generator_](http://www.helpndoc.com/feature-tour)

**重写引擎**

重写引擎采用Maude语言（见[http://maude.cs.illinois.edu](http://maude.cs.illinois.edu)）作为目标程序的表示方式，并调用线性时序逻辑（Linear Temporal Logic，LTL）模型检测工具以及符号化LTL模型检测工具判断该目标程序是否满足待验证属性。

Ceagle默认采用DFS引擎进行验证，若要指定其使用重写引擎，用法如下：

*   网页版

// 网页版用法

*   命令行版

ceagle --engine=rewrite foo.c

详细使用方法请参阅[验证引擎参数](#301259762840345-_topic_Newtopic17)。

_Created with the Personal Edition of HelpNDoc:_ [_Easy to use tool to create HTML Help files and Help web sites_](http://www.helpndoc.com/help-authoring-tool)

**选择约束求解器**

Ceagle在使用DFS引擎进行验证时，会采用约束求解器对待验证属性进行判定（详情参见：DFS引擎）。Ceagle默认采用Z3求解器，但同时也提供其它多种同样优秀的约束求解器，以满足不同验证问题的需求。

Ceagle支持以下求解器：

*   Z3
*   dReal
*   CVC4
*   MathSAT

_Created with the Personal Edition of HelpNDoc:_ [_Easily create iPhone documentation_](http://www.helpndoc.com/feature-tour/iphone-website-generation)

**Z3**

Z3（[https://github.com/Z3Prover/z3/wiki](https://github.com/Z3Prover/z3/wiki)）是微软开发的一款SMT约束求解器。Ceagle默认使用Z3对待验证属性进行验证求解。

若要显式指定Ceagle使用Z3作为约束求解器，用法如下：

*   网页版

// 网页版用法

*   命令行版

ceagle --smt=z3 foo.c

详细使用方法请参阅[SMT引擎参数](#301259762840345-_topic_SMT)。

_Created with the Personal Edition of HelpNDoc:_ [_Generate EPub eBooks with ease_](http://www.helpndoc.com/create-epub-ebooks)

**dReal**

dReal（[http://dreal.github.io](http://dreal.github.io/)）是一款实数域上的SMT约束求解器。

用法如下：

*   网页版

// 网页版用法

*   命令行版

ceagle --smt=dreal foo.c

详细使用方法请参阅[SMT引擎参数](#301259762840345-_topic_SMT)。

_Created with the Personal Edition of HelpNDoc:_ [_Free Kindle producer_](http://www.helpndoc.com/feature-tour/create-ebooks-for-amazon-kindle)

**MathSAT**

MathSAT（[http://mathsat.fbk.eu](http://mathsat.fbk.eu/)）是一款高效的SMT约束求解器，目前由Fondazione Bruno Kessler和DISI-University of Trento联合开发和维护。

用法如下：

*   网页版

// 网页版用法

*   命令行版

ceagle --smt=mathsat foo.c

详细使用方法请参阅[SMT引擎参数](#301259762840345-_topic_SMT)。

_Created with the Personal Edition of HelpNDoc:_ [_Easy Qt Help documentation editor_](http://www.helpndoc.com)

**CVC4**

CVC4（[http://cvc4.cs.nyu.edu](http://cvc4.cs.nyu.edu/)）是一款支持丰富理论域的SMT约束求解器，目前由NYU和U Iowa联合开发和维护。

用法如下：

*   网页版

// 网页版用法

*   命令行版

ceagle --smt=cvc4 foo.c

详细使用方法请参阅[SMT引擎参数](#301259762840345-_topic_SMT)。

_Created with the Personal Edition of HelpNDoc:_ [_Produce online help for Qt applications_](http://www.helpndoc.com/feature-tour/create-help-files-for-the-qt-help-framework)

**FAQ**

　　用户在使用Ceagle前或使用过程中可能遇到的一些问题及解决方案。

_Created with the Personal Edition of HelpNDoc:_ [_Single source CHM, PDF, DOC and HTML Help creation_](http://www.helpndoc.com/help-authoring-tool)

**开始使用**

　　用户在使用Ceagle前、安装过程中可能遇到的问题及解决方案。

_Created with the Personal Edition of HelpNDoc:_ [_Create help files for the Qt Help Framework_](http://www.helpndoc.com/feature-tour/create-help-files-for-the-qt-help-framework)

**使用Ceagle对我的电脑有什么要求吗？**

_Created with the Personal Edition of HelpNDoc:_ [_Single source CHM, PDF, DOC and HTML Help creation_](http://www.helpndoc.com/help-authoring-tool)

**网页版和命令行版有什么区别？**

_Created with the Personal Edition of HelpNDoc:_ [_Create help files for the Qt Help Framework_](http://www.helpndoc.com/feature-tour/create-help-files-for-the-qt-help-framework)

**Ceagle可以验证什么类型的程序？**

_Created with the Personal Edition of HelpNDoc:_ [_Easily create iPhone documentation_](http://www.helpndoc.com/feature-tour/iphone-website-generation)

**Ceagle可以验证什么类型的属性？**

_Created with the Personal Edition of HelpNDoc:_ [_Create iPhone web-based documentation_](http://www.helpndoc.com/feature-tour/iphone-website-generation)

**我可以免费使用吗？**

_Created with the Personal Edition of HelpNDoc:_ [_Full-featured multi-format Help generator_](http://www.helpndoc.com/help-authoring-tool)

**我可以从哪里获得帮助？**

请参阅[获取帮助](#301259762840345-_topic_Newtopic5)。

_Created with the Personal Edition of HelpNDoc:_ [_Single source CHM, PDF, DOC and HTML Help creation_](http://www.helpndoc.com/help-authoring-tool)

**基本功能**

　　用户在使用Ceagle的基本功能时可能遇到的问题及解决方案。

_Created with the Personal Edition of HelpNDoc:_ [_Benefits of a Help Authoring Tool_](http://www.helpauthoringsoftware.com)

**在验证过程中Ceagle没有响应**

_Created with the Personal Edition of HelpNDoc:_ [_Easily create Web Help sites_](http://www.helpndoc.com/feature-tour)

**遇到unknown的验证结果我该怎么办？**

_Created with the Personal Edition of HelpNDoc:_ [_Easily create HTML Help documents_](http://www.helpndoc.com/feature-tour)

**高级功能**

　　用户在使用Ceagle的高级功能时可能遇到的问题及解决方案。

_Created with the Personal Edition of HelpNDoc:_ [_Easily create PDF Help documents_](http://www.helpndoc.com/feature-tour)

**什么时候我应该使用抽象精化选项？**

_Created with the Personal Edition of HelpNDoc:_ [_Single source CHM, PDF, DOC and HTML Help creation_](http://www.helpndoc.com/help-authoring-tool)

**什么时候我应该使用组合验证选项？**

_Created with the Personal Edition of HelpNDoc:_ [_Free PDF documentation generator_](http://www.helpndoc.com)

**路径优先策略与实时求解策略有什么区别？**

_Created with the Personal Edition of HelpNDoc:_ [_Generate EPub eBooks with ease_](http://www.helpndoc.com/create-epub-ebooks)

**我应该如何选择不同的约束求解器？**

_Created with the Personal Edition of HelpNDoc:_ [_Free EBook and documentation generator_](http://www.helpndoc.com)

**其它**

　　用户在使用Ceagle时可能遇到的其它问题及解决方案。

_Created with the Personal Edition of HelpNDoc:_ [_Full-featured Help generator_](http://www.helpndoc.com/feature-tour)

**附录：错误代码**

在使用Ceagle的过程中，会遇到因系统配置、软件配置、验证工程、环境等引起的异常情况，导致无法正常完成验证流程。

您可以将错误代码记录并反馈给清华大学以获取支持，反馈网址是：[http://sts.thss.tsinghua.edu.cn/ceagle/support](http://sts.thss.tsinghua.edu.cn/ceagle/help)。您在提交错误代码时，可以随附

各版本可能的错误代码如下。

| 序号 | 错误代码 | 说明 |
| --- | --- | --- |
|  | E1 | Ceagle没有正确安装 |
|  | E2 | 系统配置无法满足软件需求 |
|  | E10 | 预处理失败，Ceagle需要预处理才能正确验证 |
|  | E11 | 编译失败，项目中有文件无法被编译器编译 |
|  | E12 | 验证失败，超出时间限制 |
|  | E13 | 验证失败，超出内存限制 |
|  | E14 | 验证失败，内部错误，约束求解失败 |
|  | E15 | 验证失败，内部错误，其它错误 |

_Created with the Personal Edition of HelpNDoc:_ [_Easy CHM and documentation editor_](http://www.helpndoc.com)