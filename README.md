# YMM4 プラグイン配布リポジトリ（.ymme）

ゆっくりMovieMaker4（YMM4）向けの自作拡張プラグイン（`.ymme`）を配布しているリポジトリです。  
動画編集の効率化ツールから、立ち絵の生命感を高めるモーション拡張、Web技術を取り入れたリッチな背景プラグインまで、動画制作を快適・高品質にするプラグインを収録しています。

すべてのプラグインに**自動アップデート機能**が内蔵されており、YMM4起動時に新しいバージョンが公開されている場合は自動で通知・更新が行われます。

---

## 収録プラグイン一覧 & ダウンロード

| プラグイン名 | 最新リリース / ダウンロード | 詳細解説 | 種別 | 概要 |
| :--- | :--- | :---: | :--- | :--- |
| **立ち絵モーション拡張** | [v1.0.2 ダウンロード](https://github.com/KisaragiIchigo/ymme/releases/download/BlinkExtension-v1.0.2/BlinkExtension.ymme) ([Release](https://github.com/KisaragiIchigo/ymme/releases/tag/BlinkExtension-v1.0.2)) | [詳細](BlinkExtension.txt) | 立ち絵モーション | PSD立ち絵に自然なランダムまばたき・目そらし・リアルな呼吸を追加 |
| **ぽちぽちボード** | [v1.1.1 ダウンロード](https://github.com/KisaragiIchigo/ymme/releases/download/PochiPochiBoard-v1.1.1/PochiPochiBoard.ymme) ([Release](https://github.com/KisaragiIchigo/ymme/releases/tag/PochiPochiBoard-v1.1.1)) | [詳細](PochiPochiBoard.txt) | 編集支援ツール | よく使うSE・画像・動画を30マスに登録し、1クリックやキー操作でタイムラインへ即ポン出し |
| **セリフ追従** | [v1.0.1 ダウンロード](https://github.com/KisaragiIchigo/ymme/releases/download/SerifRipple-v1.0.1/SerifRipple.ymme) ([Release](https://github.com/KisaragiIchigo/ymme/releases/tag/SerifRipple-v1.0.1)) | [詳細](SerifRipple.txt) | 編集支援ツール | セリフ修正で尺が変わった際、後ろの全レイヤーアイテムを自動で前後にずらすリップル編集 |
| **セリフのタイムスタンプ保存** | [v1.0.1 ダウンロード](https://github.com/KisaragiIchigo/ymme/releases/download/SerifTimestamp-v1.0.1/SerifTimestamp.ymme) ([Release](https://github.com/KisaragiIchigo/ymme/releases/tag/SerifTimestamp-v1.0.1)) | [詳細](SerifTimestamp.txt) | 出力・連携ツール | セリフを開始時刻順に整列し、YouTubeチャプター目次や台本、表計算TSVとして一発書き出し |
| **ショート切り抜き** | [v1.0.1 ダウンロード](https://github.com/KisaragiIchigo/ymme/releases/download/ShortClip-v1.0.1/ShortClip.ymme) ([Release](https://github.com/KisaragiIchigo/ymme/releases/tag/ShortClip-v1.0.1)) | [詳細](ShortClip.txt) | 編集支援ツール | 通常の横動画から縦型ショート（1080×1920）の別タブシーンをワンクリック自動生成 |
| **HTML背景プラグイン** | [v1.0.1 ダウンロード](https://github.com/KisaragiIchigo/ymme/releases/download/WeCasBackground-v1.0.1/WeCasBackground.ymme) ([Release](https://github.com/KisaragiIchigo/ymme/releases/tag/WeCasBackground-v1.0.1)) | [詳細](WeCasBackground.txt) | 図形・背景演出 | HTML/CSS/JS（GSAP、Tailwind CSS等）のWebアニメーションをYMM4上で直接レンダリング |
| **VRM立ち絵** | [v0.17.0 ダウンロード](https://github.com/KisaragiIchigo/ymme/releases/download/VrmTachie-v0.17.0/VrmTachie.ymme) ([Release](https://github.com/KisaragiIchigo/ymme/releases/tag/VrmTachie-v0.17.0)) | [詳細](VrmTachie.txt) | 3D立ち絵・演出 | VRM・PMX対応の3D立ち絵描画、母音口パク、VLOG自撮り・手ブレ・カメラワーク |

---

## 各プラグインの特徴と機能紹介

### 1. 立ち絵モーション拡張（BlinkExtension）
- **ダウンロード**：[BlinkExtension.ymme (v1.0.2)](https://github.com/KisaragiIchigo/ymme/releases/download/BlinkExtension-v1.0.2/BlinkExtension.ymme) ｜ [Releaseページ](https://github.com/KisaragiIchigo/ymme/releases/tag/BlinkExtension-v1.0.2) ｜ [詳細解説テキスト](BlinkExtension.txt)

PSD立ち絵に「自然なランダムまばたき」「目そらし」「リアルな呼吸」を自動で追加するプラグインです。

- **自然なゆらぎまばたき**：機械的な等間隔ではなく、人間味のあるランダム周期でまばたき（最短間隔ガード付き）。
- **ダブルまばたき**：たまに「パチパチ」と2回続けてまばたきする仕草を自動でミックス。
- **キャラ同士の重複防止**：画面内の複数キャラクターが示し合わせたように同時にまばたきする違和感を自動解消。
- **待機中の目そらし**：セリフを喋っていない合間に、ふと視線を外して戻す自然なしぐさを追加（レイヤー名自動判別＋手動調整対応）。
- **呼吸エフェクト**：首から上は形を保って上下し、首から下は足元基準でふわりと伸縮（Direct2Dカスタムシェーダーによる高品位変形）。
- **発話・感情連動**：喋っている最中は浅く速く、怒り・照れは深く速く、ジト目はゆっくり…とキャラクターの感情に合わせて呼吸テンポが変化。
- **完全再現性**：プレビュー時と動画出力時でまばたきのタイミングが一切ズレないシード値決定性。

---

### 2. ぽちぽちボード（PochiPochiBoard）
- **ダウンロード**：[PochiPochiBoard.ymme (v1.1.1)](https://github.com/KisaragiIchigo/ymme/releases/download/PochiPochiBoard-v1.1.1/PochiPochiBoard.ymme) ｜ [Releaseページ](https://github.com/KisaragiIchigo/ymme/releases/tag/PochiPochiBoard-v1.1.1) ｜ [詳細解説テキスト](PochiPochiBoard.txt)

よく使う効果音（SE）・画像・動画を登録し、1クリックやキーボード操作で再生ヘッド位置へ瞬時に配置できるサンプラーツールです。

- **30マスの直感サンプラー**：6×5マスに素材を登録し、押すだけでタイムラインに即座に配置。複数ページ対応で動画シリーズごとに素材を整理可能。
- **テンキーでキーポン出し**：「キー」をオンにすると、テンキー（1〜0 / Shift+1〜0）を押すだけでキーボードからダイレクトに素材をタイムラインへ連続投入。
- **D&Dで簡単登録**：エクスプローラーから空きマスへファイルをドロップするだけで即登録（複数ファイル一括登録対応）。
- **演出・アニメーションの記憶**：選択中アイテムから座標、拡大率、回転、エフェクト、キーフレーム情報を丸ごと取り込んで同じ演出状態で配置可能。
- **音量400%ブースト＆その場試聴**：小さい効果音もプラグイン上で事前に音量アップ可能。ボタンを押した瞬間にツール上で音が鳴るため手応え抜群。
- **カラー絵文字アイコン**：マスには視認性の高い鮮やかなカラー絵文字を設定可能。

---

### 3. セリフ追従（SerifRipple）
- **ダウンロード**：[SerifRipple.ymme (v1.0.1)](https://github.com/KisaragiIchigo/ymme/releases/download/SerifRipple-v1.0.1/SerifRipple.ymme) ｜ [Releaseページ](https://github.com/KisaragiIchigo/ymme/releases/tag/SerifRipple-v1.0.1) ｜ [詳細解説テキスト](SerifRipple.txt)

セリフの文字修正や音声再生成でボイスの長さが伸び縮みしたとき、後ろにある全レイヤーのアイテムを自動でまとめて前後にずらしてくれるリップル編集プラグインです。

- **全レイヤー一括追従**：セリフの尺が変わった瞬間、後続の立ち絵、表情、効果音、画像、テロップなどをまとめて同じフレーム数だけ自動シフト。
- **またぐアイテムの自動伸縮**：BGMや背景など、セリフの終わりをまたいで長く続いているアイテムは長さをぴったり自動追従。
- **他のセリフは長さをキープ**：他のボイスアイテムは音声の長さを保ったまま「位置だけ」を平行移動。
- **ロック保護＆衝突回避**：動かしたくないロック済みアイテムは完全保護。衝突の恐れがある場合は無理に動かさず安全に停止。
- **完全Undo（元に戻す）対応**：セリフの長さ変更と後ろのアイテムシフトが1回の操作として記録されるため、Ctrl+Z一発で元通り。
- **日常のあらゆる操作で発動**：セリフ編集、発音・話速変更、キャラ変更、「アイテムの長さをリセット」実行時などに自動で働きます。

---

### 4. セリフのタイムスタンプ保存（SerifTimestamp）
- **ダウンロード**：[SerifTimestamp.ymme (v1.0.1)](https://github.com/KisaragiIchigo/ymme/releases/download/SerifTimestamp-v1.0.1/SerifTimestamp.ymme) ｜ [Releaseページ](https://github.com/KisaragiIchigo/ymme/releases/tag/SerifTimestamp-v1.0.1) ｜ [詳細解説テキスト](SerifTimestamp.txt)

タイムライン上の全セリフを開始時刻順に並べ、YouTube概要欄のチャプター目次や台本、表計算用データとして一瞬で書き出し・コピーできるツールです。

- **フレーム精度の正確な時刻**：フレーム番号とfpsから時刻を整数計算するため、小数点の累積誤差ゼロ。
- **自由なテンプレート設計**：`{開始}` `{終了}` `{キャラ}` `{セリフ}` `{番号}` を組み合わせた自由なフォーマットを作成可能。
- **定番プリセット搭載**：
  - 「チャプター」：`{開始} {セリフ}`（YouTube概要欄にそのまま貼れる 0:05 / 1:02:03 形式）
  - 「台本」：`{開始} {キャラ}「{セリフ}」`（00:00:05 形式の読みやすい台本形式）
  - 「表計算」：ExcelやGoogleスプレッドシートに直接貼れるタブ区切り（TSV）形式
- **リアルタイムプレビュー**：タイムラインの編集・移動・追加・削除に自動追従してプレビューを更新。
- **柔軟な絞り込み**：非表示レイヤー・アイテムの除外、選択中セリフのみの書き出し、セリフ内改行の1行化に対応。

---

### 5. ショート切り抜き（ShortClip）
- **ダウンロード**：[ShortClip.ymme (v1.0.1)](https://github.com/KisaragiIchigo/ymme/releases/download/ShortClip-v1.0.1/ShortClip.ymme) ｜ [Releaseページ](https://github.com/KisaragiIchigo/ymme/releases/tag/ShortClip-v1.0.1) ｜ [詳細解説テキスト](ShortClip.txt)

通常の横動画（16:9）プロジェクトから、YouTubeショートやTikTok、Reels向けの縦型動画（1080×1920）の別シーン（タブ）をワンクリックで自動生成するプラグインです。

- **ワンクリックで別シーン生成**：元動画のタイムラインを一切壊さず、新しいタブとして「ショート」「ショート 2」を非破壊生成。
- **直感的な区間指定**：タイムラインの再生ヘッドを合わせて「この位置を開始」「この位置を終了」を押すだけで切り抜き区間を決定。
- **定番ショートレイアウトへ自動変換**：
  - 中央：元の動画やゲーム画面を美しい角丸フレーム内に配置
  - 上部：目を引く大きなタイトル枠（黄色太字＋赤縁取り）
  - 下部：左右の指定枠に立ち絵を最適配置（複数キャラ時の奥・手前ずらし対応）
- **ショート専用字幕スタイル**：スマホ画面で読みやすい位置・サイズ・縁取りへ自動変換（文字色はキャラ固有色を維持）。

---

### 6. HTML背景プラグイン（WeCasBackground）
- **ダウンロード**：[WeCasBackground.ymme (v1.0.1)](https://github.com/KisaragiIchigo/ymme/releases/download/WeCasBackground-v1.0.1/WeCasBackground.ymme) ｜ [Releaseページ](https://github.com/KisaragiIchigo/ymme/releases/tag/WeCasBackground-v1.0.1) ｜ [詳細解説テキスト](WeCasBackground.txt)

HTML/CSS/JavaScript（GSAP、Tailwind CSS、anime.js）で書かれたWebアニメーション演出を、動画に書き出すことなくYMM4タイムライン上で直接レンダリングする背景プラグインです。

- **1フレーム単位の完全同期描画**：WebView2と独自仮想時計フックにより、実時間の処理速度に依存せずYMM4のフレーム・タイムライン時刻と1フレーム単位で完全同期。プレビューも動画出力も同一結果を保証。
- **シーク・巻き戻しに完全追従**：タイムラインを巻き戻しても、仮想時計が正確にその時刻の状態を再現。
- **完全オフライン動作**：GSAP 3.15、anime.js 4.4、Tailwind CSS 3.4、図解アニメーション用ランタイムを内包。ネット接続不要。
- **背景透過対応**：Web背景のベースカラーを抜いて、他の映像素材の上に動くグラフィックスやテロップとして重ね合わせ可能。
- **制作支援ツール「Web演出ツール」同梱**：
  - タイムラインの解像度・fps・総秒数に合わせたAI向け最適化プロンプトをワンクリック生成
  - ChatGPTやClaudeなどのAIが返したコードを丸ごと貼り付けるだけでHTML/JSを自動切り分け
  - 尺の10%/50%/90%のサムネイルプレビューとエラー検出で動作確認
  - 空いている最奥の背景レイヤーへ即座にタイムライン配置

---

### 7. VRM立ち絵（VrmTachie）
- **ダウンロード**：[VrmTachie.ymme (v0.17.0)](https://github.com/KisaragiIchigo/ymme/releases/download/VrmTachie-v0.17.0/VrmTachie.ymme) ｜ [Releaseページ](https://github.com/KisaragiIchigo/ymme/releases/tag/VrmTachie-v0.17.0) ｜ [詳細解説テキスト](VrmTachie.txt)

3DのVRM・PMX（MMD）モデルをYMM4の立ち絵として自由自在に動かせるプラグインです。

- **VRM & PMXモデル完全統合**：VRM 0.x / 1.0 および PMXを透過背景で高速描画（Direct2D共有メモリ転送）。
- **リアルな母音口パク**：セリフから「あ・い・う・え・お」の母音を自動解析し、口形と音量に合わせてリアルタイム開閉。
- **部位別の表情合成**：笑顔、怒り、照れ、ジト目、ウィンクなど多数の表情に対応し、部位ごとに自然合成。
- **14種の内蔵VLOGモーション**：歩く、走る、周りを見る、見上げる、振り返る、自撮り構え、ピース、驚くなどがすぐ使える。
- **VRMポーズメーカー付属**：MMDのポーズ（.vpd）、モーション（.vmd）、VRMAを取り込んでタグ登録可能。
- **多彩なカメラ・視点**：三人称、一人称（目線）、自撮りモード（腕を伸ばして構えたスマホから撮影、体幹連動）。
- **実写背景なじませ**：実写動画の手ブレ解析による上下揺れ同期、背景光・色味の陰影反映、床へのリアルな影落とし。
- **専用映像エフェクト同梱**：手持ちスマホ揺れと立体パララックスを生み出す「VLOG手ブレ」、定番構図の「VLOGカメラワーク」。
- **生命感あふれる動き**：まばたき、視線ゆらぎ、目そらし、胸や肩が動く呼吸、待機揺れ、髪・衣装の物理演算が自然に駆動。

---

## インストール方法

1. 上記の表または各項目から、使いたいプラグインの `.ymme` ファイルをダウンロードします。
2. ゆっくりMovieMaker4（YMM4）を起動します。
3. ダウンロードした `.ymme` ファイルを YMM4 のウィンドウ上にドラッグ＆ドロップします（またはファイルをダブルクリックして開きます）。
4. プラグインのインストール確認ダイアログが表示されるので、インストールを実行します。
5. YMM4 を再起動すると、プラグインが有効になります。

※ツール系のプラグイン（ぽちぽちボード、セリフ追従、セリフのタイムスタンプ保存、ショート切り抜き、Web演出ツール）は、YMM4上部メニューの「表示」→「パネル」またはツール一覧から開くことができます。

---

## 動作環境

- OS：Windows 10 / Windows 11 (64bit)
- ホストアプリ：ゆっくりMovieMaker4（YMM4）最新版
- 実行環境：.NET 10 ランタイム（YMM4の動作環境に準拠）
- 一部プラグイン（HTML背景プラグイン等）では Microsoft Edge WebView2 ランタイムを使用します（通常のWindows環境には標準でインストールされています）。

---

## 注意事項・免責事項

- 本プラグインの利用により生じたいかなるトラブル・損害等について、作者は一切の責任を負いかねます。重要なプロジェクトファイルは定期的にバックアップを取ることを推奨します。
- 各プラグインの詳細な機能・操作方法・制約事項については、各プラグイン名の `.txt` ファイルをご確認ください。
