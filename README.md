# JSPatch-Guide
[JSPatch](https://github.com/bang590/JSPatch) 调研笔记与使用教程  

### 技术选型
目前项目考虑热更新一些功能，就想到Hotfix的`JSPatch`，这个现在和基于 `lua` 的 [Wax](https://github.com/alibaba/wax)以及[WaxPatch](https://github.com/mmin18/WaxPatch) 思路应该类似。  

基于以下几个原因，选择研究 `JSPatch`：  
1. 之前在调研 [React-Native](https://github.com/ReactNativeGuide)  
2. 目前在学习 `Javascript` 学习地址: [FreeCodeCamp](https://www.freecodecamp.com)  
3. iOS7以后系统内建支持 `Javascript`（JavaScriptCore.framework）  
4. 使用 `lua` 也无法与 `Android` 端通用（都是映射相应的native方法的）  

### 调研方案
目前仅仅对 `JSPatch` 有了初步的了解，后续的主要研究方向为：  
1. 基础原理（js与oc通信原理以及patch原理等）  
2. 接口扩展以及使用三方库，比如网络库  
3. 降级方案及详细策略  
4. 开发可能会遇到的问题  

### 常用工具
<http://bang590.github.io/JSPatchConvertor/>


### 具体调研细节
-   [**JavaScriptCore** 调研](/JavaScriptCore/JSCGuide.md)
-   [**JSPatch** Detail 调研](/JSPatchDetail/JSPatchDetail.md)
-   [**开发可能会遇到的问题**](/DevelopDemo/DevelopDemo.md)

### 常见问题与解答 Q&A
##### 1. 重写的方法与原来的类型不对报错怎么办？
建议仔细看下作者写的替换的[原理](https://github.com/bang590/JSPatch/wiki/JSPatch-%E5%AE%9E%E7%8E%B0%E5%8E%9F%E7%90%86%E8%AF%A6%E8%A7%A3)，本身是没有问题的。  
目前不需要怀疑JSPatch的原理以及本身的问题，先检查一下重写原有方法的参数类型与你要重写的是否一致，一定要仔细检查，不要想当然。
