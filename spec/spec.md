## アプリケーション名: EmoDialog

### 概要
EmoDialogは，ユーザーが日記を記録し，AIとの会話を通じて感情や思考を共有することができるアプリケーションである．ユーザーが日記を書くと，AIが自動的にその内容を分析し，適切な応答を生成する．またユーザーはAIとの会話を通じて気持ちを整理したり，アドバイスを受けたりすることができる．今までの日記のデータを集計して，ユーザーの感情や思考の変化を可視化する機能も提供する．

### 背景
"EmoDialog" は，"Emo" は感情（emotion）を表し，"Dialog" は対話（dialogue）を表す言葉である．この名前は，感情を中心に据えた対話やコミュニケーションを促進するアプリケーションを示している．感情と対話を融合させることで，ユーザーが自分の感情や思考をより深く理解し，整理する手助けをすることを意味している．

### 機能

1. **日記記録機能**
   - ユーザーが日記を入力できるテキストエリアを提供する．
      - 文章入力を行う操作
         - 最大文字数は500文字とする．
      - 日記の内容を保存する操作
         - 保存される内容は日付と日記の内容．
      - 日記の内容を破棄する操作
         - 戻る操作を行うと，日記の内容が破棄される．
         - 破棄する前に確認メッセージを表示する．
   - 日記はユーザーが過去の記録を参照できる．
      - 過去の日記を閲覧する操作
         - 過去の日記を新しい順に表示する．
      - 過去の日記を削除する操作
         - 削除する前に確認メッセージを表示する．

2. **AIとの会話機能**
   - 日記のスレッドでAIとの会話を行うことができる．
      - AIとの会話を開始する操作
         - ユーザーが日記を入力すると，自動的にAIがその内容を分析し，適切な応答をはじめに生成する．
      - AIとの会話を続ける操作
         - ユーザーがAIに質問を投げると，文脈に基づいてAIが適切な回答を生成する．
   - ユーザーがAIとの会話を開始できる独立したインタフェースを提供する．
      - AIとの会話を開始する操作
         - ユーザーがAIに挨拶をすると，AIが応答する．
         - ユーザーがAIに質問を投げると，AIが適切な回答を生成する．
      - AIとの会話を終了する操作
         - 戻る操作を行うと，AIとの会話が終了する．
         - 会話の内容は保存されない．

3. **感情分析**
   - ユーザーが日記を記録すると，AIがその内容を分析し，ユーザーの感情や思考を蓄積する．
      - 抽出された感情や思考を閲覧する操作
         - 日付ごとにグラフやチャートなどで可視化する．
   - 抽出された感情や思考は，ユーザーとの会話で利用される．
      - ユーザーがAIに質問を投げると，AIが過去の日記の内容を参照して適切な回答を生成する．

### 技術スタック

- フロントエンド: メインの言語はPythonを使用し，GUIはStremlitやKivy，Hugging Faceなどのライブラリで表現する．
- バックエンド: OpenAI社のGPTモデルを使用する．
- データベース: ユーザーの日記エントリーや会話のデータを保存するためにAWSやGCPのデータベースを使用する．
