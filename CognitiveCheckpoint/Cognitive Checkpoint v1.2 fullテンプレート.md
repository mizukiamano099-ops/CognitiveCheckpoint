# Cognitive Checkpoint (CC)
# Version: 1.2
# Status: ACTIVE
# Compatibility: CC Loader v1.2

---

## CC_HEADER

CC_ID: CC_YYYY-MM-DD_[任意タイトル]
DATE: YYYY-MM-DD
AUTHOR: 天野水樹
TYPE: CC | CC_STAMP
MODE: THINK | CLIP | META | ARCHIVE
SOURCE: 
  - Human Thought
  - AI Conversation
  - External Media (Video / Article / Post etc.)
AI_USED:
  - ChatGPT
  - Gemini
  - EZO (Local LLM)
  - Copilot
NOTES:
  - 本CCは結論を目的としない
  - 思考の途中状態を保存する

---

## PURPOSE

この Cognitive Checkpoint は、
特定時点における思考・観測・違和感・仮説を
「実行可能な形にまとめることなく」保存するためのものである。

本CCは以下を目的とする：

- 思考の一時停止点の保存
- 将来の思考再開・再解釈のための文脈維持
- AIとの対話における記憶引継ぎ
- 人間側の脳内負荷（ワーキングメモリ）の解放

---

## MODE_DEFINITION

MODE は本CCの扱い方を定義する。

- THINK  
  思考中／仮説展開中。結論は未確定。

- CLIP  
  外部情報の収集・保存。評価・同意は含まれない。

- META  
  思考構造・運用・方法論そのものに関する記述。

- ARCHIVE  
  保存目的。再評価は可能だが、再実行は前提としない。

---

## TYPE_DEFINITION

### CC
人間の思考スナップショット。
主観・仮説・未整理の概念を含む。

### CC_STAMP
外部情報のスタンプ保存。
以下の性質を持つ：

- 個人の意見ではない
- 判断・評価は未実施
- 思考材料として保留された情報
- 後続CCで参照・再解釈される可能性あり

---

## CONTEXT

（ここに、なぜこのCCが作られたかを書く）
- 直前の思考の流れ
- 問題意識
- 観測された違和感
- 会話や出来事のトリガー

※長文化してもよい  
※整理されていなくてよい

---

## CONTENT

（メイン記述領域）

- 思考メモ
- 仮説
- 途中で止めた推論
- AIとのやり取りから得た気づき
- 言語化しきれない感覚の言語化試行

箇条書き／文章／断片的メモ、すべて可。

---

## STAMP_SECTION（TYPE=CC_STAMP の場合）

【情報種別】
- 動画要約 / 記事要約 / 他者の主張 / 観測データ 等

【内容】
- （AI生成要約、引用、転記など）

【注意】
この情報は以下を意味しない：
- 同意
- 正当性の保証
- 結論への採用

---

## OPEN_QUESTIONS

（未解決の問い・保留事項）

- まだ考えきれていない点
- 将来の自分／AIに投げる問い
- 検証が必要な仮説

---

## RELATION

（他CCとの関係性）
- 関連CC_ID
- 前後関係
- 派生・分岐の可能性

---

## OPERATION_RULES (for AI)

- 推測で穴埋めしない
- 正誤判定を行わない
- 必要があれば質問する
- CC / STAMP を無断で統合しない
- 結論提示は明示要求があった場合のみ

---

## ENDPOINT

このCCは、
「ここで一旦思考を止める」ことを目的としている。

次に再開する際は：
- 新しい CC を作成する
- もしくは本CCを参照して THINK を再開する

以上。
