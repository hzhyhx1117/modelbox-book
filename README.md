# ModelBox介绍

## 什么是ModelBox

一个典型场景AI算法的商用落地除了模型训练外，还需要进行视频图片解码、HTTP服务、预处理、后处理、多模型复杂业务串联、运维、打包等工程开发，往往需要耗费比模型训练多得多的时间，同时算法的性能和可靠性通常随开发人员的工程能力水平高低而参差不齐，严重影响AI算法的上线效率。  

ModelBox是一套专门为AI开发者提供的易于使用，高效，高扩展的AI推理开发框架，它可以帮助AI开发者快速完成从模型文件到AI推理应用的开发和上线工作，降低AI算法落地门槛，同时带来AI应用的高稳定性和极致性能。

## ModelBox特点

||||
|:--:|:--:|:--:|
| ![indifference](assets/images/figure/flow/indifference.png) |![extend](assets/images/figure/flow/extend.png) | ![reliable](assets/images/figure/flow/reliable.png)|
|**易于开发**，AI推理业务可视化编排开发，功能模块化，丰富组件库；c++，python，java多语言支持。|**易于集成**，集成云上对接的组件，云上对接更容易。 |**高性能，高可靠**，pipeline并发运行，数据计算智能调度，资源管理调度精细化，业务运行更高效。 |
|![standard](assets/images/figure/flow/standard.png)|![integrated](assets/images/figure/flow/integrated.png)|![flow](assets/images/figure/flow/flow.png)|
|**软硬件异构**， CPU，ARM，GPU，NPU多异构硬件支持，资源利用更便捷高效。|**全场景**，视频，语音，文本，NLP全场景，专为服务化定制，云上集成更容易，端边云数据无缝交换。|**易于维护**，服务运行状态可视化，应用，组件性能实时监控，优化更容易。|

## ModelBox主要功能

| 功能              |      说明                                                     |
| ------------------ | --------------------------------------------------------    |
| 主要业务场景       | 快速完成AI推理业务的开发工作                                   |
| 支持数据类型       | 视频，图片，文字，通用数据，其他                                |
| 用户群             | 软件开发者，研究人员，学生，平台集成商                         |
| 跨平台             | 服务器， 边侧设备，嵌入式设备                                  |
| 图形化编排         | 支持模型的串联，支持视频流，音频流，图片等推理                   |
| API列表            | C++SDK, PYTHON SDK, JAVA SDK(暂未支持)                       |
| 支持OS             | Linux, andriod(暂未支持),iOS（暂未支持)                       |
| 支持硬件           | X86, ARM, GPU, Ascend, ...                                      |
| 图可视化           | 编排开发可视化图，子图                                        |
| 性能调测           | 性能跟踪                                                   |
| 图能力             |支持条件分支，循环分支，splice，reduce等图能力                   |
| 分布式             | 支持分布式图处理，分布式动态调整业务执行                       |
| 一次开发，多处运行  | PYTHON功能单元，C++功能单元，java功能单元（暂未支持)                 |
| 完善的功能单元        | 包含了大部分高性能的基础功能单元，包括http，视频，图像，云相关的功能单元|

## ModelBox解决的问题

目前AI应用开发时，训练完成模型后，需要将多个模型和应用逻辑串联在一起组成AI应用，并上线发布成为服务或应用。在整个过程中，需要面临复杂的应用编程问题：
  
|问题|问题说明|
|--|--|
|需要开发AI应用的周边功能|比如AI应用编译工程，应用初始化，配置管理接口，日志管理口，应用故障监控等功能。|
|需要开发AI常见的前后处理|音视频加解码，图像转换处理，推理前处理，后处理YOLO等开发。 |
|需要开发和云服务对接的周边功能|比如HTTP服务开发，云存储，大数据服务，视频采集服务对接开发。 |
|需要开发出高性能的推理应用|需要基于多线程，内存池化，显存池化，多GPU加速卡，模型batch批处理，调用硬件卡的API等手段开发应用。|
|需要开发验证docker镜像|需要开发docker镜像，集成必要的ffmpeg，opencv软件，cudamindsopre，tensorflow等软件，并做集成测试验证。|
|多种AI业务，需要共享代码，降低维护工作|需要复用不同组件的代码，包括AI前后处理代码，AI应用管理代码，底层内存，线程管理代码等。|
|模型开发者，验证模型功能比较复杂|模型开发者完成模型训练后，需要编写python代码验证，之后，再转成生产代码；在高性能，高可靠场景改造工作量大。|

ModelBox的目标是解决AI开发者在开发AI应用时的编程复杂度，降低AI应用的开发难度，将复杂的数据处理，并发互斥，多设备协同，组件复用，数据通信，交由ModelBox处理。开发者主要聚焦业务逻辑本身，而不是软件细节。 在提高AI推理开发的效率同时，保证软件的性能，可靠性，安全性等属性。
