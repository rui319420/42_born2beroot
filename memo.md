パッケージ管理とは
DebianやUbuntuでは、ソフトウェアのインストール、更新、削除は「パッケージ管理システム」で行う。最標的なツールがaptやaptitudeである。いずれもAPTをベースにしているが、設計の思想や使用感が大きく異なる。

APT: Advanced Package Toolの略

### Debian

Linuxディストリビューションの1つ。
安定性とパッケージ管理の豊富さが特徴。初心者にも扱いやすい。
パッケージ管理はdeb形式、パッケージマネージャはAPTが採用されている。
Deabianは汎用性が高く、Ubuntuは

#### Linuxディストリビューション

「Linuxカーネル」をもとにして作られたOS全体のこと。パッケージ管理の方式や設計思想の違いなどから、主に Debian系、Red Hat系、Arch系に分かれている。

### apt

Debianが推奨しており、積極的にアップデートされている
apt-getの設計上のミスを修正したもの
CLI
動作は速くて軽い
コマンドの例

```
sudo apt update #パッケージ情報の更新
sudo apt upgrade #インストール済みパッケージを更新
```

### aptitude

apt-markやapt-cacheなどのパッケージの機能を含む
GUIを持つ
依存関係の衝突を自動で検知し、複数の解決策を提示
操作はやや遅く、それなりにメモリを消費する
コマンドの例

```
sudo aptitude safe-upgrade #安全な範囲での更新のみを実施する
```

### aptとaptitudeの違い

aptは軽量、aptitudeは多機能
VScodeとVisual Stadioみたいなもの

### SELinux

Linuxカーネルに矯正アクセス制御（MAC）機能を追加し、不正アクセスや侵害後の被害拡大を防ぐセキュリティ対策のひとつ。

### AppArmer

DAC(Linuxで一般的に使われているuser/groupを使ったセキュリティ機能)に加え、ファイルのパスに直接アクセス制限を付与する仕組みのこと
