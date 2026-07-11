# 監査レポート

## 日付

2026-07-12 JST

## 確認したこと

- 広い検索語と、検索中に繰り返し現れた語を使って調査を広げたこと。
- 代表論文とデータセットについて、一次情報または一次情報に近いページを優先したこと。
- 各論文エントリに URL、タスクカテゴリ、入力、出力、データセット、手法タグ、貢献、限界、BibTeX キーがあること。
- データセット項目で、確認済みの事実と `Unknown` を区別したこと。
- 分類が、事前に固定したリストではなく、調査で現れたタスク群に基づいていること。
- 作品サーベイを追加し、論文中心・機械学習中心の偏りを明示したこと。

## 残課題

- このサーベイは初版です。2024-2026 年の AV foundation model、動画からの音生成、拡散モデルによる Foley 生成、音を扱う大規模マルチモーダルモデルの論文は不足している可能性があります。
- AVE、MUSIC、LRS2、LRS3、LRW、GRID、VoxCeleb、AVSBench、MUSIC-AVQA、AVSD の正確なデータ件数は完全には監査していません。
- 一部の BibTeX は、ページ番号、publisher、DOI、正式な proceedings 情報を追加する余地があります。
- 2025 年の AV セグメンテーションサーベイは arXiv preprint として含めています。査読済み文献として引用する前に出版状況を確認する必要があります。
- 作品サーベイは追加したばかりで、視覚音楽、ビデオアート、VJ、ライブシネマ、メディアアート史をまだ網羅していません。

## 重要だが未追加の可能性がある研究系列

- アクティブ話者検出と AV diarization。
- AV navigation と embodied agents。
- AV 感情認識・センチメント分析。
- AV 異常検知。
- AV 検索と cross-modal indexing。
- Foley / video-to-audio 生成と同期評価。
- 音、映像、言語を同時に扱う汎用マルチモーダルエンコーダ。
- オーディオビジュアル作品史: visual music、expanded cinema、live cinema、VJ culture、日本のメディアアート。

## バイアス監査

現在の論文サーベイは、発見されたアンカー論文が CVPR、ICCV、ECCV、ACM Multimedia、NeurIPS、ICASSP に多かったため、コンピュータビジョン・マルチメディア・機械学習寄りです。作品サーベイを追加しましたが、まだ網羅的な美術史・メディアアート史の調査にはなっていません。

## リンク監査

リンクは、公式ページ、プロジェクトページ、proceedings、arXiv、リポジトリページ、作家ページ、美術館ページから選びました。公開前には、自動リンクチェッカーを追加するのが望ましいです。

## 分類監査

分類は、調査中に繰り返し現れたタスク群から作りました。対応学習、定位・分離、音声・読唇、イベント認識・セグメンテーション、QA・対話・生成、作品系譜は互いに重なります。そのため YAML では複数カテゴリを許容しています。

## 次の作業

1. 2020-2026 年の論文を、トピックごとに 20-40 件追加する。
2. 公式論文から正確なデータセット統計を追加する。
3. YAML 検証とリンクチェック用の CI を追加する。
4. YAML から README の表を生成する `scripts/` を追加する。
5. active speaker detection、AV retrieval、embodied AV navigation、affect、generation の個別ページを追加する。
6. 作品サーベイについて、一次資料、展覧会カタログ、美術館ページ、作家公式ページから作品情報を増やす。

---

# Audit Report

## Date

2026-07-12 JST

## What Was Checked

- Broad discovery from survey-like queries and recurring terms.
- Primary or near-primary pages were preferred for representative papers and datasets.
- Each structured paper entry includes URL, task categories, inputs, outputs, datasets, method tags, contribution, limitations, and BibTeX key.
- Dataset entries distinguish confirmed facts from `Unknown` details.
- The taxonomy follows discovered task clusters rather than a pre-fixed category list.
- The artworks survey was added to make the paper-centered and ML-centered bias explicit.

## Known Gaps

- This is a first-pass survey and may miss recent 2024-2026 work on AV foundation models, video-to-audio generation, diffusion-based Foley generation, and audio-capable large multimodal models.
- Exact dataset counts were not fully audited for AVE, MUSIC, LRS2, LRS3, LRW, GRID, VoxCeleb, AVSBench, MUSIC-AVQA, and AVSD.
- Some BibTeX entries may need page numbers, publisher fields, DOI, or official proceedings formatting.
- The 2025 AV segmentation survey is included as an arXiv preprint; publication status should be verified before citing it as peer-reviewed.
- The works survey was newly added and is not yet comprehensive across visual music, video art, VJing, live cinema, and media art history.

## Potentially Missing Important Lines

- Active speaker detection and audio-visual diarization.
- Audio-visual navigation and embodied agents.
- Audio-visual emotion recognition and sentiment analysis.
- Audio-visual anomaly detection.
- Audio-visual retrieval and cross-modal indexing.
- Foley/video-to-audio generation and synchronization metrics.
- Universal multimodal encoders that include audio, vision, and language.
- Audiovisual artwork history: visual music, expanded cinema, live cinema, VJ culture, and Japanese media art.

## Bias Audit

The current paper survey is biased toward computer vision, multimedia, and machine learning because many discovered anchor papers came from CVPR, ICCV, ECCV, ACM Multimedia, NeurIPS, and ICASSP. The artworks survey has been added, but it is not yet a comprehensive art-historical or media-art-historical survey.

## Link Audit

Links were selected from official pages, project pages, proceedings, arXiv, repositories, artist pages, and museum pages. An automated link checker should be added before publication.

## Classification Audit

The taxonomy was derived from recurring task clusters. Correspondence learning, localization/separation, speech/lip reading, event recognition/segmentation, QA/dialogue/generation, and artwork lineages overlap. YAML therefore allows multiple categories.

## Next Actions

1. Add 20-40 more papers from 2020-2026 using targeted searches per topic.
2. Add exact dataset statistics with citations from official papers.
3. Add CI for YAML validation and link checking.
4. Add scripts for generating README tables from YAML.
5. Add topic pages for active speaker detection, AV retrieval, embodied AV navigation, affect, and generation.
6. Expand the works survey from primary materials, exhibition catalogues, museum pages, and artist/project pages.
