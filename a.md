# 漫画：什么是加密算法？

> 文章来自：程序员小灰  
> 作者：小灰

![640?wx_fmt=jpeg](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_jpg/NtO5sialJZGp9TT0Ekj0yafjpHfyGy9S6ZD9J85I6P8dxicQb9Lye7zdgSW0Xt9FdfQUFH8EBKoV7P0C4aTIASAg/640?wx_fmt=jpeg)

![640?wx_fmt=jpeg](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_jpg/NtO5sialJZGp9TT0Ekj0yafjpHfyGy9S6rxNH3NibToZpLc0ljjicQA0SxAAcZfV6icu41W6LMjkia20Hb7kMsrnIeA/640?wx_fmt=jpeg)

![640?wx_fmt=jpeg](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_jpg/NtO5sialJZGp9TT0Ekj0yafjpHfyGy9S6qM71ibkvDvpDRAd3ic9PoHFQ9VNokL9ko9Oac9LBJGicLTslTaRzqO8Ow/640?wx_fmt=jpeg)

![640?wx_fmt=jpeg](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_jpg/NtO5sialJZGp9TT0Ekj0yafjpHfyGy9S6CM3GxxcEqwkicc86pYsiaR63mYjqibsEwRGp0oicxSj0GicSNgCnssjs1GQ/640?wx_fmt=jpeg)

![640?wx_fmt=jpeg](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_jpg/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xScqe8jpZ1icXVNiaiamblaRMkY6kjwp5aZpf3HOSI8DlRlm9pWmwooicmFg/640?wx_fmt=jpeg)

![640?wx_fmt=jpeg](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_jpg/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xSH4ib5ZibFErVSo64hF78WOOTnOn9npY4z6ahlWLhP5NKyH3F5t29AMibw/640?wx_fmt=jpeg)

## 加密算法的历史

加密算法最早诞生在什么时候？是在计算机出现之后吗？不不不，早在古罗马时期，加密算法就被应用于战争当中。

![640?wx_fmt=png](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_png/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xSsatYQLu60JAXhxOuDZPuzxygm97BHggUVicx03qdickAw1fIzwWHL75A/640?wx_fmt=png)

在大规模的战争中，部队之间常常需要信使往来，传递重要的军事情报。

![640?wx_fmt=png](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_png/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xSC3A5HyOtN3fgoXMHCctKFd3PUV8eYm7zC8wpXXnpia5GGFFFaDZK5eQ/640?wx_fmt=png)

可是，一旦信使被敌军抓获，重要的军事情报就完全暴露给了敌方。

![640?wx_fmt=png](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_png/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xSC7P2vD7vO0KEGD0zawfPviaaVHug73Siazm332ymVxZq5LHq3uWqdhicg/640?wx_fmt=png)

甚至，狡猾的敌人有可能篡改军事情报，并收买信使把假情报传递给我方部队。

![640?wx_fmt=png](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_png/NtO5sialJZGoolYsx25YgAl2ALXjYJlRGVUuicZaiaq1ibrzTJlQia0NsUrKpu1ckWUqQrS2edfhEr8CMCEbKjA28fQ/640?wx_fmt=png)

这样一来，我方部队就完全落入到了敌方的陷阱之中。这种拦截并篡改信息的手法，在网络安全领域被称为**中间人攻击**。

怎样防止这种情况的发生呢？不让信使被敌人抓获？这个肯定是无法绝对避免的。

那么我们不妨换个角度，让敌人即使截获了军事情报，也看不懂里面的内容，这就是对信息的**加密**。

![640?wx_fmt=png](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_png/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xSxx1siaaHJCO6nRicticfoiafStze7sMmsLDODn5KeUWA95Wj4uFgV5rt1g/640?wx_fmt=png)

如何进行加密呢？古人想出了一种非常朴素的加密方法，被称为**凯撒密码**。加密的原理就像下图这样：

![640?wx_fmt=png](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_png/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xS7jC5lichssHmO7uz1gJ6LReyvQ9iavicpaiadonibVbS0lOJCgfFy9DkkKw/640?wx_fmt=png)

如图所示，图中第一行的字母代表信息的“明文”，第二行字母代表信息的密文。这个加密算法十分简单，就是选择一个偏移量（这里的偏移量是 2），把明文当中的所有字母按照字母表的顺序向后偏移两位，从而生成密文。比如：

原文的字母**A**，对应的密文是字母**C**。

