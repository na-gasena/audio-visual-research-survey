# 対応学習・表現学習 / Correspondence and Representation Learning

## 中心アイデア / Core Idea

音と映像は自然に共起しますが、同じ情報を持っているわけではありません。映像は音源候補や状況を示し、音は見た目だけでは分からない出来事を示します。対応学習・表現学習では、この関係を教師信号として利用します。  
Audio and vision naturally co-occur, but they are not identical. Video can reveal likely sound sources and context, while audio can reveal events that are not visually explicit. Representation learning uses this relationship as supervision.

## 重要論文 / Key Papers

### Deep Audio-Visual Learning: A Survey

このサーベイは、初期の深層 AV 学習を、分離/定位、対応、生成、表現学習に整理しており、分野の入口として有用です。データセットと評価指標も扱っているため、タスク発見から体系的な読解へ進むための足場になります。  
This survey is a useful entry point because it organizes early deep audio-visual learning around separation/localization, correspondence, generation, and representation learning.

限界として、AV-HuBERT 系の自己教師あり学習、AV セグメンテーション、音を扱う基盤モデルなど、2022 年以降の発展は十分に含みません。  
Its limitation is that it predates much of the post-2022 work on AV-HuBERT-style self-supervision, AV segmentation, and audio-capable foundation models.

### SoundNet

SoundNet は、視覚認識モデルからの知識転移により、ラベルなし動画から音響表現を学習しました。手作業の音ラベルなしに、大規模動画を音響モデルの教師として使えることを示した点が重要です。  
SoundNet learns audio representations from unlabeled video by transferring supervision from visual recognition networks.

限界として、教師信号が視覚モデルに依存するため、見えない音源や純粋に音響的なクラスは弱く表現される可能性があります。  
A limitation is that supervision is inherited from visual models, so invisible sources and purely acoustic classes may be weakly represented.

### Look, Listen and Learn

この研究は、音と映像が対応しているかを判定する自己教師ありタスクを代表的な問題設定として普及させました。得られた表現は、下流の認識タスクへ転移できます。  
This work popularized audio-visual correspondence as a self-supervised task: predict whether audio and video match.

限界として、意味理解ではなく、データセットバイアスや単純な同期手がかりで解けてしまう場合があります。  
A limitation is that correspondence can sometimes be solved through dataset bias or easy synchronization cues rather than semantic understanding.

### AV-HuBERT

AV-HuBERT は、隠れ単位予測と自己教師あり学習を AV 音声へ適用した重要文献です。音声と口唇領域映像のペアから表現を学び、音声認識などの下流タスクに利用できます。  
AV-HuBERT applies hidden-unit prediction and self-supervised learning to paired speech audio and lip-region video.

限界として、主対象は話者顔映像つき音声であり、一般的な非音声 AV シーンへの転移は主目的ではありません。  
Its main target is talking-face speech, not general non-speech audio-visual scenes.

## 代表的手法 / Common Methods

- 音と画像/映像埋め込みの対照学習。  
  Contrastive objectives between audio and image/video embeddings.
- 視覚から音、または音から視覚へのクロスモーダル蒸留。  
  Cross-modal distillation from vision to audio or audio to vision.
- 同期判定や時間順序予測。  
  Synchronization and temporal order prediction.
- 音声単位、映像フレーム、融合トークンに対するマスクドモデリング。  
  Masked modeling over audio units, visual frames, or fused tokens.
- late fusion、early fusion、cross-attention transformer。  
  Late fusion, early fusion, and cross-attention transformers.

## 未解決課題 / Open Questions

- 同期アーティファクトやデータ収集バイアスによる近道学習をどう避けるか。  
  How to avoid shortcuts caused by synchronization artifacts or dataset bias.
- 見えない音源や画面外イベントをどう表現するか。  
  How to represent invisible sources and off-screen events.
- 共起ではなく因果的な関係を学べているか、どう評価するか。  
  How to evaluate whether representations capture causality rather than co-occurrence.
- 著作権やプライバシーに配慮しながら、大規模動画データをどう使うか。  
  How to scale with video data while respecting copyright and privacy.
