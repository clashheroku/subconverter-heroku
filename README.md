# subconverter-heroku
subconverter自动部署到heroku
[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/tindy2013/heroku-subconverter)


步骤如下：

forksubconverter-heroku项目
添加Secret：HEROKU_API_KEY和HEROKU_EMAIL
修改heroku.yml里的heroku_app_name的值
点击Actions->点击heroku->点击Run workflow
部署后访问/version，如果出现subconverter v版本号 backend说明部署成功。

subconverter-后端
注意，订阅转换不代表协议转换，vemss节点不可能转成ssr，但是可以转成clash节点和ssr节点在一个软件中同时使用

简单用法看这里，target参考支持类型的最后一列参数。注意：原始订阅url必须要进行url转码！

转换结果不太妙：

clash -> ssr：失败（原因见后面）
v2ray -> ssr：失败（原因见后面）
ssr -> clash：成功
注意：

v2ray -> ssr：失败！为什么？因为ssr客户端只支持ss和ssr，它是不能处理v2ray的！所以转换失败！
clash -> ssr：失败！为什么？同样的原因！clash节点 大部分也都是 v2ray节点，ssr客户端是不能处理的！
ssr -> clash：成功。为什么？因为clash是后来出的客户端，它支持ss、ssr、v2ray、clash，clash客户端能支持这些协议，所以能转换。

sub-web-前端
sub-web：https://github.com/clashheroku/sub-web
sub-web是VUE开发的一个网页，没有后台，不要担心隐私泄露（subconverter后端是在页面上手动输入的）

可以从action的Artifacts下载最新版，解压即可使用。

推荐使用render来部署：创建Static Sites，输入github项目地址，设置生成文件目录为dist，自动部署后即可。

注意：绑定的链接必须是根路径，否则网页不展示！！
