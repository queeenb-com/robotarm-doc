# ロボットアーム ユーザーマニュアル

このマニュアルでは、ロボットアームの基本的な使用方法について説明します。
初めてご利用の方も、安心してお使いいただけるよう詳細な手順を記載しています。

## はじめに
このマニュアルは以下の順序で読み進めていただくことをお勧めします：

1. [ハードウェア](./hardware.md)  
      まずは機器の基本的な取り扱い方法を確認してください。
   - [電源の入れ方](hardware.md#電源の入れ方)
   - [土台と周辺部品・機器について](hardware.md#土台と周辺部品機器の説明と配置について)
   - [緊急停止ボタンの使い方](hardware.md#土台と周辺部品機器の説明と配置について)

2. [ソフトウェア](./software.md)  
   次に、操作アプリケーションの使い方を学びます。
   - [アプリケーションの起動方法](software.md#アプリケーションとロボットを立ち上げて両者を接続する)
   - [リモートアクセス方法](software.md#リモートアクセス)
   - [自動化の実行方法](software.md#自動化を行う)
   - [アップデート方法](software.md#アップデート方法)
   - [トラブルシューティング](software.md#トラブルシューティング)

3. [ノード詳細](./nodesdetails.md)  
   最後に、より高度な自動化のための各種ノードについて学習します。
   - [ノードの基本概念](nodesdetails.md#2-ノードの概要)
   - [移動系ノードの使い方](nodesdetails.md#31-移動系)
   - [データ処理ノードの使い方](nodesdetails.md#32-データ処理)
   - [ループなどその他のノード](nodesdetails.md#33-その他)
   - [実践的な活用例](nodesdetails.md#4-自分だけのプロトコルをつくる)

<div style="border-left: 4px solid #ffd700; background:rgb(230, 210, 172); padding: 15px; margin: 20px 0; border-radius: 5px;">
  <p style="margin: 0; font-size: 1.1em;">
    💡 <strong>Tips:</strong> 初めてお使いの方は、必ずハードウェアの章から順番に読み進めてください。<br>
    各章は前の章の内容を理解していることを前提に解説しています。
  </p>
</div>

## サポート情報
製品のご意見やフィードバックは[こちら](https://forms.gle/KhQCS1gYCF6BUkbf7)にご投稿ください。<br>
問題が発生した場合は、info( at mark) queeen-b.com までご連絡ください。

## クイックナビゲーション

<div style="display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 20px;">
  <a href="" style="display: block; padding: 10px 15px; background: #3498db; color: white; text-decoration: none; border-radius: 5px; min-width: 150px; text-align: center;">
    📖 メインガイド
  </a>
  <a href="hardware.html" style="display: block; padding: 10px 15px; background: #e74c3c; color: white; text-decoration: none; border-radius: 5px; min-width: 150px; text-align: center;">
    🔧 ハードウェアマニュアル
  </a>
  <a href="software.html" style="display: block; padding: 10px 15px; background: #f39c12; color: white; text-decoration: none; border-radius: 5px; min-width: 150px; text-align: center;">
    💻 ソフトウェアマニュアル
  </a>
  <a href="nodesdetails.html" style="display: block; padding: 10px 15px; background: #2ecc71; color: white; text-decoration: none; border-radius: 5px; min-width: 150px; text-align: center;">
    🧩 ノード詳細ガイド
  </a>
  <a href="protocol/colonypicking.html" style="display: block; padding: 10px 15px; background: #9b59b6; color: white; text-decoration: none; border-radius: 5px; min-width: 150px; text-align: center;">
    🧪 コロニーピッキング
  </a>
</div>
