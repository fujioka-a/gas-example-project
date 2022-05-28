# Google Apps Script サンプルプロジェクト
## 概要  
- 要件が決まりきっていない段階で「ひとまず動くものを作ろう」という要望は多々ある。  
簡易的かつスピーディーに、画面インターフェース構築やデータ管理などを実現するために、**GoogleAppsScript**（以下、GASとする）が有効な手段の１つとなる。  
  
- GASでは、各種Googleサービスと連携することで効率的に機能開発ができる。  
例としては、SpreadSheetを利用することで、入力画面や、データ表示画面を実現することができる。

## 前提
1) TypeScript構成  
GASコンソールから直接スクリプトを作成せずに、ローカルからTypeScript構成でプロジェクト作成する。

2) claspデプロイ  
GASプロジェクトへのデプロイは、**clasp**を利用する。  
⇒claspの現状のデメリットは、Googleの認証ファイルの利用が必要であることだ。これにより、CDツールなどを実現するためには、認証ファイル（.clasprc.json）をセキュアに保存してデプロイ構築の必要がある。  
⇒★SecretManagerに保存して、AWS Code Deployから利用できるかは、将来的な調査項目。  
参考リンク：https://qiita.com/HeRo/items/4e65dcc82783b2766c03  
  
## 環境構築  
###  必要モジュール
- node >= 16.4.0
  - `> node --version`
- python >= 3.8.0
  - `> python --version`

###  パッケージのインストール(npm)
- `> npm init`  
- `> npm insatall --save package@x.y.z`  
- `> npm insatall --save-dev package(dev)@x.y.z`  

- 参考：https://qiita.com/Sekky0905/items/452619651cdd950c2271  

###  Lint　 
- 2019年以降くらいから、JSでもTSでもESLintの推奨がされている。  
https://iwb.jp/use-eslint-instead-of-tslint-for-typescript/  

##  テスト実行
VS Codeでの開発を前提として、Test Explore＋Jestによりテストケースを実行する。  
- Extensionから、Test ExploreとJestをインストール    
- Exploreから、"Run tests"を選択して実行する  
