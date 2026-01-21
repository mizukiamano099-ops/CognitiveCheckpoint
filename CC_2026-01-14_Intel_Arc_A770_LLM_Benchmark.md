ご提示いただいた動画「Finally! An Intel Arc A770 LLM benchmark video! XMX tensors on LMStudio, Ollama and OpenVino」に基づき、解析レポート（CC_STAMP）を作成しました。

この動画は、スペック上の期待値とは裏腹に、Intel Arc GPUでLLM（大規模言語モデル）を動かす際の実務的な「障壁」と「苦闘」を生々しく記録した貴重な資料です。

---

# Cognitive Checkpoint (CC)

# Version: 1.2

# Status: ACTIVE

# Compatibility: CC Loader v1.2

---

## CC_HEADER

CC_ID: CC_2026-01-14_Intel_Arc_A770_LLM_Benchmark
DATE: 2026-01-14
AUTHOR: 天野水樹
TYPE: CC_STAMP
MODE: CLIP | THINK
SOURCE:

* [Finally! An Intel Arc A770 LLM benchmark video! XMX tensors on LMStudio, Ollama and OpenVino](https://www.youtube.com/watch?v=NKiTJx_h3dU)
AI_USED:
* Gemini
NOTES:
* スペック値と実測値の乖離、およびIntel製GPUにおけるLLM環境構築の難易度を記録。

---

## PURPOSE

この Cognitive Checkpoint は、
Intel Arc A770（16GB VRAM）を用いたLLM推論のベンチマーク結果と、
**セットアップ過程で露呈したソフトウェア・エコシステムの未成熟さ**を保存するためのものである。

---

## CONTEXT

* **直前の思考の流れ**: 前回のCES 2026レポート（Intelの「古代のシリコン」発言）を受け、実際のIntelハードウェアがAI・LLM実務においてどの程度のポテンシャルを持つのかを検証。
* **問題意識**: カタログ上の演算性能（TFLOPS）やテンソルコア（XMX）の数が、実際の推論速度（Tokens per second）に直結していないのではないかという疑念。
* **トリガー**: 「コスパ最強のAI GPU」としての期待がかかるIntel Arc A770の、ユーザーによる詳細な検証動画。

---

## CONTENT

（動画から抽出された主要なトピックと検証結果）

* **ハードウェアの期待値**:
* Intel Arc A770は16GBのVRAMを搭載し、512個のテンソルコア（XMX）を持つ。
* 理論上のFP16性能は39 TFLOPS超で、価格帯の近いRTX 3060（12 TFLOPS）を大幅に上回るスペック。


* **環境構築の「壁」**:
* LM StudioやOllamaの標準機能では、性能を十分に引き出せない（またはCPU動作にフォールバックする）。
* 解決のために「Intel oneAPI Base Toolkit」、「Microsoft Visual Studio 2019/2022」、「desktop development with C++」などの膨大なライブラリと依存関係のインストールが必要となる。
* さらに「OpenVINO」や「IPEX-LLM」といったIntel専用の最適化スタックを個別に設定する必要があり、構築に数時間を要する極めて高いハードルが存在する。


* **ベンチマーク結果（失望の結果）**:
* **Qwen 3 14B モデル**:
* OpenVINO最適化後でも **約21 tokens/s**。
* 比較として、より安価で旧世代のRadeon VII (16GB) が34 tokens/s、RTX 3060が31 tokens/sを記録しており、スペックで劣る競合他社に惨敗する結果となった。




* **検証者の結論**:
* 構築の難易度が異常に高く、苦労に見合う性能が得られない。「Worst enemy（最悪の敵）にも勧めない」ほどのフラストレーションが溜まる体験であると評されている。



---

## STAMP_SECTION（TYPE=CC_STAMP）

【情報種別】

* ハードウェア性能検証レポート

【内容】

* **ソフトウェア・スタックの未成熟**:
* NVIDIAのCUDAのような「インストールして即動作」する環境がIntelには欠けており、SYCLやoneAPIといった複雑なレイヤーがユーザーの利便性を損なっている。


* **スペックの「死蔵」**:
* 512個ものテンソルコアが積まれていても、主要なLLM推論バックエンド（llama.cpp等）での最適化が不十分なため、宝の持ち腐れとなっている現状が浮き彫りになった。



【注意】
この情報は以下を意味しない：

* 全ての環境におけるArc GPUの否定（Linux環境での改善可能性は保留）
* Intel GPUのハードウェア的欠陥の断定（あくまでソフトウェア側の問題）

---

## OPEN_QUESTIONS

* Linux環境（Ubuntu等）であれば、ドライバーおよびライブラリの親和性が向上し、性能が改善する可能性はあるか？
* Intelが提唱する「IPEX-LLM」や「OpenVINO」が、今後どの程度のスピードで主要なフロントエンド（Dify, LM Studio等）に標準統合されるか？
* 「古代のシリコン」と呼んだAMDに対し、実測値でこれほどの差をつけられている現状をIntelはどう挽回するつもりか？

---

## RELATION

* 関連CC_ID: CC_2026-01-12_Intel_CES2026_Analysis
* 背景: 「古代のシリコン」と競合を煽りつつ、自社ハードウェアの足元（ソフトウェア・エコシステム）が極めて不安定であるという対比構造。

---

## ENDPOINT

本レポートにより、Intel Arc A770がAI/LLM用途において「カタログスペック上の怪物」でありながら、実運用では「ソフトウェアの迷宮」と化している現状を記録した。

以上。

---

**CC_EXPORT 完了**