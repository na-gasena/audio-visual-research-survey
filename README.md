# Audio-Visual 研究サーベイ

このリポジトリは、**Audio-Visual / Audiovisual（音響・視覚）研究と作品**を対象にした、GitHub 公開向けのサーベイです。音と映像を組み合わせた機械学習研究だけでなく、視覚音楽、ビデオアート、ライブ AV、メディアインスタレーションなどの作品系譜も扱います。

現在の論文サーベイに含まれる文献年は、収録済みエントリ上では **2016-2025 年**です。検索時に年フィルタはかけていませんが、英語圏で `audio-visual learning` や `audiovisual datasets` と検索すると、深層学習以後の機械学習研究が強く出るため、初版はその方向に寄っています。作品サーベイは、この偏りを補正するために追加しました。

分類は最初から固定せず、広い検索語から出発して、サーベイ論文、一次論文、公式データセットページ、プロジェクトページ、作家・美術館・展示関連ページで繰り返し現れたタスク、データセット、会議、作品形式をもとに整理しました。

## 対象範囲

研究側では、映像、音声波形、スペクトログラム、発話、音楽、イベント、言語などを、同期または弱同期したマルチモーダル信号として扱います。主な領域は、コンピュータビジョン、機械学習、音声・音響、マルチメディア、自然言語処理です。

作品側では、音と映像を分類対象や入力データとしてではなく、知覚、身体、空間、時間、社会的意味を作る媒体として扱います。視覚音楽、ビデオアート、ライブシネマ、VJ、舞台、インスタレーション、AI/data art などが含まれます。

## 調査から得られた主要カテゴリ

| カテゴリ | 典型的な入力と出力 | 代表例 |
|---|---|---|
| 対応学習・表現学習 | 映像 + 音 -> 共有表現、自己教師あり表現 | SoundNet, Look Listen and Learn, AV-HuBERT |
| 音源定位・イベント定位 | 映像 + 音 -> 空間的/時間的な音イベント位置 | AVE, Objects that Sound |
| 音源分離・音声強調 | 混合音 + 映像 -> 分離音、強調音声 | The Sound of Pixels, Looking to Listen |
| AV 音声認識・読唇 | 顔/映像 + 音 -> テキスト、分離音声 | GRID, LRW, LRS2, LRS3, AVSpeech |
| イベント認識・シーン理解 | 映像 + 音 -> クラスラベル、イベント | AudioSet, VGGSound, AVE |
| AV セグメンテーション | 映像 + 音 -> 音を出す物体のピクセルマスク | AVSBench |
| AV 質問応答・対話 | 映像 + 音 + テキスト -> 回答、応答 | MUSIC-AVQA, AVSD |
| AV 生成・同期 | 条件入力 -> 生成音、生成映像、同期スコア | talking-face, Foley, video-to-audio |
| オーディオビジュアル作品 | 音 + 映像 + 空間 + 身体 -> 鑑賞経験、展示、ライブ | Fischinger, Paik, Dumb Type, Ikeda |

## 主要会議・ジャーナル

収集した論文で特に多く現れた会議・ジャーナルは次の通りです。

- コンピュータビジョン・機械学習: CVPR, ICCV, ECCV, NeurIPS, ICML, ICLR, TPAMI
- マルチメディア・音声・音響: ACM Multimedia, ICASSP, INTERSPEECH, WASPAA, DCASE Workshop
- 言語・対話・人間中心マルチモーダル: ACL, EMNLP, NAACL, ICMI

## 入口となる重要文献・作品

- **Deep Audio-Visual Learning: A Survey**: 2020 年時点の AV 学習を、分離/定位、対応、生成、表現学習に整理した入口文献。
- **From Waveforms to Pixels**: AV セグメンテーションに焦点を当てた近年のサーベイ。
- **SoundNet**: 視覚モデルを教師として、ラベルなし動画から音響表現を学習した研究。
- **Look, Listen and Learn**: 音と映像が対応するかどうかを自己教師信号として使った代表的研究。
- **AudioSet / VGGSound**: 大規模な音響・AV イベント認識の基盤データセット。
- **AVE / AVSBench**: AV イベント定位と AV セグメンテーションの代表的ベンチマーク。
- **Visual music / video art / live audiovisual performance**: Oskar Fischinger、Mary Ellen Bute、Nam June Paik、Dumb Type、Bill Viola、Ryoji Ikeda などの作品系列。

## 読むページ

