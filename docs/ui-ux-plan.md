---
layout: default
title: 'UI/UX相談'
permalink: /ui-ux-plan/
mermaid: true
---

# このドキュメントの概要

デザイナーにUI/UXを相談する際にZEROの概要とUI/UX面での課題感を共有するためのドキュメント

# ZEROの概要

ELE社で現在提供中の動画コンテンツ作成AIツールです。
AI時代の動画コンテンツ作成を再定義するツールで、現時点では、ただ分かりやすいだけではなく、”売上に繋がる”YouTube台本を自動生成します。

顧客は「良いものを作っているのに売れない」という悩みを抱える事業者で、
弊社独自のノウハウで台本の書き方と、それを形にするツールをセットで提供することで彼らを支援しています。

**ツールURL:** [https://youtube-content-gen.vercel.app/](https://youtube-content-gen.vercel.app/)

※ URLを最初に開いた際にはベーシック認証が求められます。  
別途案内しているユーザー名とパスワードをご入力ください。

**マニュアルURL:** [https://ele-inc.github.io/zero_user_manual/](https://ele-inc.github.io/zero_user_manual/)

# ZEROの画面構成

## トップ画面

ZEROは現状で①企画案作成AI、②冒頭台本作成AI、③台本全文作成AI、④ショート台本作成AI の4つのモードがあり、トップ画面から各モードを選択して、それぞれのモードの必要情報入力画面に遷移します。
必要情報入力後は前モード共通のチャット画面にリダイレクトします。
チャット画面でAIと対話しながら台本を作成していきます。

<img width="1441" height="836" alt="image" src="https://github.com/user-attachments/assets/881c8b7f-52c7-4ca2-8f2f-da4f671e0771" />

## 企画案作成AIへのスタート画面

<img width="1441" height="817" alt="image" src="https://github.com/user-attachments/assets/ffb85a4b-f07e-4d5c-ad3d-267a5940f652" />


## 冒頭台本作成AIへのスタート画面

<img width="1416" height="802" alt="image" src="https://github.com/user-attachments/assets/4796fd01-a790-4a3f-9cee-944610a15245" />


## 台本全文作成AIのスタート画面

<img width="1425" height="830" alt="image" src="https://github.com/user-attachments/assets/d702e28d-bf73-445e-8146-189c77eb4493" />

## ショート台本作成AIへのスタート画面

<img width="1423" height="829" alt="image" src="https://github.com/user-attachments/assets/4ecb5785-6867-4151-842f-1bb15867e9fc" />

## 発信者情報の設定画面（マイページ）
※ メールアドレスの箇所から遷移できます
<img width="1406" height="805" alt="image" src="https://github.com/user-attachments/assets/02121dc4-6914-40c2-a646-7ebc113d5a2f" />

## チャット形式の画面（全モード共通）
※ 画像は企画案作成AIの必要情報入力後にリダイレクトした後の画面
<img width="1382" height="806" alt="image" src="https://github.com/user-attachments/assets/fddf0af3-1552-418f-965a-2287b0fe9d2b" />

## ドキュメント機能の画面

Claudeのアーティファクト機能やChatGPTのキャンバス機能に近い機能で、台本をマークダウン形式で出力させ、編集と簡単なバージョン管理ができます。

<img width="1419" height="821" alt="image" src="https://github.com/user-attachments/assets/18c583c9-06fa-4c2b-aa3c-718ed729f345" />

<img width="1422" height="815" alt="image" src="https://github.com/user-attachments/assets/d80bce08-8b1c-409b-91e5-33df6d816da2" />


# ZEROのUI/UX課題感

大きく二つの課題感があります。

## 機能間の連携がUI上で表現できていない

YouTube動画作成の一般的なフローは「企画→台本作成」ですが、ZEROでは各機能が独立しており、UI/UX面で以下の課題があります。

- **現状:**
  - 「企画作成AIで作成した企画を、台本作成AIに入力して利用できる」といった機能間の連携をテキストの説明によって補っている。
- **ユーザーからの要望:**
  - 説明によって機能は利用されているものの、「作成した企画からシームレスに（コピー＆ペーストなどを介さず）台本を作成したい」という声が寄せられている。
- **目指す方向性:**
  - より直感的なワークフローを実現するため、UI/UXをゼロベースで再考したい。

### 補足：現状のデザインに至った背景

各機能が単体で利用されるケースも想定しています。
例えば「冒頭台本作成AI」は、企画から内容を膨らませるだけでなく、既存の台本の冒頭部分を改善するためにも利用できます。
このような背景から、初期リリースでは各機能間の連携をあえて強く定義せず、トップ画面に各モードを並列に配置する構成としました。

## チャットベースUIの最適性

全てのモードで、AIとの対話を通じて成果物を作成するフローを採用していますが、以下の課題があります。

- **現状:**
  - 「台本作成AI」のように、ある程度の対話を経てドキュメント形式で成果物が出力された後は、ユーザーによる編集作業が主となる。
- **課題:**
  - 編集段階ではツールが実質的にエディタとして機能するため、プロセス全体を通して対話形式のUIが最適であるかについては、十分に検討できていない。
