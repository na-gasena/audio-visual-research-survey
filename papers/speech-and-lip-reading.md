# 音声・読唇 / Speech and Lip Reading

## 中心アイデア / Core Idea

視覚的な発話情報は、音声が雑音下にある場合、欠落している場合、複数話者が混ざっている場合に役立ちます。この領域には、読唇、AV 音声認識、アクティブ話者検出、話者映像つき音声分離、自己教師あり AV 音声表現が含まれます。  
Visual speech information helps when audio is noisy, missing, or mixed with other speakers. This area includes lip reading, audio-visual speech recognition, active-speaker detection, talking-face speech separation, and self-supervised AV speech modeling.

## 主要データセット / Key Datasets

- GRID: 制御環境で収録された文レベルの AV 音声データセット。  
  Controlled sentence-level audio-visual speech.
- LRW: 野外環境に近い単語レベル読唇データセット。  
  Word-level lip reading in the wild.
- LRS2 / LRS3: 放送動画や TED 系動画を使った文レベル読唇・AV 音声認識データセット。  
  Sentence-level lip reading and AV speech recognition from broadcast and TED-style videos.
- VoxCeleb: インタビュー動画由来の話者認識データセットで、AV 音声・顔音声研究にも使われます。  
  A speaker recognition dataset from interview videos, often reused for AV speech and face/audio work.
- AVSpeech: 話者映像つき音声分離に使われる大規模 talking-face データセット。  
  A large talking-face dataset used for audio-visual speech separation.

## 代表論文 / Representative Papers

### Lip Reading Sentences in the Wild

LRS 系データセットは、読唇研究を制御環境の定型文から、より現実的な Web/放送動画へ広げました。モデルだけでなく、文レベルの視覚音声評価を現実的にしたベンチマークとして重要です。  
LRS-style datasets shifted lip reading from controlled lab sentences toward unconstrained web and broadcast video.

### AV-HuBERT

AV-HuBERT は、現代的な自己教師あり AV 音声研究の中核文献です。音声と口唇領域映像のペアから表現を学び、音声認識などに利用できます。  
AV-HuBERT is a central reference for modern self-supervised audio-visual speech representation learning.

### Looking to Listen

Looking to Listen は音源分離の論文でもありますが、顔トラックによって混合音から対象話者を選べることを示したため、AV 音声研究としても重要です。  
Looking to Listen is also a separation paper, but it is important for AV speech because face tracks can select a target speaker from a mixture.

## 注意点 / Common Risks

- モデルが発話内容ではなく、話者 ID や動画ソースの偏りを学ぶ可能性があります。  
  Models may learn speaker identity or video-source bias rather than speech content.
- YouTube 由来データは、時間とともに入手性が変わります。  
  YouTube-derived data can change over time.
- 顔と音声を含むデータセットでは、ライセンス、同意、プライバシー確認が重要です。  
  Face/audio datasets require careful license, consent, and privacy checks.
- 主要ベンチマークは英語に偏りがちです。  
  Many benchmarks are English-heavy.
