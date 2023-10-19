---
title: AIアプリケーションに基づいた電子在室表の作成 (3)
subtitle: 

# Summary for listings and search engines
summary: 電子在室表のブラケット製作およびコードの最終デプロイ

# Link this post with a project
projects: [電子在室表制作]

# Date published
date: '2023-04-18T00:00:00Z'

# Date updated
lastmod: '2023-04-25T00:00:00Z'

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

categories:
  - Tech Blog
---
*過去の記事：*  
*[AIアプリケーションに基づいた電子在室表の作成 (1)](https://weils302.com/techblog/status_list_1_20230407/)*  
*[AIアプリケーションに基づいた電子在室表の作成 (2)](https://weils302.com/techblog/status_list_2_20230415/)*

---

<div style="text-align: justify;">
画像リソースが手に入った後、次にブラケットを作成し、コードを実際に動かすことです。
</div>

## ラズベリーパイとディスプレイ用ブラケットの製作
--------------------
<div style="text-align: justify;">
画像を作成する過程で、近くのホームセンターでブラケットを作るための材料を探していました。いくつかの鉄片とネジを使って、ディスプレイを固定するブラケットを簡単に作成しました。
</div>

![組み立てられたブラケット](IMG_8799.jpg "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 0.6;"><i>(このようなブラケットを組み立てました)</i></p>

<div style="text-align: justify;">
次に、ブラケットをドアにどのように固定することです。最初の記事で、鉄製のドアに穴を開けることができないため、磁石を使用することを考えていると言及しました。
この時、磁石の吸引力がどれほど強いかが非常に重要です。さらに、磁石には穴が開いている必要があり、それによって磁石をブラケットに固定するためのネジを使用します
（ブラケットには多くのネジ穴があります）。ホームセンターを見て回ったところ、穴が開いている磁石の吸引力はそれほど強くなく、
小さなメモを貼るのに適しているだけでした。私のオフィス部屋には強力な磁石のフックがありますが、これらのフックは前後に動くので、
ドアを開け閉めするときにブラケットが前後に揺れて、ディスプレイに当たる可能性があるため使用できません。最終的に、インターネットで探し、
Amazonで適切な強力な磁石を見つけました。
</div>

![回転可能な磁石](IMG_8949.jpg "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 0.6;"><i>(一方はネジを1つだけ締めて、自由に回転できます)</i></p>

![もう一方の磁石はしっかり固定](IMG_8950.jpg "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 0.6;"><i>(もう一方はしっかり固定)</i></p>

![固定後の様子](IMG_5608.jpg "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 0.6;"><i>(このようにしてドアに固定しました)</i></p>  


## ラズベリーパイの取り付けと設定
--------------------
<div style="text-align: justify;">
このディスプレイの背面にはラズベリーパイのサイズに合ったネジ穴があるので、ラズベリーパイをディスプレイに簡単に固定することができます。
初回起動時にはシステムの設定が必要で、リモートコントロールのためのプラグインなどをインストールする必要があるため、通常のマウスとキーボードを接続しました。
</div>

![背面にラズベリーパイを固定](IMG_8952.jpg "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 0.6;"><i>(ラズベリーパイはディスプレイの背面に固定できます)</i></p>

![各種外部デバイスを接続](IMG_8953.jpg "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 1.5;"><i>(電源、キーボード、マウス、ディスプレイを接続すると、背面にはたくさんのケーブルがあります。)</i></p>

![起動画面](IMG_8954.jpg "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 0.6;"><i>(無事に起動して、システムにアクセスし、部屋のWiFiに接続しました。)</i></p>

<div style="text-align: justify;">
ラズベリーパイにVNCを設定した後、仕事用のデスクトップから直接操作やファイル転送が可能になりました。デスクトップのVNC Viewerを使用して、
準備したサーバーコードファイルをラズベリーパイに転送し、システムの組み込みターミナルでそのコードを実行すると、ラズベリーパイはリスニングを開始します。
その後、デスクトップでクライアントコードを実行すると、GUIウィンドウが表示され、そのウィンドウで状態を設定すると、
画像がラズベリーパイのディスプレイに表示されます。現在の画像表示状態を確認するには、VNC Viewerで確認できます。現在のバージョンでは、状態を変更する際に、
VNC ViewerでESCキーを押して画像表示を終了し、次の状態を選択して表示する必要があります。このプロセスは少し煩雑で、
次のバージョンアップデートで改善することを考えています。
</div>

![クライアントインターフェース](client_window.png "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 1.5;"><i>(クライアントウィンドウ、左側で現在の天気を選択し、右側で状態を選択。選択後、ボタンをクリックすると画像が表示されます。)</i></p>

![VNC Viewerでの状態確認](IMG_5778.JPG "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 0.6;"><i>(VNC Viewerで画像表示状態を確認)</i></p>

![実際の効果1](IMG_5779.JPG "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 0.6;"><i>(ドア上の表示)</i></p>

![実際の効果2](featured.JPG "画像クレジット: Ⓒ WEILISI")
<p style="font-size: 16px; line-height: 0.6;"><i>(全体的にディスプレイの表示も良好で、非常にクリアに見えます)</i></p>

<div style="text-align: justify;">
今後のバージョン管理のために、関連コードをGitHubリポジトリにアップロードしました（現在はプライベートリポジトリ）。後で状況に応じて公開するかどうかを決定する予定です。
</div>
