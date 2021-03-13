                                                                      ## Flutter 介绍
                                                             ### 姓名：迪力胡玛·居马洪   学号：1813066
                                                             
Flutter是Google的UI工具包，用于从单个代码库构建漂亮的、本地编译的移动、web和桌面应用程序，并且它是完全免费、开源的。Flutter可以实现写一份代码同时运行在iOS和Android设备上，并且提供很好的性能体验。Flutter使用Dart作为开发语言，这是一门简洁、强类型的编程语言。Flutter对于iOS和Android设备，提供了两套视觉库，可以针对不同的平台有不同的展示效果。

Flutter特点：

快速发展
Flutter的热加载功能可以帮助开发者快速、轻松地试验、构建ui、添加功能，并更快地修复bug。在模拟器、模拟器和硬件上体验亚秒级的重新加载时间，而不会丢失状态。
表达,漂亮的用户界面
Flutter的内置漂亮的材料设计和Cupertino (ios风格)小部件，丰富的motion api，平滑的自然滚动，和平台感知，让用户高兴。
本机性能
Flutter的小部件整合了所有关键平台差异，如滚动、导航、图标和字体，从而在iOS和Android上提供完整的本机性能。

Flutter整体框架：

Flutter可以理解为开发SDK或者工具包，其通过Dart作为开发语言，并且提供Material和Cupertino两套视觉控件，视图或其他和视图相关的类，都以Widget的形式表现。Flutter有自己的渲染引擎，并不依赖原生平台的渲染。Flutter还包含一个用C++实现的Engine，渲染也是包含在其中的。

Engine
Flutter是一套全新的跨平台方案，Flutter并不像react Native那样，依赖原生应用的渲染，而是自己有自己的渲染引擎，并使用Dart当做Flutter的开发语言。Flutter整体框架分为两层，底层是通过C++实现的引擎部分，Skia是Flutter的渲染引擎，负责跨平台的图形渲染。Dart作为Flutter的开发语言，在C++引擎上层是Dart的Framework。

Flutter不仅仅提供了一套视觉库，在Flutter整体框架中包含各个层级阶段的库。例如实现一个游戏功能，上面一些游戏控件可以用上层视觉库，底层游戏可以直接基于Flutter的底层库进行开发，而不需要调用原生应用的底层库。Flutter的底层库是基于Open GL实现的，所以Open GL可以做的Flutter都可以。

视觉库
在上层Framework中包含两套视觉库，符合Android风格的Material，和符合iOS风格的Cupertino。也可以在此基础上，封装自己风格的系统组件。Cupertino是一套iOS风格的视觉库，包含iOS的导航栏、button、alertView等。

Flutter对不同硬件平台有不同的兼容，例如同样的Material代码运行在iOS和Android不同平台上，有一些平台特有的显示和交互，Flutter依然对其进行了区分适配。例如滑动ScrollView时，iOS平台是有回弹效果的，而Android平台则是阻尼效果。例如iOS的导航栏标题是居中的，Android导航栏标题是向左的，等等。这些Flutter都做了区分兼容。

除了Flutter为我们做的一些适配外，有一些控件是需要我们自己做适配的，例如AlertView，在Android和iOS两个平台下的表现就是不同的。这些iOS特性的控件都定义在Cupertino中，所以建议在进行App开发时，对一些控件进行上层封装。

例如AlertView则对其进行一个二次封装，控件内部进行设备判断并选择不同的视觉库，这样可以保证各个平台的效果。

虽然Flutter对于iOS和Android两个平台，开发有cupertino和material两个视觉库，但实际开发过程中的选择，应该使用material当做视觉库。因为Flutter对iOS的支持并不是很好，主要对Android平台支持比较好，material中的UI控件要比cupertino多好几倍。

Dart
Dart是Google在2011年推出的一款应用于Web开发的编程语言，Dart刚推出的时候，定位是替代JS做前端开发，后来逐步扩展到移动端和服务端。

Dart是Flutter的开发语言，Flutter必须遵循Dart的语言特性。在此基础上，也会有自己的东西，例如Flutter的上层Framework，自己的渲染引擎等。可以说，Dart只是Flutter的一部分。

Dart是强类型的，对定义的变量不需要声明其类型，Flutter会对其进行类型推导。如果不想使用类型推导，也可以自己声明指定的类型。

Hot Reload
Flutter支持亚秒级热重载，Android Studio和VSCode都支持Hot Reload的特性。但需要区分的是，热重载和热更新是不同的两个概念，热重载是在运行调试状态下，将新代码直接更新到执行中的二进制。而热更新是在上线后，通过Runtime或其他方式，改变现有执行逻辑。

AOT、JIT
Flutter支持AOT(Ahead of time)和JIT(Just in time)两种编译模式，JIT模式支持在运行过程中进行Hot Reload。刷新过程是一个增量的过程，由系统对本次和上次的代码做一次snapshot，将新的代码注入到DartVM中进行刷新。但有时会不能进行Hot Reload，此时进行一次全量的Hot Reload即可。

而AOT模式则是在运行前预先编译好，这样在每次运行过程中就不需要进行分析、编译，此模式的运行速度是最快的。Flutter同时采用了两种方案，在开发阶段采用JIT模式进行开发，在release阶段采用AOT模式，将代码打包为二进制进行发布。

在开发原生应用时，每次修改代码后都需要重新编译，并且运行到硬件设备上。由于Flutter支持Hot Reload，可以进行热重载，对项目的开发效率有很大的提升。

由于Flutter实现机制支持JIT的原因，理论上来说是支持热更新以及服务器下发代码的。可以从服务器。但是由于这样会使性能变差，而且还有审核的问题，所以Flutter并没有采用这种方案。

 
