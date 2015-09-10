STP协议笔记
==

STP操作
--
###选择根桥
* 选择根端口
* 选择候选端口
* 禁止其他端口

	网桥id:priority(4bits)+system id extension(12bits)+mac(48bits);
	端口id:(4bits)+id(interface number)(12bits);


端口类型:
--
* 根端口
* 后选端口
* 阻塞端口

端口状态:
--
* Blocking:
	不参与转发数据。接受BPDU报文。参与STP的计算。
* Listening:
	处理BPDU报文.不填写mac地址，不转发数据
* Learning:
	填写mac地址,不转发数据帧
* Frowarding:
	转发数据并处理BPDU
* Diabled:
	不参与BPDU的处理


BPDU:
--
	源mac: 发送端口mac
	目的mac: 01:80:c2:00:00:00
	报文类型:CBPDU(配置),TCN(拓扑改变)

