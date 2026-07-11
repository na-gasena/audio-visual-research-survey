# 定位・分離

## 中心アイデア

定位は、音がどこで、またはいつ発生したかを推定するタスクです。分離は、混合音から特定の音源や話者を取り出すタスクです。Audio-Visual モデルは、物体、顔、動き、時間同期を手がかりにして、音だけでは難しい推定を補助します。

## 重要論文

### Audio-Visual Event Localization in Unconstrained Videos

AVE 論文は、制約の少ない動画内で「聞こえ、かつ見える」イベントを時間方向に定位するベンチマークを導入しました。クリップ全体の分類ではなく、イベントが発生する時間を扱う点が重要です。限界として、ラベルは主に時間方向のイベント単位であり、ピクセル単位の空間アノテーションではありません。

### The Sound of Pixels

映像の見た目や動きを使って、動画内の音を分離する研究です。視覚特徴とスペクトログラムマスクを結びつけ、ピクセル情報が音源分離を導けることを示しました。限界として、音源が画面内で見えていることや、訓練時の混合音の仮定に依存します。

### Objects that Sound

音を出す物体の視覚定位と音源分離を扱います。見えているすべての物体が音を出すわけではないため、音を画像へのクエリとして使う考え方が重要です。複数の音源候補が同時に存在する場合、弱教師だけで精密な定位を行うのは難しくなります。

### Looking to Listen

話者の顔映像を条件として、混合音から対象話者の音声を分離します。AVSpeech データセットにより、大規模な話者映像つき音声分離実験が可能になりました。限界として、対象話者の顔が見えていることを前提にしています。

## データセット傾向

大規模動画プラットフォームは規模を提供しますが、ラベルは弱く、動画削除により再現時の入手性が変わります。MUSIC や VGGSound のようなキュレーション済みデータセットは、規模と引き換えに、音と映像の意味的対応を強めています。

---

# Localization and Separation

## Core Idea

Localization estimates where or when sound occurs. Separation recovers a target source from a mixture. Audio-visual models use objects, faces, motion, and synchrony to constrain problems that are difficult from audio alone.

## Key Papers

### Audio-Visual Event Localization in Unconstrained Videos

The AVE paper introduced a benchmark for temporally localizing events that are both audible and visible in unconstrained videos. Its key contribution is framing event timing separately from whole-clip classification. Its labels are temporal/event-level rather than pixel-level.

### The Sound of Pixels

The Sound of Pixels uses visual appearance and motion to separate sounds from videos. It connects visual features with spectrogram masks and shows that pixels can guide source separation. Its quality depends on whether the source is visually available and whether training mixture assumptions match test scenes.

### Objects that Sound

Objects that Sound studies localization and separation of sounding objects. Because not every visible object is sounding, it treats audio as a query over the image. Precise grounding is difficult when multiple plausible sources co-occur under weak supervision.

### Looking to Listen

Looking to Listen separates target speech from a mixture by conditioning on the speaker's face video. AVSpeech enabled large-scale experiments for talking-face speech separation. The method assumes the target face is visible.

## Dataset Pattern

Large video platforms provide scale, but labels are often weak and availability can decay as videos are removed. Curated datasets such as MUSIC and VGGSound trade scale for clearer modality alignment.
