# イベント理解・セグメンテーション

## イベント認識

AudioSet と VGGSound は、大規模な音響/AV イベント認識を分野の中心に置きました。AudioSet は広範な弱ラベル音響イベントデータセットで、VGGSound は音と映像の意味的対応を重視してキュレーションされた AV データセットです。

## イベント定位

AVE は、イベントが「聞こえ、かつ見える」時間を扱います。クリップ内のすべての音が常に視覚的証拠を伴うわけではないため、クリップ分類とは別に、時間方向の定位が重要になります。

## AV セグメンテーション

AVSBench は、音を出す物体をピクセル単位でセグメンテーションする問題を導入しました。ヒートマップによる大まかな定位よりも、音と対応する物体境界をより精密に推定する必要があります。2025 年の **From Waveforms to Pixels** は、このサブフィールドの集中的なサーベイです。

## 手法ファミリー

- 2-stream encoder と late fusion
- スペクトログラム/音声トークンと視覚パッチの cross-modal attention
- 弱ラベルのための multiple-instance learning
- イベント定位のための temporal proposal や attention
- ピクセルマスクを出す decoder-style segmentation head

## 評価上の注意

イベント分類の精度だけでは、モデルが本当に音と映像を対応づけているか分かりません。定位やセグメンテーションでは、クリップ精度だけでなく、時間方向または空間方向の評価指標を確認する必要があります。

---

# Event Understanding and Segmentation

## Event Recognition

AudioSet and VGGSound made large-scale audio and audio-visual event recognition central to the field. AudioSet is broad and weakly labeled, while VGGSound is curated for audio-visual correspondence.

## Event Localization

AVE focuses on when an event is both audible and visible. This temporal framing matters because not every sound in a clip has visible evidence throughout the clip.

## Audio-Visual Segmentation

AVSBench introduced pixel-level segmentation of sounding objects, requiring sharper spatial grounding than coarse localization heatmaps. The 2025 survey **From Waveforms to Pixels** provides a focused map of this subfield.

## Method Families

- Two-stream encoders with late fusion
- Cross-modal attention between spectrogram/audio tokens and visual patches
- Multiple-instance learning for weak clip labels
- Temporal proposal or attention mechanisms for event localization
- Decoder-style segmentation heads for pixel masks

## Evaluation Notes

Event classification metrics can hide poor grounding. Localization and segmentation should report temporal or spatial metrics, not only clip accuracy.
