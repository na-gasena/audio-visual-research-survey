# 質問応答・対話・生成

## AV 質問応答

AV 質問応答では、音、映像、またはその両方を必要とする自然言語質問に回答します。MUSIC-AVQA は音楽動画を対象とした代表例で、楽器、見た目、実際に音を出している音源の関係を推論する必要があります。

## AV シーン対話

AVSD は、動画、音、対話履歴を使って応答を生成または選択するタスクです。AV 知覚を単なる分類ではなく、対話的な言語タスクへ接続した点が重要です。

## 生成・同期

生成系の研究には、talking-face 生成、音声駆動アニメーション、動画からの音生成、Foley 風効果音生成、AV 同期判定などがあります。この領域はベンチマークが分散しており、主観評価や知覚評価が必要になることも多いです。

## 限界

QA や対話データセットには、アノテーション由来の偏りが入る可能性があります。質問によっては、音を使わず言語事前知識だけで答えられる場合があります。生成音・生成映像の品質は、論文間で比較しにくいです。

## 推奨監査

QA、対話、生成の論文では、視覚のみ、音のみ、テキストのみ、融合モデルのアブレーションがあるかを確認するべきです。アブレーションがない場合、その手法が本当に AV 証拠を使っているか判断しにくくなります。

---

# QA, Dialogue, and Generation

## Audio-Visual QA

Audio-visual question answering asks models to answer natural-language questions that may require sound, vision, or both. MUSIC-AVQA is a representative music-domain example requiring reasoning about instruments, appearance, and sounding sources.

## Audio-Visual Scene-Aware Dialogue

AVSD uses video, audio, and dialogue history to generate or select responses. It extends audio-visual perception into interactive language tasks rather than only classification.

## Generation and Synchronization

Generation work includes talking-face generation, speech-driven animation, video-to-audio generation, Foley-style sound generation, and audio-visual synchronization. Benchmarks are fragmented, and subjective or perceptual evaluation is often needed.

## Limitations

QA and dialogue datasets may encode annotation artifacts. Some questions can be answered from language priors without using audio. Generated audio/video quality is difficult to compare across papers.

## Recommended Audit

For QA, dialogue, and generation papers, check whether they report visual-only, audio-only, text-only, and fused-model ablations. Without ablations, it is hard to know whether the method truly uses audio-visual evidence.
