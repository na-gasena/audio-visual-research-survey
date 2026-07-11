# イベント理解・セグメンテーション / Event Understanding and Segmentation

## イベント認識 / Event Recognition

AudioSet と VGGSound は、大規模な音響/AV イベント認識を分野の中心に置きました。AudioSet は広範な弱ラベル音響イベントデータセットで、VGGSound は音と映像の意味的対応を重視してキュレーションされた AV データセットです。  
AudioSet and VGGSound made large-scale audio and audio-visual event recognition central to the field. AudioSet is broad and weakly labeled, while VGGSound is curated for audio-visual correspondence.

## イベント定位 / Event Localization

AVE は、イベントが「聞こえ、かつ見える」時間を扱います。クリップ内のすべての音が常に視覚的証拠を伴うわけではないため、クリップ分類とは別に、時間方向の定位が重要になります。  
AVE focuses on when an event is both audible and visible. This temporal framing matters because not every sound in a clip has visible evidence throughout the clip.

## AV セグメンテーション / Audio-Visual Segmentation

AVSBench は、音を出す物体をピクセル単位でセグメンテーションする問題を導入しました。ヒートマップによる大まかな定位よりも、音と対応する物体境界をより精密に推定する必要があります。  
AVSBench introduced pixel-level segmentation of sounding objects, requiring sharper spatial grounding than coarse localization heatmaps.

2025 年の **From Waveforms to Pixels** は、このサブフィールドの集中的なサーベイです。問題設定、ベンチマーク、評価指標、融合設計、デコーダ、訓練パラダイムを整理しています。  
The 2025 survey **From Waveforms to Pixels** provides a focused map of problem formulation, benchmarks, metrics, fusion design, decoder choices, and training paradigms.

## 手法ファミリー / Method Families

- 2-stream encoder と late fusion。  
  Two-stream encoders with late fusion.
- スペクトログラム/音声トークンと視覚パッチの cross-modal attention。  
  Cross-modal attention between spectrogram/audio tokens and visual patches.
- 弱ラベルのための multiple-instance learning。  
  Multiple-instance learning for weak clip labels.
- イベント定位のための temporal proposal や attention。  
  Temporal proposal or attention mechanisms for event localization.
- ピクセルマスクを出す decoder-style segmentation head。  
  Decoder-style segmentation heads for pixel masks.

## 評価上の注意 / Evaluation Notes

イベント分類の精度だけでは、モデルが本当に音と映像を対応づけているか分かりません。定位やセグメンテーションでは、クリップ精度だけでなく、時間方向または空間方向の評価指標を確認する必要があります。  
Event classification metrics can hide poor grounding. Localization and segmentation should report temporal or spatial metrics, not only clip accuracy.
