# RollUpSample

モジュラーブロックチェーンで RollApp を開発してみるリポジトリです。

## 構築手順

docker コンテナを立ち上げていることが前提

```bash
curl -L https://dymensionxyz.github.io/roller/install.sh | bash
```

```bash
💈 Downloading roller...
######################################################################## 100.0%
💈 Installing roller...
💈 Installation complete! You can now use roller from your terminal.
```

バージョンの確認

```bash
roller version
```

```bash
💈 Roller version v1.0.6-beta
💈 Build time: 2024-01-18T09:01:52+0000"
💈 Git commit: 21b1b22e96466cc83b051ebacfb513b3a0d99de1
```

roller の初期化

```bash
roller config init --interactive
```

そうすると以下のようにアドレスが 3 種類出力される

froopyland 用のアドレスと celestia 用のアドレスが出力される。

```bash
 Total Token Supply: 1,000,000,000 MASH. Note that 1 MASH == 1 * 10^18 uMASH (like 1 ETH == 1 * 10^18 wei).

🔑 Addresses:

  Sequencer, froopyland_100-1    | dym1m7x5uz2vp7uqv3u60wahe23gcpsl3r6x7n4nq7
  Hub                            |
  Relayer, froopyland_100-1 Hub  | dym19ss04xrnyhypjlspnz2l4s4f0mu8v8c69yxzhz
  DA, arabica Network            | celestia14tcwhqsm84vlhhvert2lufrjjt006hyxa9k4qr
```

discord で faucet をもらうこと！！

[https://explorer.silknodes.io/testnet-dymension/tx/BC0AF7E89B978459FE84010E4B8EAA828E4D2C95722446441C85D539A562042C](https://explorer.silknodes.io/testnet-dymension/tx/BC0AF7E89B978459FE84010E4B8EAA828E4D2C95722446441C85D539A562042C)

register を行う

```bash
roller tx register
```

```bash
💈 Rollapp 'test_2457805-1' has been successfully registered on the hub.
```

roller を起動する。

```bash
roller run
```

### 参考文献

1. [モジュラーブロックチェーンで RollApp を作ってみよう](https://lu.ma/1y3srpal)
2. [2024/03/30 モジュラーブロックチェーンで RollApp を作ってみよう](https://docs.google.com/presentation/d/1k86CK8zfo2FrMZs2hBEp2yLy35fJOCgzVtuDi-Hjj88/edit#slide=id.g1780d6762b8_0_189)
3. [# **モジュラーブロックチェーンで RollApp を作ってみよう**　勉強会資料](https://cosmosjapan.notion.site/RollApp-075288811557466cba49e0e300b23c9c)
4. [dymension 公式 HP](https://docs.dymension.xyz/)
5. [dymension RollApps overview](https://docs.dymension.xyz/learn/rollapps/overview/)
