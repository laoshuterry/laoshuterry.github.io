# 利用HEXO构建的个人博客
从2014年起就开始搭建和使用博客。先后折腾了**Octopress**，**Jekyll**，**Wordpress**和目前使用的**Hexo**。**Jekyll**是Github Pages官方推荐的框架，使用也很广泛，但是搭建一个完整的博客其实是有些复杂的，而且其使用的脚本语言是**Ruby**，个人不是很喜欢，这也意味着以后做扩展的空间不是很大，所以放弃了。**Octopress**是在Jekyll上做了进一步封装，使用起来方便了一些，而且网上支持也较多。可是使用了一段时间，总觉得生成页面速度有点慢。直到一次买了个VPS，在搭建其他服务的同时，索性搭建了一套Wordpress作为个人博客。**Wordpress**不用多说，超级强大的博客专业写作工具了，能让人专心写作而不用去做过多的配置。最后放弃的原因是购买的VPS是国外的，由于网络环境的关系速度一直不稳定。最后还是决定迁回到Github Pages，同时更换了一个使用Nodejs的框架**Hexo**，这个博客就诞生了。

具体的安装过程网上有很多，这里不再累述，主要是参考**Hexo的官方网站**和**Next主题**的说明，仔细阅读以后不难搭建。
>* [Hexo](https://hexo.io/)
>* [Next](http://theme-next.iissnan.com/)

这里说几点在搭建时注意的事项：
1. 博客框架基于Nodejs，所以要确保系统里有。在Ubuntu系统中，不要使用`apt-get`方法来获得。Ubuntu包管理库中的Nodejs版本较老，直接安装的Nodejs是不能成功搭建的。
2. 安装**Hexo**时，请使用`sudo npm install -g hexo --no-optional`。一定要有后面的参数选项，否则后面运行hexo时会出错。
3. 在搭建好博客后，我们可能还会要安装一些扩展，例如用`hexo-generator-sitemap`来生成**sitemap.xml**文件，或者`hexo-generator-feed`来生成**atom.xml**文件等。在安装扩展时，要使用命令`npm install hexo-generator-sitemap --save`，只有加上`--save`后面的参数，新增加的扩展才能被记录在**packages.json**文件中，从而正确的生成文件。
4. Hexo不是直接将**Markdown**文件推送到Github Pages中，而是根据**md**文档生成相应的网页文件，然后将网页文件推送到Github上。所以为了方便跨平台使用和安全性着想，个人建议最好能够对**_posts**文件夹使用git来管理。

目前博客还是有些不完善的地方，有待以后慢慢折腾，这里先记一下：
1. 使用自定义LOGO和font-icon。目前还不知道怎么增加。
2. 添加图片流扩展，使得博客中能够显示其他图片社交网站的图片流。

>**参考网站：**

>* [Hexo搭建Github静态博客](http://www.cnblogs.com/zhcncn/p/4097881.html)
