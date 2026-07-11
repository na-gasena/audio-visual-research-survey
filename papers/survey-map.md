# 研究マップ

## 調査方法

調査は、`audio visual learning survey`、`audio-visual datasets`、`audio visual source separation`、`audio visual speech recognition` などの広い検索語から始めました。その後、AudioSet、VGGSound、AVE、AVSpeech、AV-HuBERT、AVSBench、MUSIC-AVQA、AVSD、SoundNet、Look Listen and Learn、Sound of Pixels、Objects that Sound など、検索中に繰り返し現れた語を使って拡張しました。

作品側については、`audiovisual art`、`visual music`、`video art`、`live cinema`、`VJing`、`audiovisual installation`、作家名や作品名を使って追加調査しました。

## 自然に得られた分類

### 1. 対応学習・表現学習

中心的な問いは、音と映像が対応しているか、または片方のモダリティからもう片方を予測できるかを使って、意味的な表現を学習できるかです。代表的な手法には、対照学習、クロスモーダル蒸留、同期判定、マスクドモデリング、共有埋め込み空間があります。

### 2. 定位・分離

中心的な問いは、どの物体が音を出したのか、いつ音が発生したのか、混合音から個別の音源を分離できるかです。この系列では、視覚的注意、物体性、時間同期、スペクトログラムマスク、音源数の仮定がよく使われます。

### 3. 音声・読唇・話者映像

中心的な問いは、口唇や顔の動きが、雑音下音声認識、無音読唇、話者分離、自己教師あり音声表現にどう役立つかです。GRID、LRW、LRS2、LRS3、VoxCeleb、AVSpeech などのベンチマークがあります。

### 4. イベント理解・セグメンテーション

中心的な問いは、音と見た目の両方で定義されるイベントを、分類、時間定位、空間定位、ピクセル単位のセグメンテーションとして扱えるかです。弱ラベルの AV イベント分類、時間方向のイベント定位、音を出す物体のピクセル単位セグメンテーションが含まれます。

### 5. 質問応答・対話・生成

中心的な問いは、音響・視覚知覚を、自然言語による推論、対話、生成タスクへどう接続するかです。この領域では、視覚のみ、音のみ、テキストのみ、融合モデルのアブレーション確認が重要です。

### 6. オーディオビジュアル作品

作品としての Audio-Visual は、音と映像を入力データとして処理するだけでなく、知覚、身体、空間、時間、社会的意味を構成する媒体として扱います。視覚音楽、ビデオアート、ライブシネマ、VJ、メディアインスタレーション、AV パフォーマンス、AI/data art が含まれます。

詳細は [audiovisual-works.md](audiovisual-works.md) に分けました。

## 横断軸

| 軸 | 観察された値 |
|---|---|
| 教師信号 | 教師あり、弱教師、自己教師、対照学習、マスク予測 |
| 同期の強さ | 同期、弱同期、弱ペア、不対応 |
| 出力粒度 | クリップラベル、時間区間、空間ヒートマップ、ピクセルマスク、波形、テキスト |
| モダリティの役割 | 音をラベルにする、音をクエリにする、視覚を分離器にする、視覚を文脈にする、言語をインターフェースにする |
| 作品側の関係 | 同期、対位法、相互変換、フィードバック、没入環境、ライブ生成 |

## 推奨読書順

1. **Deep Audio-Visual Learning: A Survey** で、2020 年時点の機械学習系 AV 研究の全体像を把握します。
2. **SoundNet**、**Look Listen and Learn**、**AudioSet** で、映像が音響表現学習の大規模教師になった流れを理解します。
3. **AVE**、**Sound of Pixels**、**Objects that Sound**、**Looking to Listen** で、定位・分離の問題設定を押さえます。
4. **VGGSound** と **AV-HuBERT** で、大規模認識と自己教師あり AV 音声表現を確認します。
5. **AVSBench**、**MUSIC-AVQA**、**AVSD** で、分類・分離を超えたタスク拡張を見ます。
6. 作品側は [audiovisual-works.md](audiovisual-works.md) から読み、視覚音楽、ビデオアート、ライブ AV、インスタレーションの系譜を分けて把握します。

---

# Survey Map

## Discovery Method

The search started from broad queries such as `audio visual learning survey`, `audio-visual datasets`, `audio visual source separation`, and `audio visual speech recognition`. It was then expanded using recurring terms such as AudioSet, VGGSound, AVE, AVSpeech, AV-HuBERT, AVSBench, MUSIC-AVQA, AVSD, SoundNet, Look Listen and Learn, Sound of Pixels, and Objects that Sound.

For the artworks section, additional searches used terms such as `audiovisual art`, `visual music`, `video art`, `live cinema`, `VJing`, `audiovisual installation`, and artist/work names.

## Natural Taxonomy

### 1. Correspondence and Representation Learning

The core question is whether semantic representations can be learned by predicting whether audio and video match, or by predicting one modality from the other. Typical methods include contrastive learning, cross-modal distillation, synchronization prediction, masked modeling, and shared embedding spaces.

### 2. Localization and Separation

The core question is which object made the sound, when it sounded, and whether its sound can be separated from a mixture. This line often uses visual attention, objectness, temporal alignment, spectrogram masks, and source-count assumptions.

### 3. Speech, Lip Reading, and Talking Faces

The core question is how mouth and face motion can support noisy speech recognition, silent lip reading, speaker separation, and self-supervised speech representation learning. Benchmarks include GRID, LRW, LRS2, LRS3, VoxCeleb, and AVSpeech.

### 4. Event Understanding and Segmentation

The core question is whether events defined by both sound and appearance can be recognized, temporally localized, spatially grounded, or segmented at the pixel level. This includes weakly labeled AV event classification, temporal event localization, and pixel-level segmentation of sounding objects.

### 5. QA, Dialogue, and Generation

The core question is how audio-visual perception can support natural-language reasoning, dialogue, and generation. For this area, modality ablations across visual-only, audio-only, text-only, and fused models are especially important.

### 6. Audiovisual Works

Audiovisual works treat sound and image not only as input data, but as media for perception, body, space, time, and social meaning. This includes visual music, video art, live cinema, VJing, media installation, AV performance, and AI/data art.

Details are separated into [audiovisual-works.md](audiovisual-works.md).

## Cross-Cutting Axes

| Axis | Observed values |
|---|---|
| Supervision | supervised, weak labels, self-supervised, contrastive, masked prediction |
| Alignment | synchronized, loosely synchronized, weakly paired, unpaired |
| Output granularity | clip label, temporal segment, spatial heatmap, pixel mask, waveform, text |
| Modality role | audio as label, audio as query, vision as separator, vision as context, language as interface |
| Artwork relation | synchronization, counterpoint, translation, feedback, immersive environment, live generation |

## Reading Order

1. Start with **Deep Audio-Visual Learning: A Survey** for a 2020 snapshot of ML-oriented AV research.
2. Read **SoundNet**, **Look Listen and Learn**, and **AudioSet** to understand why video became a scalable audio supervision source.
3. Read **AVE**, **Sound of Pixels**, **Objects that Sound**, and **Looking to Listen** for localization and separation.
4. Read **VGGSound** and **AV-HuBERT** for large-scale recognition and self-supervised AV speech.
5. Read **AVSBench**, **MUSIC-AVQA**, and **AVSD** for task extensions beyond classification and separation.
6. For artworks, start with [audiovisual-works.md](audiovisual-works.md) and separate the lineages of visual music, video art, live AV, and installation.
