# 研究マップ / Survey Map

## 調査方法 / Discovery Method

調査は、`audio visual learning survey`、`audio-visual datasets`、`audio visual source separation`、`audio visual speech recognition` などの広い検索語から始めました。その後、検索で繰り返し現れた AudioSet、VGGSound、AVE、AVSpeech、AV-HuBERT、AVSBench、MUSIC-AVQA、AVSD、SoundNet、Look Listen and Learn、Sound of Pixels、Objects that Sound などを使って検索を拡張しました。  
The search started from broad queries such as `audio visual learning survey`, `audio-visual datasets`, `audio visual source separation`, and `audio visual speech recognition`. It was then expanded using recurring entities such as AudioSet, VGGSound, AVE, AVSpeech, AV-HuBERT, AVSBench, MUSIC-AVQA, AVSD, SoundNet, Look Listen and Learn, Sound of Pixels, and Objects that Sound.

## 自然に得られた分類 / Natural Taxonomy

### 1. 対応学習・表現学習 / Correspondence and Representation Learning

中心的な問いは、音と映像が対応しているか、または片方のモダリティからもう片方を予測できるかを使って、意味的な表現を学習できるかです。  
The core question is whether semantic representations can be learned by predicting whether audio and video match, or by predicting one modality from the other.

代表的な手法には、対照学習、クロスモーダル蒸留、同期判定、マスクドモデリング、共有埋め込み空間があります。  
Typical methods include contrastive learning, cross-modal distillation, synchronization prediction, masked modeling, and shared embedding spaces.

### 2. 定位・分離 / Localization and Separation

中心的な問いは、どの物体が音を出したのか、いつ音が発生したのか、混合音から個別の音源を分離できるかです。  
The core question is which visual object made the sound, when it sounded, and whether its sound can be separated from a mixture.

この系列では、視覚的注意、物体性、時間同期、スペクトログラムマスク、音源数の仮定がよく使われます。  
This line often uses visual attention, objectness, temporal alignment, spectrogram masks, and assumptions about the number of sources.

### 3. 音声・読唇・話者映像 / Speech, Lip Reading, and Talking Faces

中心的な問いは、口唇や顔の動きが、雑音下音声認識、無音読唇、話者分離、自己教師あり音声表現にどのように役立つかです。  
The core question is how mouth and face motion can support noisy speech recognition, silent lip reading, speaker separation, and self-supervised speech representation learning.

この領域には GRID、LRW、LRS2、LRS3、VoxCeleb、AVSpeech などの比較的成熟したベンチマークがあります。ただし、ライセンスや入手性はデータセットごとに異なります。  
This area has comparatively mature benchmarks such as GRID, LRW, LRS2, LRS3, VoxCeleb, and AVSpeech, although licensing and availability differ by dataset.

### 4. イベント理解・セグメンテーション / Event Understanding and Segmentation

中心的な問いは、音と見た目の両方で定義されるイベントを、分類、時間定位、空間定位、ピクセル単位のセグメンテーションとして扱えるかです。  
The core question is whether events defined by both sound and appearance can be recognized, temporally localized, spatially grounded, or segmented at the pixel level.

弱ラベルの AV イベント分類、時間方向のイベント定位、音を出す物体のピクセル単位セグメンテーションが含まれます。  
This includes weakly labeled AV event classification, temporal event localization, and pixel-level segmentation of sounding objects.

### 5. 質問応答・対話・生成 / QA, Dialogue, and Generation

中心的な問いは、音響・視覚知覚を、自然言語による推論、対話、生成タスクへどう接続するかです。  
The core question is how audio-visual perception can support natural-language reasoning, dialogue, and generation.

この領域のベンチマークは、認識や音声タスクほど標準化されていません。タスク特化で小規模なデータセットも多く、モダリティ別のアブレーション確認が重要です。  
Benchmarks here are less standardized than recognition or speech tasks. Many datasets are task-specific and sometimes small, making modality ablations important.

## 横断軸 / Cross-Cutting Axes

| 軸 | 観察された値 | Values observed |
|---|---|---|
| 教師信号 | 教師あり、弱教師、自己教師、対照学習、マスク予測 | supervised, weak labels, self-supervised, contrastive, masked prediction |
| 同期の強さ | 同期、弱同期、弱ペア、不対応 | synchronized, loosely synchronized, weakly paired, unpaired |
| 出力粒度 | クリップラベル、時間区間、空間ヒートマップ、ピクセルマスク、波形、テキスト | clip label, temporal segment, spatial heatmap, pixel mask, waveform, text |
| モダリティの役割 | 音をラベルにする、音をクエリにする、視覚を分離器にする、視覚を文脈にする、言語をインターフェースにする | audio as label, audio as query, vision as separator, vision as context, language as interface |

## 推奨読書順 / Reading Order

1. まず **Deep Audio-Visual Learning: A Survey** で、2020 年時点の全体像を把握します。  
   Start with **Deep Audio-Visual Learning: A Survey** for a 2020 snapshot of the field.
2. **SoundNet**、**Look Listen and Learn**、**AudioSet** を読み、映像が音響表現学習の大規模教師になった流れを理解します。  
   Read **SoundNet**, **Look Listen and Learn**, and **AudioSet** to understand why video became a scalable audio supervision source.
3. **AVE**、**Sound of Pixels**、**Objects that Sound**、**Looking to Listen** で、定位・分離の問題設定を押さえます。  
   Read **AVE**, **Sound of Pixels**, **Objects that Sound**, and **Looking to Listen** for localization and separation.
4. **VGGSound** と **AV-HuBERT** で、大規模認識と現代的な自己教師あり AV 音声表現を確認します。  
   Read **VGGSound** and **AV-HuBERT** for large-scale recognition and modern self-supervised AV speech.
5. **AVSBench**、**MUSIC-AVQA**、**AVSD** で、分類・分離を超えたタスク拡張を見ます。  
   Read **AVSBench**, **MUSIC-AVQA**, and **AVSD** for task extensions beyond classification and separation.
6. AV セグメンテーションを深掘りする場合は **From Waveforms to Pixels** を読みます。  
   Read **From Waveforms to Pixels** when focusing on audio-visual segmentation.
