 ECMH 
 =
 Elliptic Curve Diffie-Hellman(ECDH)算法是基于椭圆曲线密码学的密钥交换算法，与传统的Diffie-Hellman算法相比，ECDH算法具有更高的安全性和更短的密钥长度。

**步骤:**    
1.首先，每个通信方会选择一对公钥和私钥，这些密钥是基于椭圆曲线的算法生成的。每个通信方都会将其公钥发送给对方。  
⒉接下来，每个通信方会使用对方的公钥和自己的私钥计算一个共享密钥。这是通过将对方的公钥和自己的私钥相乘得到的。
由于椭圆曲线的离散对数问题的复杂性，其他人无法从这个结果中计算出通信方使用的私钥。  
3.最后，通信方将这个共享密钥用于对称加密算法，例如AES，来加密和解密他们之间的通信。  


关键代码实现：  
![image](https://github.com/yxh1120/Homework-group-41/blob/main/Project%2013/2.png)

**应用**  
SSL/TLS协议：SSL/TLS协议作为加密通信的基础，使用ECDH算法进行密钥交换，保证通信过程中的数据机密性和完整性。  
数字签名：数字签名是一种将数字信息和用于检测其真实性和完整性的数据保护码（数字签名）相结合的技术。使用椭圆曲线数字签名算法(ECDSA)可以确保数字签名的正确性和安全性。  
区块链：区块链通过使用非对称加密算法来确保数字货币的安全性，而ECDH算法作为其中一种加密算法，可以使得区块链更加安全且高效。  

运行结果如图：  
![image](https://github.com/yxh1120/Homework-group-41/blob/main/Project%2013/1.png)

运行速度：  进行一次运算约消耗0.02秒

实验环境： IDLE (Python 3.10 64-bit)