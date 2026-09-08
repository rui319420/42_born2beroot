パッケージ管理とは
DebianやUbuntuでは、ソフトウェアのインストール、更新、削除は「パッケージ管理システム」で行う。最標的なツールがaptやaptitudeである。いずれもAPTをベースにしているが、設計の思想や使用感が大きく異なる。

APT: Advanced Package Toolの略

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