- [研究マップ](papers/survey-map.md): 分野全体の分類、横断軸、推奨読書順。
- [対応学習・表現学習](papers/representation-learning.md): SoundNet、Look Listen and Learn、AV-HuBERT など。
- [定位・分離](papers/localization-and-separation.md): AVE、Sound of Pixels、Objects that Sound、Looking to Listen など。
- [音声・読唇](papers/speech-and-lip-reading.md): GRID、LRW、LRS2/LRS3、AVSpeech、AV-HuBERT など。
- [イベント理解・セグメンテーション](papers/event-understanding-and-segmentation.md): AudioSet、VGGSound、AVE、AVSBench など。
- [質問応答・対話・生成](papers/qa-dialogue-and-generation.md): MUSIC-AVQA、AVSD、talking-face、Foley 生成など。
- [オーディオビジュアル作品](papers/audiovisual-works.md): 視覚音楽、ビデオアート、ライブ AV、メディアインスタレーションなど。
## リポジトリ構成

```text
README.md
references.bib
data/
  papers.yaml
  datasets.yaml
  venues.yaml
  artworks.yaml
papers/
  survey-map.md
  representation-learning.md
  localization-and-separation.md
  speech-and-lip-reading.md
  event-understanding-and-segmentation.md
  qa-dialogue-and-generation.md
  audiovisual-works.md
audit-report.md
```

## YAML ファイルの役割

`data/*.yaml` は、人間が読む本文とは別に、論文、データセット、会議、作品の情報を機械処理しやすい形で保存するためのファイルです。Markdown は読むための文書、YAML は再利用するためのデータです。

YAML があると、論文一覧表の自動生成、特定カテゴリの論文抽出、データセットごとのタスク一覧化、BibTeX キーや URL の不足チェック、将来の Web ページや検索 UI の生成がしやすくなります。

## GitHub Pages で公開する手順

このリポジトリは、GitHub Pages で Markdown サイトとして読めるように `index.md` と `_config.yml` を追加しています。公開する場合は、GitHub 上で次の設定を行います。

1. GitHub のリポジトリページで **Settings** を開く。
2. 左メニューから **Pages** を開く。
3. **Build and deployment** の Source を **Deploy from a branch** にする。
4. Branch を `main`、folder を `/ (root)` にする。
5. Save する。

その後、GitHub Pages の URL から `index.md` を入口として各 Markdown ページを閲覧できます。
## 情報源ポリシー

一次論文、公式プロジェクトページ、arXiv、OpenReview、ACL Anthology、IEEE、ACM、公式データセットページ、作家公式ページ、美術館ページを優先しました。確認できない情報は `Unknown` と書き、推測で埋めない方針にしています。

## 限界

これは初版の公開向けサーベイです。2025-2026 年の最新研究、非英語文献、ロボティクス寄りの AV 研究、商用または非公開データセットを使う研究、作品史・展示史はまだ十分に網羅していません。

---

# Audio-Visual Research Survey

This repository is a GitHub-ready survey of **audio-visual / audiovisual research and works**. It covers not only machine-learning research across sound and vision, but also artistic lineages such as visual music, video art, live AV, and media installation.

The currently included research papers range from **2016 to 2025**. No year filter was applied during search, but broad English queries such as `audio-visual learning` and `audiovisual datasets` strongly surfaced post-deep-learning machine-learning papers. The artworks section was added to correct that bias.

The taxonomy was not fixed in advance. It was built from broad searches and refined around recurring tasks, datasets, venues, and artwork forms found in surveys, primary papers, official dataset pages, project pages, artist pages, museum pages, and exhibition-related sources.

## Scope

On the research side, the survey treats video, waveforms, spectrograms, speech, music, events, and language as synchronized or weakly aligned multimodal signals. The main fields are computer vision, machine learning, speech/audio, multimedia, and NLP.

On the artwork side, sound and image are treated not as inputs to classify, but as media for perception, body, space, time, and social meaning. This includes visual music, video art, live cinema, VJing, stage work, installation, and AI/data art.

## Emergent Categories

