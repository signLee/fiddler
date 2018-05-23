# fiddler
fiddler use construction


配置：(配置抓取https链接)
tools--->options--->https--->勾选capture HTTPS CONNECTs（捕获https连接），decrypt HTTPS traffic（解密https流量），ignore server certificate errors（忽略https错误）

F12开始捕捉（默认是打开状态）
autoResponder：地址代理 将远程地址代理到本地路径  可用于将本地地址代理到测试地址
enable rules勾选->unmatched requests passthrough（不匹配允许通过）勾选
add rule:
EG:把百度的地址代理到本地文件
EXACT:https://www.baidu.com/  //访问地址
C:\Users\sign\Desktop\test.txt   //本地代理地址
save

composer本地发送请求
type:POST
http://test.msjk95596.com/rest/personnel/svr/v0/recruitinfo/page
设置Content-Type: application/json
request Body里输入入参
{
	"pageNo": 0, 
	"pageSize": 10,
	"jobType": "", 
	"status": "online"
}
execute调用接口
查看接口返回信息：
双击链接，Inspectors里是关于接口的各种信息，底部是接口返回的各种信息

火狐配置允许fiddler代理：设置->高级->网络->配置firfox如何连接到互联网--->使用系统代理设置

filters：过滤指定网站
EG:
如需要抓取https://www.xxxx.com/wxproduct/getProductLoanList这个链接的数据
Filter:
勾选use Filters
host里选内网还是外网 (www开头的为外网)
下面选择过滤条件
填写地址 ：www.xxxx.com
request header里勾选show only fi URL contains，填写接口名：wxproduct/getProductLoanList	
这样fiddler就只会抓https://www.xxxx.com/wxproduct/getProductLoanList这个链接的数据了


fiddler断点使用：F11  可以设置请求前断点或请求后断点 rules-----automatic breakoptions ---before request  一般配合filter使用
点击连接---------break on response-----textview里是返回的数据，修改好后点run to completion就实现了修改后台返回的数据

开启远程调试：允许抓取手机数据
tools----options------connections--allow remote computers to connect -----重启flddler
手机和PC必须在同一网段
手机设置：wifi----http代理---输入PC端的ip和端口号-----数据PC端ip地址和端口号-------下载证书安装---通用-设置-关于本机-----信任证书




