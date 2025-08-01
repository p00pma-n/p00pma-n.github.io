---
layout: page
title: "software Eng. lecture note"
permalink: /docs/softwareEng2025
---

# ソフトウェア工学のまとめ
## 20TI008 伊藤一馬 
### ソフトウェアの定義
1.実行されることによって必要な特性、機能、性能を提供する命令語群（コンピュータプログラム） <br>
2.プログラムが適切に情報を扱うことを可能とするデータ構造                                <br>
3.プログラムの操作や使用法を記述した情報 <br><br>
ハードウェアと異なり劣化しないが、悪化はする<br>
↑どういうことか？・・・部品の酸化などによる劣化は起きないが、環境や技術が日々更新されているため、仕様を強化していかなければ他のシステムと相互運用ができず、役に立たなくなってしまうということ<br>
### ソフトウェア工学とは
「品質」、「コスト」、「納期」の最適なバランスを実現するための手法・方法論<br>
### ソフトウェアエンジニアリングツールとは
ソフトウェアの開発・設計・保守・運用・テストなどを効率よく行うために使われる支援ツールのこと。<br>
目的：ソフトウェア開発の生産性と品質の向上、作業の自動化など<br>
**なぜ生産性の向上、作業の自動化が必要なのか？**<br>
1. 正確性と速度が求められているから<br>
    ソフトウェアはプログラミングと違いサービスとして顧客に提供するものであるため、サービス開始に合わせた納期がある。決められた予算・時間でサービスを完成させるためには自動化を活用して時間を短縮したりなるべく人手を使わずに手入力によるミスを減らしたほうが良いため。
2. 市場変化に対応するため<br>
    市場の変化が速く、それに合わせた対応が求められる。手作業ではスピードが遅いため自動化が必要となる。<br>
### ソフトウェアライフライクル
ニーズの誕生→企画→開発→運用→保守→サービス終了のサイクル<br>
### プロジェクトについて
* 有期性
    * 必ず終わりがある
* 独自性
    * 独自の目的を達成する<br><br>
* フォアキャスティング
    * 現在位置から目標に向かって進んでいく
    * 目標に正しく向かうことができない可能性がある
* バックキャスティング
    * 目標から必要な手順を逆算・計画し達成に向かう
    * 目標をはっきりと定める必要がある
    * 手順が目標達成に沿っているか検討する必要がある<br>
### 開発プロセス
* ウォーターフォール型開発プロセス
    * 手順通りに進めていく方式
    * 前の手順が詰まると後の手順にしわ寄せがいってしまう可能性がある
* 反復型開発プロセス
    * ソフトウェアの機能ごとに分割し、管理する方式
    * 部分的に完成させるため、ユーザーの要望を反映させやすい
    * 一括で稼働するシステムには不向き
* アジャイル開発
    * PDCAサイクルを週単位で素早く回し、何回も納品を繰り返して評価をもらい、それを基にまた開発を行う方式
    * 早期かつ継続的な納品によって顧客の満足度を達する
    * **スクラム**と呼ばれる10人前後のチームを組み、メンバーで協力し合うことが前提となる<br>
これらの方式は一長一短であり、顧客が望むサービスの形態によって得意とする方式が決まる他、複数の方式を組み合わせたハイブリッド型なども存在する<br>
### WBS (Work Breakdown Structure)
プロジェクト目標を達成し、必要な要素成果物を生成するために、プロジェクトチームが実行する作業を、要素成果物を主体に階層的に要素分解したもの
* プロジェクトを細かい作業に分解した構成図
* 作業をさらに細かく分解し、順に並べる
メリット
* やるべきこと・やらないことが明確になる
* 全体管理と作業計画が見えるようになる
演習では、ゲーム大会の主催者となって、協力者2人とともに大会の準備・当日の運営をするにあ立って必要となるWBSを作成した（[作成したWBS](https://docs.google.com/spreadsheets/d/1CxA3SS6YRpk3jSHurMJrWj4SLLayf37pOnBwMImtcbY/edit?gid=1437396437#gid=1437396437)）

### コーディング
コードを書くときは読む人に向けてスタイルを統一をさせることが望ましい
* **flake8**
    * Pythonの代表的なスタイルである***PEP8***に基づくコードチェックツール
    演習では、flake8を用いてサンプルコードをPEP8に合わせたコーディングチェックを行った

### 特別講義
特別講義ではスタートアップ企業の概要について学んだ。国の成長にはスタートアップ企業が欠かせないこと、日本のスタートアップ企業が中国やアメリカに比べ少ないこと、スタートアップ企業を作るための考え方や支援などを講演を通じて学ぶことができた。

### バージョン管理
バージョン管理には2つの型が存在する
1. 集中管理型
    * バージョン管理をリモートのみで行う
    * 複数のローカルでの変更があった場合変更の競合が起こりやすく同期に時間がかかる
2. **分散管理型**
    * ローカルでもバージョン管理を行う
    * リモートレポジトリへのアクセスが少ないため同期しやすく、障害にも強い
* **git**
    * 分散管理型のバージョン管理システム
    * **ブランチ**・・・作業を枝分かれさせ並行作業を可能にする
* **gitフロー**
    * mainブランチ・・・完成した作業のみが存在するブランチ．最終的な作品のみ置いておくイメージ
    * devブランチ・・・バージョンを変更する際に修正作業を行うためのブランチ．変更作業やバグのチェックを行った後mainブランチと同期を行う（プル＆マージ）
    演習ではgitコマンドとブランチの仕組みを活用しgithubで制作物の作成・バージョン管理を行った