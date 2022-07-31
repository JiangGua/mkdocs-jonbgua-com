# 帮助

本页是酱瓜的经验手记。



## 加密插件相关

### 隐藏 [Protected] 前缀

默认情况下，被加密的文章标题会自动加一个前缀。在 mkdocs.yml 中的对应位置增加一个空的 title_prefix 参数即可：

```yaml
plugins:
  - encryptcontent:
  	title_prefix: ' '
```



### 全局加密时某篇文章不需要加密

在该文章的 Markdown 文件一开头加入下面几行即可：

```
---
password: ''
---
```

似乎被加密的 Jupyter Notebook 不能用这个办法解除。