| Category | Typical input and output | Representative examples |
|---|---|---|
| Correspondence and representation learning | video + audio -> shared or self-supervised representation | SoundNet, Look Listen and Learn, AV-HuBERT |
| Sound source and event localization | video + audio -> spatial/temporal event location | AVE, Objects that Sound |
| Source separation and enhancement | mixed audio + video -> separated or enhanced audio | The Sound of Pixels, Looking to Listen |
| AV speech and lip reading | face/video + audio -> text or separated speech | GRID, LRW, LRS2, LRS3, AVSpeech |
| Event recognition and scene understanding | video + audio -> class labels or events | AudioSet, VGGSound, AVE |
| Audio-visual segmentation | video + audio -> pixel masks of sounding objects | AVSBench |
| QA and dialogue | video + audio + text -> answer or response | MUSIC-AVQA, AVSD |
| Generation and synchronization | condition -> generated audio/video or sync score | talking-face, Foley, video-to-audio |
| Audiovisual artworks | sound + image + space + body -> experience, exhibition, live work | Fischinger, Paik, Dumb Type, Ikeda |

## Major Venues

The most frequent venues in the collected papers are:

- Computer vision and ML: CVPR, ICCV, ECCV, NeurIPS, ICML, ICLR, TPAMI
- Multimedia, speech, and audio: ACM Multimedia, ICASSP, INTERSPEECH, WASPAA, DCASE Workshop
- Language, dialogue, and human-centered multimodal work: ACL, EMNLP, NAACL, ICMI

## Key Starting Points

- **Deep Audio-Visual Learning: A Survey**: a 2020 entry point covering separation/localization, correspondence, generation, and representation learning.
- **From Waveforms to Pixels**: a recent survey focused on audio-visual segmentation.
- **SoundNet**: audio representation learning from unlabeled video using visual models as teachers.
- **Look, Listen and Learn**: a representative paper using audio-visual correspondence as self-supervision.
- **AudioSet / VGGSound**: foundational datasets for large-scale audio and AV event recognition.
- **AVE / AVSBench**: representative benchmarks for AV event localization and AV segmentation.
- **Visual music / video art / live audiovisual performance**: artistic lineages including Oskar Fischinger, Mary Ellen Bute, Nam June Paik, Dumb Type, Bill Viola, and Ryoji Ikeda.

## Reading Pages

- [Survey Map](papers/survey-map.md): field taxonomy, cross-cutting axes, and recommended reading order.
- [Correspondence and Representation Learning](papers/representation-learning.md): SoundNet, Look Listen and Learn, AV-HuBERT, and related work.
- [Localization and Separation](papers/localization-and-separation.md): AVE, Sound of Pixels, Objects that Sound, Looking to Listen, and related work.
- [Speech and Lip Reading](papers/speech-and-lip-reading.md): GRID, LRW, LRS2/LRS3, AVSpeech, AV-HuBERT, and related work.
- [Event Understanding and Segmentation](papers/event-understanding-and-segmentation.md): AudioSet, VGGSound, AVE, AVSBench, and related work.
- [QA, Dialogue, and Generation](papers/qa-dialogue-and-generation.md): MUSIC-AVQA, AVSD, talking-face, Foley generation, and related work.
- [Audiovisual Works](papers/audiovisual-works.md): visual music, video art, live AV, and media installation.
## Repository Structure

```text
README.md
references.bib
data/
  papers.yaml
  datasets.yaml
  venues.yaml
  artworks.yaml
papers/
  survey-map.md
  representation-learning.md
  localization-and-separation.md
  speech-and-lip-reading.md
  event-understanding-and-segmentation.md
  qa-dialogue-and-generation.md
  audiovisual-works.md
audit-report.md
```

## Why YAML Files Exist

The `data/*.yaml` files store papers, datasets, venues, and artworks as reusable structured data. Markdown files are for reading; YAML files are for processing and reuse.

YAML makes it easier to generate paper tables, filter papers by category, list dataset tasks, check missing BibTeX keys or URLs, and later build a website or search interface.

## GitHub Pages Setup

This repository includes `index.md` and `_config.yml` so it can be viewed as a Markdown site with GitHub Pages. To publish it, configure the repository on GitHub as follows.

1. Open **Settings** on the GitHub repository page.
2. Open **Pages** from the left menu.
3. Set **Build and deployment** Source to **Deploy from a branch**.
4. Set Branch to `main` and folder to `/ (root)`.
5. Save the setting.

After that, the GitHub Pages URL will use `index.md` as the entry point and link to the Markdown pages.
## Source Policy

Primary papers, official project pages, arXiv, OpenReview, ACL Anthology, IEEE, ACM, official dataset pages, artist pages, and museum pages were preferred. Unverified details are marked `Unknown` rather than guessed.

## Limitations

This is a first-pass public survey. It does not yet comprehensively cover very recent 2025-2026 work, non-English publications, robotics-oriented AV research, commercial or non-public datasets, or the full history of audiovisual works and exhibitions.


