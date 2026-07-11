# Audio-Visual 研究サーベイ / Audio-Visual Research Survey

このリポジトリは、**Audio-Visual / Audiovisual（音響・視覚）研究**を対象にした、GitHub 公開向けの研究サーベイです。音と映像を組み合わせた、表現学習、認識、定位、分離、セグメンテーション、質問応答、対話、生成を扱います。  
This repository is a GitHub-ready survey of **audio-visual / audiovisual research**, covering representation learning, recognition, localization, separation, segmentation, QA, dialogue, and generation across sound and vision.

分類は最初から固定せず、広い検索語から出発して、サーベイ論文、一次論文、公式データセットページ、プロジェクトページで繰り返し現れたタスク・データセット・会議をもとに整理しました。  
The taxonomy was not fixed in advance. It was built from broad search terms and then refined around recurring tasks, datasets, and venues found in surveys, primary papers, official dataset pages, and project pages.

## 対象範囲 / Scope

Audio-Visual 研究では、映像、音声波形、スペクトログラム、発話、音楽、イベント、言語などを、同期または弱同期したマルチモーダル信号として扱います。研究領域は、コンピュータビジョン、機械学習、音声・音響、マルチメディア、ロボティクス、HCI、自然言語処理にまたがります。  
Audio-visual research treats video, waveforms, spectrograms, speech, music, events, and language as synchronized or weakly aligned multimodal signals. It spans computer vision, machine learning, speech and audio, multimedia, robotics, HCI, and NLP.

## 調査から得られた主要カテゴリ / Emergent Categories

| 日本語カテゴリ | English category | 典型的な入力 -> 出力 | 代表データセット |
|---|---|---|---|
| 対応学習・表現学習 | Audio-visual correspondence and representation learning | 映像 + 音 -> 共有表現、自己教師あり表現 | Flickr-SoundNet, AudioSet, VGGSound |
| 音源定位・イベント定位 | Sound source and event localization | 映像 + 音 -> 空間的/時間的な音イベント位置 | AVE, Flickr-SoundNet, VGGSound |
| 音源分離・音声強調 | Audio-visual source separation and enhancement | 混合音 + 映像 -> 分離音、強調音声 | MUSIC, AVSpeech, VoxCeleb |
| AV 音声認識・読唇・話者分離 | Audio-visual speech, lip reading, and speech separation | 顔/映像 + 音 -> テキスト、分離音声 | GRID, LRW, LRS2, LRS3, AVSpeech, VoxCeleb |
| イベント認識・シーン理解 | Audio-visual event recognition and scene understanding | 映像 + 音 -> クラスラベル、イベント | AudioSet, VGGSound, AVE |
| AV セグメンテーション | Audio-visual segmentation | 映像 + 音 -> 音を出す物体のピクセルマスク | AVSBench |
| AV 質問応答・対話 | Audio-visual question answering and dialogue | 映像 + 音 + テキスト -> 回答、応答 | AVSD, MUSIC-AVQA, AVQA |
| AV 生成・同期 | Audio-visual generation and synchronization | 映像/音/テキスト条件 -> 生成音・生成映像・同期スコア | LRS2/LRS3, VoxCeleb, AVSpeech |
| 音楽・感情・人間中心理解 | Music, affect, and human-centered AV understanding | 演奏/顔/身体/音 -> ラベル、感情、楽器 | MUSIC, VoxCeleb, CMU-MOSEI |

研究の全体地図は [papers/survey-map.md](papers/survey-map.md)、論文メタデータは [data/papers.yaml](data/papers.yaml) にあります。  
The research map is in [papers/survey-map.md](papers/survey-map.md), and structured paper metadata is in [data/papers.yaml](data/papers.yaml).

## 主要会議・ジャーナル / Major Venues

収集した論文で特に多く現れた会議・ジャーナルは次の通りです。  
The most frequently recurring venues in the collected papers are:

- コンピュータビジョン・機械学習: CVPR, ICCV, ECCV, NeurIPS, ICML, ICLR, TPAMI.
- マルチメディア・音声・音響: ACM Multimedia, ICASSP, INTERSPEECH, WASPAA, DCASE Workshop.
- 言語・対話・人間中心マルチモーダル: ACL, EMNLP, NAACL, ICMI.

詳細は [data/venues.yaml](data/venues.yaml) にまとめています。  
Details are listed in [data/venues.yaml](data/venues.yaml).

## 入口となる重要文献 / Key Starting Points

