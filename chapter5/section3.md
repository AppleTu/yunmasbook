# 5.3 二次开发接口常见问题

**1.A**:客户侧平台能否提前与API进行调试？  
**Q**:不能，如果OpenMAS服务器未安装启用，客户侧平台与API进行调测，一定报错。且短信需要计费也无法提供测试API。 

------------
**2.A**:OpenMAS中的扩展码是否有个数限制？  
**Q**:OpenMAS中可以在短信接入号的末尾继续添加扩展码，扩展码的添加个数没有限制。  
&nbsp;&nbsp;但是短信网关侧对号码长度是有限制，扩展码和短信接入号的总长度不能超过20位。  

------------
**3.A**:用户侧平台如何获取短信状态报告？  
**Q**:客户侧平台不需要主动获取状态报告，只需要发布一个WebService被动接受即可。OpenMAS会主动将状态报告发送到客户侧平台的WebService。  
&nbsp;&nbsp;客户侧平台发布一个WebService，然后把WebService链接地址告知一线维护工程师，由一线维护工程师配置到OpenMAS中；则当OpenMAS收到网关发来的回执时，就会自动向客户侧的WebService投递。  

------------
**4.A**:openmas能调到NotifySmsDeliveryReport，但是参数是null  
**Q**:客户侧接口方法参数大小写是否正确。  

------------
**5.A**:调用OpenMas信息机接口地址，返回值详解。  
**Q**:  

|返回值						|描述  
|:-------- 					|:--------  
|对不起，您没有相应的权限 	|接口密码错误  
|对不起，尚未定义应用 		|接口应用账户错误，或接口地址错误，或接口未开通  