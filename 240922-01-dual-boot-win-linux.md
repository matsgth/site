# Linux（Proxmox VE）、Windows11 の dual boot ？
2024/09/22

これまで、VMware 製品には大変お世話になってきたが、ライセンス関連の話を聞き、今後、どうするか？考えてみた。
ひとまず、以前、操作したことのある KVM がよいか、と考え、調べてみたところ、Proxmox VE は、KVM でもあることがわかった。

SFP+ ポートを持ち、InfiniBand接続する人もいる？製品も出しているMinisforum の Minisforum UM790 Pro を導入することに。
折角、WIndows11 も入っているので、Proxmox と dual boot にしようと考えたが、「Secure Boot」も残せるなら残したいし、ブートマネージャはどうなるのか？調べてみたが、よくわからない。grub2 などをいじる？、Windows のブートマネージャをいじる？

最近、Proxmox 8.1 から「Secure Boot」対応した、ということで、以下の手順で試したところ、dual boot できたのだろうか？こう言った記事は見かけていないが、このまま使ってみる。こんなことでよいのだろうか？

```
■「デュアルブート」の確認〜「BIOS（UEFI）」の「Boot Menu」（起動時、f7）を利用。
（１）Windows11 入りの SSD をはずし、空の SSD に proxmox ve 8.2 をインストール
（２）Windows11 入りの SSD を取り付け。
（３）普通に起動し、f7 連打し、起動ディスクを選択。
```
