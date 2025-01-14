＃ 问题陈述
我们相信 web3 开发正在迅速超越当今的智能合约语言和执行层。我们在今天的解决方案中看到的一些关键问题是：

1. **智能合约语言不是跨平台的。**
语言过度适合区块链的实现细节，例如交易和账户结构、签名/散列算法和共识算法。
这会阻碍互操作性，阻止智能合约重用，并阻止社区跨平台形成。
新平台的设计者面临着一个艰难的选择：要么引导一种全新的语言和生态系统，要么使用现有的语言（例如，Solidity/EVM），迫使你的新平台继承旧平台的许多限制。
去中心化的网络需要一种通用语，它允许平台创建者试验截然不同的架构，而无需为每个架构创建一种新语言。

2. **智能合约语言不够安全。**
数百万美元的漏洞利用是 [常规](https://rekt.news/) 事件。
有效的智能合约开发人员必须是安全和产品方面的专家。
语言设计错误（例如，重入、访问控制功能不足、无声整数溢出）增加了合约的攻击面，使审计变得昂贵且缓慢，并阻碍了形式验证的采用。
我们认为，语言安全性不足是数字资产主流采用和可访问智能合约开发的严重障碍。

3. **智能合约执行层并不快。**
在大多数平台中，事务执行是顺序的和低吞吐量的。
对此进行改进具有挑战性，因为现有语言在设计时并未考虑到并行执行的顺从性。
此外，大多数语言具有非常规的特性（例如，不适合寄存器的大默认整数，基于无数据局部性的抗冲突散列的集合），这些特性阻碍了有效提前或 JIT 编译等改进本机代码。
吞吐量不足将 gas 价格推到了荒谬的水平，并锁定了负担不起的用户/用例。

4. **不成熟的语言生态系统。**
语言不提供合约组合的功能，导致[大量代码重复](http://www.ifca.ai/fc20/preproceedings/106.pdf)并浪费昂贵的链上存储。
传统语言与专用包管理器保持一致（例如，用于 Rust 的 crates.io，用于 Python 的 JavaScript pip 的 npm）用于共享/构建代码、发布、错误修复、漏洞披露等，但智能合约语言不存在此类包管理器.
相反，开发人员手动复制/粘贴和调整流行的模板。
这种不成熟使得构建（也许更重要的是）维护大型应用程序变得困难。

5. **糟糕的最终用户体验。**
最终用户直接暴露于当今执行层中的设计错误。
像“查看我的账户拥有的所有资产”这样的基本操作需要扫描整个区块链或依赖第三方基础设施。
钱包要求用户签署内容（或效果）不易理解的不透明交易。这为盗窃尝试打开了大门，例如 [毒令牌](https://www.theblockcrypto.com/post/112339/creative-attacker-steals-76000-in-rune-by-giving-out-free-tokens) 或[欺骗令牌批准](https://www.theverge.com/2022/2/20/22943228/opensea-phishing-hack-smart-contract-bug-stolen-nft)。