# Awesome Move 中文版 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 来自 [Move](https://github.com/move-language/move) 编程语言社区的代码和内容精选列表。

Move 是一种用于编写安全智能合约的编程语言，最初由 Facebook 开发，用于为 Libra 区块链提供支持。 Move 旨在成为一种与平台无关的语言，以使通用库、工具和开发人员社区能够跨具有截然不同的数据和执行模型的不同区块链。 Move 的目标是成为无处不在的“web3 的 JavaScript”——当开发人员想要快速编写涉及资产的安全代码时，应该使用 Move 编写。

## 内容

- [Awesome Move 中文版 ![Awesome](https://awesome.re)](#awesome-move-中文版-)
  - [内容](#内容)
  - [概述](#概述)
  - [移动驱动的区块链](#移动驱动的区块链)
  - [书籍](#书籍)
  - [教程](#教程)
  - [社区](#社区)
  - [代码](#代码)
    - [可替代代币](#可替代代币)
    - [不可替代的代币](#不可替代的代币)
    - [DeFi](#defi)
    - [链上治理](#链上治理)
    - [帐户](#帐户)
    - [框架](#框架)
    - [库](#库)
    - [杂项](#杂项)
  - [工具](#工具)
  - [IDE](#ide)
  - [钱包](#钱包)
  - [论文](#论文)
    - [语言设计](#语言设计)
    - [静态分析和验证](#静态分析和验证)
  - [视频](#视频)
  - [贡献](#贡献)

## 概述

- [安装](https://github.com/move-language/move/tree/main/language/tools/move-cli#installation)
- [问题陈述](docs/problem_statement.md)

## 移动驱动的区块链

- [Sui](https://github.com/MystenLabs/sui) (在 [devnet](https://medium.com/mysten-labs/sui-devnet-public-release-a2be304ff36b))
- [0L](https://github.com/OLSF/libra) (在 [mainnet](https://0l.network/))
- [星币](https://github.com/starcoinorg/starcoin) (在[主网](https://stcscan.io/))
- [Pontem](https://github.com/pontem-network) (在 [testnet](https://polkadot.js.org/apps/?rpc=wss://testnet.pontem.network/ws#/explorer)）
- [Aptos](https://github.com/aptos-labs) (在 [testnet](https://aptos.dev/))
- [Celo](https://github.com/celo-org) ([即将推出](https://www.businesswire.com/news/home/20210921006104/en/Celo-Sets-Sights-On-Becoming-Fastest-EVM-Chain-Through-Collaboration-With-Mysten-Labs))

## 书籍

- https://move-language.github.io/move/ - 由 Move 核心团队维护。
- https://move-book.com/ - 由 [@damirka](https://github.com/damirka) 维护。

## 教程

- [实施、测试和验证可替代代币](https://github.com/move-language/move/tree/main/language/documentation/tutorial) - 由 Move 核心团队维护。

## 社区

- [移动@Mysten Labs Discord](https://discord.gg/M95qX3KnG8)
- [移动语言不和谐](https://discord.gg/9K7ca8Vnr7)
- [Move @ 0L Discord](https://discord.gg/zzXzhbE3aN)
- [移动@Starcoin Discord](https://discord.gg/starcoin)

## 代码

用 Move 编写的代码。

### 可替代代币

- [可替代代币示例](https://github.com/MystenLabs/sui/tree/main/sui_programmability/examples/fungible_tokens)。来自隋。
- [BasicCoin](https://github.com/move-language/move/tree/main/language/documentation/examples/experimental/basic-coin) - [ERC20](https://ethereum) 的玩具实现.org/en/developers/docs/standards/tokens/erc-20/) 类似的可替代令牌。
- [Diem](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/Diem.move) - 一种类似 ERC20 的代币，具有许可铸造/燃烧，另请参阅此 [规范](https://github.com/diem/dip/blob/main/dips/dip-20.md)。部署在 0L 上。
- [代币](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Token.move)- 另一个类似 ERC20 的代币。部署在星币上。
- [GAS](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/GAS.move) - 实例化上述 Diem 标准的令牌。部署在 0L 上。
- [STC](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/STC.move) - 实例化上述星币标准的代币。部署在星币上。
- [WEN 稳定币](https://github.com/wenwenprotocol/wen-protocol) - 部署在 Starcoin 上。
- [FAI 稳定币](https://github.com/BFlyFinance/FAI) - 部署在 Starcoin 上。
- [FLY stablecoin](https://github.com/BFlyFinance/FLY) - 在 Move 中实现的 [Ohm](https://www.olympusdao.finance/) 的分叉。部署在星币上。
- [由包含其他代币储备的篮子支持的合成代币](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/XDX.move) - 来自 Diem。

### 不可替代的代币

- [NFT 示例](https://github.com/MystenLabs/sui/tree/main/sui_programmability/examples/nfts)。来自隋。
- [NFT](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/NFT.move) - 类似 ERC721 的代币。部署在星币上。
- [Merkle Airdrop](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/MerkleNFT.move) - 用于空投大量 NFT 的实用程序。部署在星币上。
- [NFT](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/NFT.move) - 混合 ERC721/ERC1155 类令牌的实现。来自迪姆。
- [BARS](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/BARS.move) - 实例化此混合标准的 NFT。来自迪姆。
- [MultiToken](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/MultiToken.move) - 类似 ERC1155 的令牌。来自迪姆。
- [NFTGallery](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/NFTGallery.move) - 保存多个相同类型的 NFT 的实用程序。来自迪姆。

### DeFi

- [DeFi 示例](https://github.com/MystenLabs/sui/tree/main/sui_programmability/examples/defi)。来自隋。
- [CoinSwap](https://github.com/move-language/move/tree/main/language/documentation/examples/experimental/coin-swap) - [Uniswap](https://uniswap.org/) 的玩具实现。 类似的流动性池，包含两个代币。
- [StarSwap](https://github.com/Elements-Studio/starswap-core) - Uniswap 风格的 DEX。部署在星币上。
- [Offer](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/Offer.move) - 任何一对资产的原子交换的通用实现。

### 链上治理

- [ValidatorUniverse](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/ValidatorUniverse.move) - 验证器集管理。部署在 0L 上。
- [Oracle](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/Oracle.move) - 用于链上社区投票。部署在 0L 上。
- [DAO](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Dao.move) - 用于链上提案和投票。部署在星币上。
- [DiemSystem](https://github.com/diem/diem/blob/main/diem-move/diem-framework/DPN/sources/DiemSystem.move) - 验证器集管理。来自迪姆。
- [投票](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/Vote.move) - 链上投票。来自迪姆。
  
### 帐户

- [帐户](https://github.com/diem/diem/blob/main/diem-move/diem-framework/core/sources/Account.move) - Diem 驱动链的通用帐户。来自迪姆。
- [DiemAccount](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/DiemAccount.move) - 以上的分叉。从 0L。
- [帐户](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Account.move) - 上述的分叉。来自星币。

### 框架

Move **framework** 是包含在链的创世状态中的一组 Move 模块。
这些模块通常实现诸如账户、货币等关键概念。
将特定于区块链的框架逻辑与 Move 语言的通用功能分离的能力是 Move 平台无关设计的关键部分。

- [Sui 框架](https://github.com/MystenLabs/sui/tree/main/crates/sui-framework)
- [Aptos 框架](https://github.com/aptos-labs/aptos-core/tree/main/aptos-move/framework)
- [0L 框架](https://github.com/OLSF/libra/tree/main/language/diem-framework/modules/0L)
- [星币框架](https://github.com/starcoinorg/starcoin-framework)
- [Diem 框架](https://github.com/diem/diem/tree/main/diem-move/diem-framework/DPN)

### 库

- [Move 标准库](https://github.com/move-language/move/tree/main/language/move-stdlib) - 旨在（但不是必需）在每个运行 Move 的平台中使用的实用程序。来自 Move 存储库。
- [Move Nursery](https://github.com/move-language/move/tree/main/language/move-stdlib/nursery) - 最终可能被提升为标准库的实验模块。来自 Move 存储库。
- [十进制](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/Decimal.move) - 十进制值的有效实现。从 0L。
- [数学](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Math.move) - 数学实用函数。来自星币。
- [比较](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/Compare.move) - 多态比较（即比较任意两个移动值同类型）。从托儿所。
- [Vault](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/Vault.move)和[ACL](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/ACL.move)- 用于功能和基于列表的访问控制的库。从托儿所。
- [TaoHe](https://github.com/taoheorg/taohe) - 可嵌套的 Move 资源集合。
- [Starcoin Framework Commons](https://github.com/starcoinorg/starcoin-framework-commons) - Starcoin-framework 上 Move commons 实用程序的库。来自星币。

### 杂项

- [Move-on-EVM](https://github.com/move-language/move/tree/main/language/evm/examples) - 项目编译 Move 源代码到 EVM 字节码的实验示例。

## 工具

- [移动包管理器](https://github.com/move-language/move/tree/main/language/tools/move-cli) - 像移动的`cargo`或`npm`：单个CLI（和相应的用于构建、运行、测试、调试和验证 Move [包](https://move-language.github.io/move/) 的其他工具的 Rust API。由 Move 核心团队维护。
- [Move Prover](https://github.com/move-language/move/tree/main/language/move-prover) - 用 Move 源代码编写的用户定义规范的形式化验证。由 Move 核心团队维护。
- [移动读/写集分析器](https://github.com/move-language/move/tree/main/language/tools/read-write-set) - 用于计算全局内存过度逼近的静态分析工具被移动程序触动。由 Move 核心团队维护。

## IDE

- Move vscode 插件（[安装](https://marketplace.visualstudio.com/items?itemName=move.move-analyzer)，[源代码](https://github.com/move-language/move/tree/main/language/move-analyzer)) - 由 Move 核心团队维护。
- Move语法 vscode 插件：基于上下文的移动语法高亮（[安装](https://marketplace.visualstudio.com/items?itemName=damirka.move-syntax)，[源代码](https://github.com/damirka/vscode-move-syntax)) - 由 [@damirka](https://github.com/damirka) 维护。
- Move IntelliJ 插件 ([安装](https://plugins.jetbrains.com/plugin/14721-move-language), [源代码](https://github.com/pontem-network/intellij-move))
- [Move Playground](https://playground.pontem.network/) - 与 Move 的 [Remix](https://remix.ethereum.org/) 类似——Web IDE 的 alpha 版本。请参阅[说明](https://gist.github.com/borispovod/64b6d23741d8c1f4b0b958a3a74aa68d)。由 Pontem 团队维护。

## 钱包

- StarMask ([安装](https://chrome.google.com/webstore/detail/starmask/mfhbebgoclkghebffdldpobeajmbecfk?hl=en), [源代码](https://github.com/starcoinorg/starmask-extension)) - Starcoin 区块链的钱包。由 Starcoin 团队维护。
- [bcs-js](https://github.com/pontem-network/lcs-js) - Move 使用的 [BCS](https://github.com/diem/bcs) 序列化方案的 JavaScript 实现，可能对实现钱包有用。

## 论文

### 语言设计

- [移动：具有可编程资源的语言](https://developers.diem.com/papers/diem-move-a-language-with-programmable-resources/2019-06-18.pdf) - 这是原文2018 年发布的 Move 白皮书。其中的许多方面现在已经过时（例如，字节码指令的语法和描述），但前两节值得一读，以解释使用资产进行编程的困难以及 Move 如何解决他们。
- [强大的移动安全](https://arxiv.org/abs/2110.05043)
- [移动借贷检查器](https://arxiv.org/abs/2205.05181)
- [资源：货币的安全语言抽象](https://arxiv.org/abs/2004.05106)

### 静态分析和验证

- [使用 Move Prover 对智能合约进行快速可靠的形式验证](https://arxiv.org/abs/2110.08362)
- [移动证明者](https://research.facebook.com/publications/the-move-prover/)
- [验证用 Libra 的 Move 语言编写的程序]([https://ethz.ch/content/dam/ethz/special-interest/infk/chair-program-method/pm/documents/Education/Theses/Constantin_M%C3%BCller_MS_Report.pdf](https://ethz.ch/content/dam/ethz/special-interest/infk/chair-program-method/pm/documents/Education/Theses/Constantin_M%C3%BCller_MS_Report.pdf))
- [精确和线性时间 Gas-Cost 分析](https://research.facebook.com/publications/exact-and-linear-time-gas-cost-analysis/)

## 视频

- [Move：用钱编程的安全语言](https://www.youtube.com/watch?v=EG2-7bQNPv4&ab_channel=FieldsInstitute) - 来自  [@sblackshear](https://github.com/sblackshear) 的谈话) 在 [Fields Institute Blockchain](http://www.fields.utoronto.ca/activities/seminar_series/blockchain-research-seminar-series) 研究研讨会系列。
- [Libra 区块链移动程序的正式验证](http://www.fields.utoronto.ca/talks/Formal-verification-Move-programs-Libra-blockchain) - 来自 [@DavidLDill](https://github.com/DavidLDill) 在 [Fields Institute Blockchain](http://www.fields.utoronto.ca/activities/seminar_series/blockchain-research-seminar-series) 研究研讨会系列。

## 贡献

欢迎投稿！首先阅读[贡献指南](CONTRIBUTING.md)。