原文的字母**D**，对应的密文是字母**F**。

原文的单词**Java**，对应的密文是**Lcxc**。

这样一来，敌方看到信使的情报内容，就彻底蒙逼了。相应的，我军事先约定好了密文通信的偏移量，当友军收到情报以后，把密文的所有字母向前偏移两位，就还原成了明文，这个过程叫做**解密**。

但是，这种加密方法真的百分百保险吗？并不是。

在英语的 26 个字母中，出现频率最高的字母是**e**。如果敌人截获了情报，发现这段看不懂的密文当中出现频率最高的字母是 g，由于 e 和 g 相差两个字母，就可以猜测出我军的密文通信很可能选择 2 作为偏移量。这样一来，我军的密码就被破解了。

最不济，敌人可以把每一种偏移量都尝试一遍（26 个字母，最多 25 种偏移），终究可以试出符合正常语法的偏移量。这种方式被称为**暴力破解**。

![640?wx_fmt=jpeg](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_jpg/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xSdEMXg55G9bmm2ia5S1Hv2htz5cXCwiaUiaqzZVfspzA4y7l0sibWlPCQlA/640?wx_fmt=jpeg)

![640?wx_fmt=jpeg](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_jpg/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xSSnuQONsbmpibPYOQMLTCTNqNGENJD1CFxwvJtQmzrAwxckrMjQUslzA/640?wx_fmt=jpeg)

## 加密算法的种类

在如今的信息安全领域，有各种各样的加密算法凝聚了计算机科学家门的智慧。从宏观上来看，这些加密算法可以归结为三大类：**哈希算法、对称加密算法、非对称加密算法。**

### 1.哈希算法

从严格意义上来说，**哈希算法并不属于加密算法**，但它在信息安全领域起到了很重要的作用。

哈希算法能做什么用呢？其中一个重要的作用就是**生成信息摘要**，用以验证原信息的完整性和来源的可靠性。

让我们来举个栗子：

在某个互联网应用上，有用户下单买了东西，于是应用需要通知支付宝，并告诉支付宝商户 ID、支付金额等等信息。

![640?wx_fmt=png](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_png/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xSnnFp6t8wpf6FEWDQsxFAicmDE8fTSxksorw8RUvsJFvd1cOREPTic3pQ/640?wx_fmt=png)

支付宝怎么知道这个请求是真的来自该应用，并且没有被篡改呢？

请求的发送方把所有参数，外加双方约定的 Key（例子中 Key=abc）拼接起来，并利用哈希算法生成了一段信息摘要：

**Hash（1234_100_abc） = 948569CD3466451F**  
</br>
而请求的接收方在接到参数和摘要之后，按照同样的规则，也把参数和 Key 拼接起来并生成摘要：

**Hash（1234_100_abc） = 948569CD3466451F**  
</br>
如果最终发现两端信息摘要一致，证明信息没有被篡改，并且来源确实是该互联网应用。（只要参数修改了一点点，或者 Key 不一样，那么生成的信息摘要就会完全不同）

生成信息摘要的过程叫做**签名**，验证信息摘要的过程叫做**验签**。

哈希算法包含哪些具体的算法呢？其中最著名的当属**MD5 算法**。后来，人们觉得 MD5 算法生成的信息摘要太短（128 位），不够安全，于是又有了**SHA 系列算法**。

### 2.对称加密算法

哈希算法可以解决验签的问题，却无法解决明文加密的问题。这时候，就需要真正的加密算法出场了。

什么是对称加密呢？这个概念很好理解：

![640?wx_fmt=png](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_png/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xSSh6r7JI6ol6FNg3EjFdSf7G6bliaXAicoN3EYBCV3V80F3gYa4M6OshA/640?wx_fmt=png)

如图所示，一段明文通过密钥进行加密，可以生成一段密文；这段密文通过同样的密钥进行解密，可以还原成明文。这样一来，只要双方事先约定好了密钥，就可以使用密文进行往来通信。

除了通信过程中的加密以外，数据库存储的敏感信息也可以通过这种方式进行加密。这样即使数据泄露到了外界，泄露出去的也都是密文。

对称加密包含哪些具体的算法呢？在早期，人们使用**DES 算法**进行加密解密；后来，人们觉得 DES 不够安全，发明了**3DES\*\***算法**；而如今，最为流行的对称加密算法是**AES 算法\*\*。

