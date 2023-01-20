# PreventNotEndingParagraphUseUnity
## 介绍
> 此插件专门开发用于Unity程序，主要防止在双方交易金额较小，且甲方实在不结尾款的情况下使用。

## 如何使用？
  1. 将**PreventNotEndingParagraph.dll**复制粘贴到Unity项目工程**Asset/Plugin**目录下；
  2. 在Unity任意对象上添加`PreventNotEndingParagraphBrain`组件；
  3. 组件各属性描述:
  
     Field | Type | Description 
     ----- | ---- | ----------- 
     url|string|用于请求服务器数据的地址。
     outputCopyright|bool|要打印开发者版权信息吗?
     outputMasterSwitch|bool|输出调试信息的总开关。
     forceToExit|bool|当读取服务器数据不同意继续运行或未识别时，直接退出当前游戏。
     allowInfo|string|读取正确的信息。
     denyInfo|string|读取错误消息。
     getDataDelay|float|获取服务器数据的时间间隔。
     runtimePlatform|Enum|当前游戏运行平台。
     isIdentifiedData|bool|是否识别了服务器数据。
     
   4. 充分了解后，我们只需要在Server/Github/Giteee/COS（可以提供公有文件链接并且可以正常访问的平台）创建一个文本文件，并且将allowInfo或denyInfo其中一个的值输入进去保存；
   5. 我们将文件链接复制并粘贴到Unity组件url后面输入框内；
   6. 那么这样就可以正常调试了，只是在UnityEditor模式下并不能真正退出Play状态，考虑到在之后导出包的时候如果程序集,dll带有UnityEditor的调用方法代码都会报错导致不能正常导出，所以在Unity Editor测试只能通过Console输出信息来查看，在实机一切正常。
   
