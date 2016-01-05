### babel-ie10-polyfill

* 问题应该是babel升级到6.0以上之后导致的，不支持在IE10及以下正常使用extends

* 问题出在当B继承自A的时候，实例化B的时候，A的constructor不会被调用

* 这好像是IE10及以下Object不支持setPrototypeOf方法导致的，而Object.getPrototypeOf也不足够完善

### 使用方法

#### webpack

* 在entry里添加对babel-ie10-polyfill的引入