# 監査レポート / Audit Report

## 日付 / Date

2026-07-12 JST

## 確認したこと / What Was Checked

- 広い検索語と、検索中に繰り返し現れた語を使って調査を広げたこと。  
  Broad discovery from survey-like queries and recurring terms.
- 代表論文とデータセットについて、一次情報または一次情報に近いページを優先したこと。  
  Primary or near-primary pages were preferred for representative papers and datasets.
- 各論文エントリに URL、タスクカテゴリ、入力、出力、データセット、手法タグ、貢献、限界、BibTeX キーがあること。  
  Each structured paper entry includes URL, task categories, inputs, outputs, datasets, method tags, contribution, limitations, and BibTeX key.
- データセット項目で、確認済みの事実と `Unknown` を区別したこと。  
  Dataset entries distinguish confirmed facts from `Unknown` details.
- 分類が、事前に固定したリストではなく、調査で現れたタスク群に基づいていること。  
  The taxonomy follows discovered task clusters rather than a pre-fixed category list.

## 残課題 / Known Gaps

- このサーベイは初版です。2024-2026 年の AV foundation model、動画からの音生成、拡散モデルによる Foley 生成、音を扱う大規模マルチモーダルモデルの論文は不足している可能性があります。  
  This is a first-pass survey and may miss recent 2024-2026 work on AV foundation models, video-to-audio generation, diffusion-based Foley generation, and audio-capable large multimodal models.
- AVE、MUSIC、LRS2、LRS3、LRW、GRID、VoxCeleb、AVSBench、MUSIC-AVQA、AVSD の正確なデータ件数は完全には監査していません。`data/datasets.yaml` では `Unknown` または確認メモを残しています。  
  Exact dataset counts were not fully audited for AVE, MUSIC, LRS2, LRS3, LRW, GRID, VoxCeleb, AVSBench, MUSIC-AVQA, and AVSD.
- 一部の BibTeX は、ページ番号、publisher、DOI、正式な proceedings 情報を追加する余地があります。  
  Some BibTeX entries may need page numbers, publisher fields, DOI, or official proceedings formatting.
- 2025 年の AV セグメンテーションサーベイは arXiv preprint として含めています。査読済み文献として引用する前に出版状況を確認する必要があります。  
  The 2025 AV segmentation survey is included as an arXiv preprint; publication status should be verified before citing it as peer-reviewed.
- YouTube 由来データセットではリンク切れや動画削除が大きなリスクです。  
  Link rot and video removal are material risks for YouTube-derived datasets.
- ロボティクス、embodied audio-visual navigation、AV saliency、感情認識、医療・支援技術系の AV 研究は不足しています。  
  Robotics, embodied AV navigation, AV saliency, affective computing, and medical/assistive AV work are underrepresented.
- 非英語文献と日本語の AV 研究は網羅的には検索していません。  
  Non-English literature and Japanese-language AV research were not comprehensively searched.

## 重要だが未追加の可能性がある研究系列 / Potentially Missing Important Lines

- アクティブ話者検出と AV diarization。  
  Active speaker detection and audio-visual diarization.
- AV navigation と embodied agents。  
  Audio-visual navigation and embodied agents.
- AV 感情認識・センチメント分析。CMU-MOSEI 系データセットを含みます。  
  Audio-visual emotion recognition and sentiment analysis, including CMU-MOSEI-style datasets.
- AV 異常検知。  
  Audio-visual anomaly detection.
- AV 検索と cross-modal indexing。  
  Audio-visual retrieval and cross-modal indexing.
- Foley / video-to-audio 生成と同期評価。  
  Foley/video-to-audio generation and synchronization metrics.
- 音、映像、言語を同時に扱う汎用マルチモーダルエンコーダ。  
  Universal multimodal encoders that include audio, vision, and language.

## バイアス監査 / Bias Audit

現在のサーベイは、発見されたアンカー論文が CVPR、ICCV、ECCV、ACM Multimedia、NeurIPS、ICASSP に多かったため、コンピュータビジョン・マルチメディア寄りです。音声・音響系会議も含めていますが、音声特化文献はまだ網羅的ではありません。  
The current survey is biased toward computer vision and multimedia venues because many discovered anchor papers came from CVPR, ICCV, ECCV, ACM Multimedia, NeurIPS, and ICASSP. Speech and audio venues are included, but the speech-specific literature is not exhaustive.

## リンク監査 / Link Audit

リンクは、公式ページ、プロジェクトページ、proceedings、arXiv、リポジトリページから選びました。公開前には、自動リンクチェッカーを追加するのが望ましいです。  
Links were selected from official pages, project pages, proceedings, arXiv, and repository pages. An automated link checker should be added before publication.

## 分類監査 / Classification Audit

分類は、調査中に繰り返し現れた次のタスク群から作りました。  
The taxonomy was derived from recurring task clusters:

- 対応学習・自己教師あり表現。  
  Correspondence and self-supervised representation.
- 定位・分離。  
  Localization and separation.
- 音声・読唇。  
  Speech and lip reading.
- イベント認識・セグメンテーション。  
  Event recognition and segmentation.
- QA・対話・生成。  
  QA, dialogue, and generation.
- 音楽・感情・人間中心応用。  
  Music, affect, and human-centered applications.

これらのカテゴリは重なります。たとえば Looking to Listen は音声と分離の両方、AV-HuBERT は音声と表現学習の両方に属します。そのため YAML では複数の `task_categories` を許容しています。  
These categories overlap. For example, Looking to Listen belongs to both speech and separation, while AV-HuBERT belongs to both speech and representation learning.

## 次の作業 / Next Actions

1. 2020-2026 年の論文を、トピックごとに 20-40 件追加する。  
   Add 20-40 more papers from 2020-2026 using targeted searches per topic.
2. 公式論文から正確なデータセット統計を追加する。  
   Add exact dataset statistics with citations from official papers.
3. YAML 検証とリンクチェック用の CI を追加する。  
   Add CI for YAML validation and link checking.
4. YAML から README の表を生成する `scripts/` を追加する。  
   Add scripts for generating README tables from YAML.
5. active speaker detection、AV retrieval、embodied AV navigation、affect、generation の個別ページを追加する。  
   Add topic pages for active speaker detection, AV retrieval, embodied AV navigation, affect, and generation.
