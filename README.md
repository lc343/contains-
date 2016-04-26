# contains()方法
contains.html
使用contains()方法来检测参考节点和要检查的节点间的关系。
文中该函数使用了三种组合方式来确定一个节点是不是另一个节点的后代。函数的第一个参数是参考节点，第二个参数是要检查的检点。
在函数体内，首先是能力检测，检测refNode中是否存在contains()方法，并且还检查了当前浏览器所用的webkit版本号。若方法存在而且不是Webkit则继续执行代码。
否则，若浏览器是Webkit且至少是safari3(Webkit版本号为522或更高)，则继续执行代码，否则contains()方法不能正常进行。
第二步，检查是否存在compareDocumentPosition()方法
否则第三步，有otherNode向上遍历DOM结构，以递归方式取得parentNode,检查是否与refNode相等，在文档树顶端，parentNode值为null时，停止搜索。

client.js
完整的用户代理字符检测脚本，包括检测呈现引擎，平台，Windows，mac,unix操作系统，移动设备和游戏系统。
