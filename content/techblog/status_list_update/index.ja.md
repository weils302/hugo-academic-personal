---
title: 電子在室表更新ログ
subtitle: 

# Summary for listings and search engines
summary: バージョン更新記録

# Link this post with a project
projects: [digital_office_door_sign]

# Date published
date: '2023-04-20T00:00:00Z'

# Date updated
lastmod: '2023-05-10T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ''
  placement: 2
  preview_only: true

authors:
  - WEILISI

tags:
  - 電子在室表
  - AI

categories:
  - Tech Blog
---

### V2.0.0: サービス停止ボタンを追加し、自動画像切替機能を実装（2023.5.10）
---
<div style="text-align: justify;">
以前、ステータスを変更するには、VNC Viewerにアクセスし、ESCを押して画像表示を終了し、新しいステータスを選択する必要がありました。
このプロセスはやや煩雑であったため、このバージョンでは「Set Status」ボタンをクリックすると画像が自動的に切り替わるように変更されました。
この機能はESCキーを無効にし、VNC Viewerを介してRaspberry Piを制御することを防ぎます。これを解決するために、一部のコードロジックが改訂され、
サービス停止ボタンが追加されました。サービス停止ボタンの機能は、以前のバージョンのESCキーに相当します。
</div>

![V2.0.0](V2.0.0.png)
<p style="font-size: 16px; line-height: 1.6; text-align: center;">V2.0.0クライアントウィンドウ、「サーバーを停止する」ボタンを追加。</p>


### V1.1.0: 「講義」ステータスを追加し、表示問題を修正（2023.4.25）
---
<div style="text-align: justify;">
「講義」はよく使用されるステータスであるため、対応するオプションが追加されました。さらに、前のバージョンでは、画像が自動的に拡大され、
画像の端が表示されないという問題がありました。この更新でこの問題が解決されました。
</div>

![lecture](lecture.jpg)
<p style="font-size: 16px; line-height: 1.6; text-align: center;">「講義」ステータスの画像の一つ</p>

![V1.1.0](V1.1.0.png)
<p style="font-size: 16px; line-height: 1.6; text-align: center;">V1.1.0クライアントウィンドウ、「講義」オプションを追加。</p>

![margin](margin.jpg)
<p style="font-size: 16px; line-height: 1.6; text-align: center;">画像の端が切り取られる問題を修正しました。</p>


### V1.0.0: 製品の正式稼働開始（2023.4.20）
---
<div style="text-align: justify;">
最初のバージョンが稼働開始しました。異なる天候状況に応じて室内状態を選択し設定できます（現在は春なので、雪の天候機能は現在使用できません）。
状態は「選択 → 設定ボタンをクリック」の手順で設定します。次の状態を設定する際には、VNC ViewerでESCを押して画像表示を終了した後、状態の設定を行う必要があります。
</div>

![V1.0.0](V1.0.0.png)
<p style="font-size: 16px; line-height: 1.6; text-align: center;">V1.0.0クライアントウィンドウ。</p>
