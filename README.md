# GitWithSourcetree
Practice for using Git with Sourcetree.  

<!-- TOC -->

- [GitWithSourcetree](#gitwithsourcetree)
- [はじめに](#はじめに)
- [前提条件](#前提条件)
- [作業対象とするGitHubリポジトリ](#作業対象とするgithubリポジトリ)
- [SourceTreeについて](#sourcetreeについて)
- [今回のシナリオ](#今回のシナリオ)
- [参考資料](#参考資料)

<!-- /TOC -->

# はじめに
今の職場におけるバージョン管理システムをSVNからGitに変更することを提案したいと考えており、それの参考にと思い下記の書籍を読みました。  

[いちばんやさしいGit&GitHubの教本](https://www.amazon.co.jp/%E3%81%84%E3%81%A1%E3%81%B0%E3%82%93%E3%82%84%E3%81%95%E3%81%97%E3%81%84Git-GitHub%E3%81%AE%E6%95%99%E6%9C%AC-%E4%BA%BA%E6%B0%97%E8%AC%9B%E5%B8%AB%E3%81%8C%E6%95%99%E3%81%88%E3%82%8B%E3%83%90%E3%83%BC%E3%82%B8%E3%83%A7%E3%83%B3%E7%AE%A1%E7%90%86-%E5%85%B1%E6%9C%89%E5%85%A5%E9%96%80-%E3%80%8C%E3%81%84%E3%81%A1%E3%81%B0%E3%82%93%E3%82%84%E3%81%95%E3%81%97%E3%81%84%E6%95%99%E6%9C%AC%E3%80%8D%E3%82%B7%E3%83%AA%E3%83%BC%E3%82%BA/dp/429500524X/ref=sr_1_3?ie=UTF8&qid=1546691781&sr=8-3&keywords=Git)

インストールや初期設定の手順から、実際にブランチを切りながらバージョン管理していく流れまで述べられていて大変参考になりました。ただし、これらは全てGit bashからのコマンド操作によるものがメインであり、今後職場で導入提案をするならGUIツールを使った場合の操作手順を把握しておきたいと考えました。  
今回の記事では、GitのGUIツールとして人気の高いSourceTreeを使いながら、Gitでの複数人バージョン管理を一人で自作自演しながら体験してみた流れを紹介していきます。  

# 前提条件
- Gitのインストール及び初期設定が既に完了している
- OS: Windows 10 Home 64bit
- リモートリポジトリはGitHub上に作成

# 作業対象とするGitHubリポジトリ
今回は下記のリモートリポジトリをクローンして作業します。  
[リモートリポジトリのURL](https://github.com/ShisatoYano/GitWithSourcetree)

# SourceTreeについて
SourceTreeのインストール手順や基本的な使い方については、下記の記事に分かりやすく書かれているので参照ください。  
[Gitなんて怖くない！超初心者向け、SourceTreeの使い方はじめの一歩](https://prog-8.com/blogs/how_to_use_sourcetree)

# 今回のシナリオ
- 作業者: Shisato(自分)、作業者A、作業者Bの３名
- 全体の作業内容: 上記リポジトリのREADME.mdのファイルに、本記事と同じ内容の文章を書く。
- Shisatoの作業ブランチ: タイトルから導入部分まで
- Aの作業ブランチ: メイン内容の部分
- Bの作業ブランチ: 参考資料の部分
- Step1: リモートリポジトリをローカルにクローンする
- Step2: ３人それぞれのブランチをmasterから作成して作業開始
- Step3: Bの作業が先に完了→プルリクを作成してマージ
- Step4: Shisatoの作業ブランチにBの完了分をマージして作業継続→完了したらプルリクを作成してマージ
- Step5: Aの作業ブランチにShisatoとBの完了分をマージして作業継続→完了したらプルリクを作成してマージ
- Step6: 追加作業でブランチ作成してマージしようとしたらコンフリクト→コンフリクトを解消してマージ

# 参考資料
- [まずはGitの仕組みを理解することから](https://qiita.com/kyoyyy/items/161b6905f45bee2efe21)
- [ブランチ操作 - SourceTree](https://qiita.com/inabe49/items/be38f569040aed7d85b0)
- [Git概念の整理を試みる](https://open-groove.net/git/git-summary/)
- [たまご工房ブログ](http://tamagokobo.blogspot.com/2015/07/blog-post_21.html)