- **Deep Audio-Visual Learning: A Survey**: 2020 年時点の AV 学習を、分離/定位、対応、生成、表現学習に整理した入口文献。  
  A useful 2020 map of separation/localization, correspondence, generation, and representation learning.
- **From Waveforms to Pixels**: AV セグメンテーションに焦点を当てた近年のサーベイ。  
  A recent survey focused on audio-visual segmentation.
- **SoundNet**: 視覚モデルを教師として、ラベルなし動画から音響表現を学習した研究。  
  Self-supervised audio representation learning from unlabeled video.
- **Look, Listen and Learn**: 音と映像が対応するかどうかを自己教師信号として使った代表的研究。  
  A representative audio-visual correspondence learning paper.
- **AudioSet**: YouTube 由来の大規模弱ラベル音響イベントデータセット。  
  A large-scale weakly labeled audio event dataset.
- **AVE**: 聞こえ、かつ見えるイベントを時間方向に定位するベンチマーク。  
  A benchmark for audio-visual event localization.
- **The Sound of Pixels / Objects that Sound**: 音を出す物体の定位と分離を扱う代表的研究。  
  Representative work on localizing and separating sounding objects.
- **Looking to Listen / AVSpeech**: 顔映像を用いた話者音声分離と、そのための大規模データセット。  
  Visually guided speech separation and a large talking-face dataset.
- **VGGSound**: 音と映像の意味的対応を重視した大規模 AV 認識データセット。  
  A large-scale curated audio-visual recognition dataset.
- **AV-HuBERT**: AV 音声向けの自己教師あり表現学習。  
  Self-supervised audio-visual speech representation learning.
- **AVSBench**: 音を出す物体のピクセル単位セグメンテーションベンチマーク。  
  A pixel-level audio-visual segmentation benchmark.
- **MUSIC-AVQA / AVSD**: AV 質問応答・対話の代表的ベンチマーク。  
  Representative benchmarks for audio-visual QA and dialogue.

## リポジトリ構成 / Repository Structure

```text
README.md
references.bib
data/
  papers.yaml
  datasets.yaml
  venues.yaml
papers/
  survey-map.md
  representation-learning.md
  localization-and-separation.md
  speech-and-lip-reading.md
  event-understanding-and-segmentation.md
  qa-dialogue-and-generation.md
audit-report.md
```

## YAML ファイルの役割 / Why YAML Files Exist

`data/*.yaml` は、人間が読む本文とは別に、論文・データセット・会議の情報を機械処理しやすい形で保存するためのファイルです。README やトピックページは「読むため」の文書、YAML は「再利用するため」のデータです。キー名はスクリプト処理しやすいように英語で統一していますが、説明文には日本語項目を含めています。  
The `data/*.yaml` files store papers, datasets, and venues as reusable structured data. Markdown files are for reading; YAML files are for processing. Field names are kept in English for scripting, while Japanese descriptions are included where useful.

たとえば、YAML があると次のような使い方ができます。  
For example, YAML enables:

- 論文一覧表を README に自動生成する。  
  Automatically generating paper tables for the README.
- `task_categories: ["source-separation"]` の論文だけを抽出する。  
  Filtering only papers tagged as `source-separation`.
- データセットごとのタスク、入力、ライセンス注意点を一覧化する。  
  Listing tasks, inputs, and license notes per dataset.
- BibTeX キーの抜け、URL の抜け、リンク切れを CI で検査する。  
  Checking missing BibTeX keys, missing URLs, and broken links in CI.
- 将来、Web ページや検索 UI を作るときの元データにする。  
  Reusing the data for a future website or search interface.

## 情報源ポリシー / Source Policy

一次論文、公式プロジェクトページ、arXiv、OpenReview、ACL Anthology、IEEE、ACM、公式データセットページを優先しました。確認できない情報は `Unknown` と書き、推測で埋めない方針にしています。  
Primary papers, official project pages, arXiv, OpenReview, ACL Anthology, IEEE, ACM, and official dataset pages were preferred. Unverified details are marked `Unknown` rather than guessed.

## 限界 / Limitations

これは初版の公開向けサーベイです。Web で確認可能な一次情報に基づくため、2025-2026 年の最新研究、非英語文献、ロボティクス寄りの AV 研究、商用または非公開データセットを使う研究は不足している可能性があります。  
This is a first-pass public survey. Because it relies on web-accessible primary sources, it may underrepresent very recent 2025-2026 work, non-English publications, robotics-oriented audio-visual work, and research using commercial or non-public datasets.
