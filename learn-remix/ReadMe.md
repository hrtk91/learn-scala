# Remix Web アプリケーション

このプロジェクトは、Remix を使用して 構築された Web アプリケーション です。生徒一覧の閲覧ができます。

## ホスティング

以下の指示に従えばローカルマシン上にプロジェクトのコピーを立ち上げて動かすことができます。

### 前提条件

- [Git](https://git-scm.com/downloads)がインストールされている。
- [Docker](https://www.docker.com/products/docker-desktop)および[Docker Compose](https://docs.docker.com/compose/install/)がインストールされている。

### リポジトリのクローン

以下のコマンドでリポジトリをクローンしてください：

```bash
git clone https://github.com/hrtk91/learn-remix-and-scala.git
```

### アプリケーションの実行

アプリケーションを起動するには、本 ReadMe と同じディレクトリ(learn-remix)から以下のコマンドを実行します：

```bash
docker-compose up --build
```

アプリケーションが起動したら、以下の URL に ブラウザでアクセスしてください：

```
http://localhost:3000/
```

## アーキテクチャ

### 採用技術

| 項目                                          | バージョン | 説明                                                     |
| --------------------------------------------- | ---------- | -------------------------------------------------------- |
| [TypeScript](https://www.typescriptlang.org/) | 5.1.6      | プログラミング言語                                       |
| [React](https://ja.react.dev/)                | 18.2.0     | Web とネイティブユーザインターフェースのためのライブラリ |
| [Remix](https://remix.run/)                   | 2.8.0      | Web フレームワーク                                       |
| [tailwindcss](https://tailwindcss.com/)       | 3.4.1      | CSS スタイリング                                         |

#### Remix 採用理由

1. 環境変数を使いたい
2. Web 標準を学びたい

##### 1. 環境変数を使いたい

仕事では基本的に Vite+React の構成で開発を行っているが、Vite はビルド時にしか環境変数の切り替えができません。  
そのため、ある時期が過ぎたらこのページは無効にしたい、という要件があると再ビルドする手間が発生するなど、
環境変数の切り替えができないことが不便だと感じることが多かったです。

Remix は SSR のフレームワークであり、プログラムの再起動時に環境変数が切り替えられるため採用したいと考えました。

##### 2. Web 標準を学びたい

Remix は公式に Web 標準を学べるフレームワークとして位置づけられているため、
基礎となる技術を学ぶために採用したいと考えました。  
基本的な技術を学ぶことで今後の web 開発においても長く使える知識を得ることは重要な点だと思います。

#### tailwindcss 採用理由

これは Remix が公式に CSSinJS が非推奨なため、それに合わせての採用です。  
基本的に MUI を使うことが多いのですが、時代の流れ的にもゼロコストランタイムが流行りそうな気もするので別の選択肢を抑えておきたいと考えました。