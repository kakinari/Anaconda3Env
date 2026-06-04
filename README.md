# Anaconda3Env

このリポジトリはAnaconda 3を使用したPython開発を行えるように作成したCodeSpaceのイメージを動作させるためのテスト用リポジトリです。

デフォルトのインストールとして以下のパッケージがインストールされています。

- Anaconda3 (Python 3.13.9)
- opencv_python
- PyToach

詳細は
`conda list`
で確認ください。

## Codespaces 設定

このリポジトリは [.devcontainer/devcontainer.json](.devcontainer/devcontainer.json) で
`kakinari/ubi-micro-ja:10-cs-anaconda-3` を使うように設定しています。

既存の Codespace に反映する場合:

1. コマンドパレットで `Codespaces: Rebuild Container` を実行
2. 再起動後、`python --version` と `conda --version` を確認

## 実行手順

1. Codespace を開く
2. 必要ならコマンドパレットで `Codespaces: Rebuild Container` を実行
3. ターミナルで次を確認

	```bash
	python --version
	conda --version
	```

4. Notebook を使う場合は、`.devcontainer` 配下または任意の場所で `.ipynb` を開いて実行

## トラブル時の再ビルド手順

症状例:

- `python` や `conda` が見つからない
- 拡張機能が入らない
- コンテナ更新後に設定が反映されない

対処:

1. コマンドパレットで `Codespaces: Rebuild Container` を再実行
2. 改善しない場合は `Codespaces: Rebuild Without Cache` を実行
3. それでも改善しない場合は Codespace を停止して再作成

再確認コマンド:

```bash
python --version
conda --version
echo "$PATH"
```