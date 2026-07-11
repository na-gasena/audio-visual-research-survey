# 音声・読唇

## 中心アイデア

視覚的な発話情報は、音声が雑音下にある場合、欠落している場合、複数話者が混ざっている場合に役立ちます。この領域には、読唇、AV 音声認識、アクティブ話者検出、話者映像つき音声分離、自己教師あり AV 音声表現が含まれます。

## 主要データセット

- GRID: 制御環境で収録された文レベルの AV 音声データセット。
- LRW: 野外環境に近い単語レベル読唇データセット。
- LRS2 / LRS3: 放送動画や TED 系動画を使った文レベル読唇・AV 音声認識データセット。
- VoxCeleb: インタビュー動画由来の話者認識データセットで、AV 音声・顔音声研究にも使われます。
- AVSpeech: 話者映像つき音声分離に使われる大規模 talking-face データセット。

## 代表論文

LRS 系データセットは、読唇研究を制御環境の定型文から、より現実的な Web/放送動画へ広げました。AV-HuBERT は、音声と口唇領域映像のペアから表現を学ぶ現代的な自己教師あり AV 音声研究の中核文献です。Looking to Listen は、顔トラックによって混合音から対象話者を選べることを示したため、AV 音声研究としても重要です。

## 注意点

モデルが発話内容ではなく、話者 ID や動画ソースの偏りを学ぶ可能性があります。YouTube 由来データは、時間とともに入手性が変わります。顔と音声を含むデータセットでは、ライセンス、同意、プライバシー確認が重要です。また、主要ベンチマークは英語に偏りがちです。

---

# Speech and Lip Reading

## Core Idea

Visual speech information helps when audio is noisy, missing, or mixed with other speakers. This area includes lip reading, audio-visual speech recognition, active-speaker detection, talking-face speech separation, and self-supervised AV speech modeling.

## Key Datasets

- GRID: controlled sentence-level audio-visual speech.
- LRW: word-level lip reading in the wild.
- LRS2 / LRS3: sentence-level lip reading and AV speech recognition from broadcast and TED-style videos.
- VoxCeleb: a speaker recognition dataset from interview videos, often reused for AV speech and face/audio work.
- AVSpeech: a large talking-face dataset used for audio-visual speech separation.

## Representative Papers

LRS-style datasets shifted lip reading from controlled lab sentences toward web and broadcast video. AV-HuBERT is a central reference for modern self-supervised audio-visual speech representation learning. Looking to Listen is also important for AV speech because face tracks can select a target speaker from a mixture.

## Common Risks

Models may learn speaker identity or video-source bias rather than speech content. YouTube-derived data can change over time. Face/audio datasets require careful license, consent, and privacy checks. Many benchmarks are English-heavy.