不知道读者中有多少人曾经接触过欧盟的 GDPR 法案，为了遵从该法案，有的企业就曾经将数据库中的敏感信息使用 3DES 进行加密。

总而言之，对称算法的好处是加密解密的效率比较高。相应的，对称算法的缺点是不够安全。为什么呢？通信双方约定的密钥是相同的，只要密钥本身被任何一方泄露出去，通信的密文就会被破解；此外，在双方建立通信之初，服务端把密钥告诉给客户端的时候，也有被拦截到的危险。

为了解决这一痛点，非对称加密就登场了。

#### 3.非对称加密算法

**3.非对称加密算法**  </br>

什么又是非对称加密呢？在刚刚接触到的时候，或许你会觉得这种算法有些古怪：

![640?wx_fmt=png](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_png/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xS6sEuUrXdyv0ZOfVfibGj2P0YnNf06HlGFmcdIdG4hpvkgzRMn7I5FHg/640?wx_fmt=png)

如图所示，在非对称加密中存在一对密钥，其中一个叫做**公钥**，另一个叫做**私钥**。在加密解密的过程中，我们既可以使用公钥加密明文，使用私钥解密密文；也可以使用私钥加密明文，使用公钥解密密文。

这样设计有什么好处呢？看看通信的过程就知道了：

1.在双方建立通信的时候，服务端只要把公钥告诉给客户端，自己保留私钥。

2.客户端利用获得的公钥。加密另外一个密钥 X（可以是对称加密的密钥），发送给服务端。

3.服务端获得消息后，用自己的私钥解密，得到里面隐含的密钥 X。

4.从此以后，双方可以利用密钥 X 进行对称加密的通信了。

![640?wx_fmt=png](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_png/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xSpHEwDSuVJjibzdyTlibicP2J9bl2yZkH9SKb7C6ga4KqyAdNt754SM3ag/640?wx_fmt=png)

在这个过程中，即使公钥被第三方截获，甚至后续的所有通信都被截获，第三方也无法进行破解。因为第二步利用公钥加密的消息，只有私钥才能解开，所以第三方永远无法知道密钥 X 是什么。

非对称加密算法的代表有哪些呢？最著名的当属**RSA 算法**。

既然非对称加密这么强大，是不是没有缺点呢？也不是。非对称加密最大的问题，就是性能较差，无法应用于长期的通信。

![640?wx_fmt=jpeg](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_jpg/NtO5sialJZGoolYsx25YgAl2ALXjYJlRGvQZ4ZQyV3ROEia3UGxDdO5icAXYicE5jg8RyjeW9MLvyw1orKbyaIgTtA/640?wx_fmt=jpeg)

![640?wx_fmt=jpeg](https://ss.csdn.net/p?https://mmbiz.qpic.cn/mmbiz_jpg/NtO5sialJZGpWg5ia0lYhTYWbo3SAhA6xS41fVICZ6LwT4zAAlO8tSENkGslsUosOsiczaMIVIjbTiagt3OZ7bP9BA/640?wx_fmt=jpeg)

关于加密算法，小灰之前曾经写过一部分相关漫画，没看过的小伙伴可以看看哦：

[漫画：什么是 MD5 算法？](http://mp.weixin.qq.com/s?__biz=MzIxMjE5MTE1Nw==&mid=2653191503&idx=1&sn=b18bd0458bf884bcb5d01f1cf2ca8301&chksm=8c990f95bbee8683fcfa9e972fd887cb1e50328ab4d8bd1f6a68ea90de6c67f46e50847e36fb&scene=21#wechat_redirect)

[漫画：如何破解 MD5 算法？](http://mp.weixin.qq.com/s?__biz=MzIxMjE5MTE1Nw==&mid=2653191598&idx=1&sn=13ef6b99b8a9a25f18b839df13cd6e31&chksm=8c990f74bbee866249af65e56a73f74b90a85b8497b9eea097f813a0b398a44fe0b8320967cd&scene=21#wechat_redirect)

[什么是 AES 算法？（整合版）](http://mp.weixin.qq.com/s?__biz=MzIxMjE5MTE1Nw==&mid=2653191726&idx=1&sn=c7856fe211471d01e9afdfea4a7f6b87&chksm=8c990cf4bbee85e28bb2ea63cb1f767dee4702ca8b9ef23db3467558a4b27ff5b6c1893c8771&scene=21#wechat_redirect)
