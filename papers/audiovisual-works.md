# オーディオビジュアル作品サーベイ / Audiovisual Works Survey

## なぜ作品も別に扱うのか / Why Works Need a Separate Axis

研究論文でいう Audio-Visual は、多くの場合、音と映像を入力として扱う機械学習・認識・分離・定位の分野を指します。一方、作品としてのオーディオビジュアルは、音と映像を「分類する対象」ではなく、知覚、身体、空間、時間、社会的意味を作る媒体として扱います。  
In research papers, "audio-visual" often means machine learning tasks that use sound and image as inputs. In artistic practice, audiovisual work treats sound and image not as data to classify, but as media for perception, body, space, time, and social meaning.

このため、本サーベイでは論文とは別に、作品を次の軸で整理します。  
This survey therefore organizes works with a separate set of axes:

- 音と映像の対応関係: 同期、対位法、相互変換、フィードバック、環境化。  
  Audio-image relation: synchronization, counterpoint, translation, feedback, environmentalization.
- 形式: 映画、ライブ、VJ、インスタレーション、舞台、都市空間、AI/data art。  
  Form: film, live performance, VJing, installation, stage work, urban space, AI/data art.
- 鑑賞者の位置: 観客、参加者、移動する身体、データ提供者。  
  Viewer position: audience, participant, moving body, data subject.
- 時間性: 固定された映像、ライブ生成、反復展示、サイトスペシフィックな一回性。  
  Temporality: fixed film, live generation, repeated exhibition, site-specific singularity.

## 歴史的な入口 / Historical Entry Points

### 視覚音楽 / Visual Music

視覚音楽は、音楽の構造、リズム、強度、形式を、色、形、運動、光へ対応させる実践です。Oskar Fischinger の抽象映画や Mary Ellen Bute の Seeing Sound 系列は、音を「見る」ための初期の重要作品として位置づけられます。  
Visual music maps musical structure, rhythm, intensity, and form into color, shape, motion, and light. Oskar Fischinger's abstract films and Mary Ellen Bute's Seeing Sound works are early key examples of making sound visible.

ここでは、現在の機械学習的 AV 研究とは異なり、正解ラベルや評価指標ではなく、音と映像の感覚的・作曲的な対応が中心になります。  
Unlike current ML-based AV research, this lineage centers sensory and compositional correspondence rather than labels or metrics.

### ビデオアートと閉回路 / Video Art and Closed Circuit

Nam June Paik の TV Buddha は、テレビ、カメラ、彫刻、自己観察、時間性を組み合わせる作品です。音は中心ではありませんが、映像メディアを空間的・装置的に扱う点で、オーディオビジュアル作品の理解に欠かせません。  
Nam June Paik's TV Buddha combines television, camera, sculpture, self-observation, and temporality. Sound is not central, but the work is essential for understanding audiovisual media as spatial apparatus.

この系譜では、AV は単なる「音 + 映像」ではなく、装置、展示空間、観客の位置を含む経験として現れます。  
In this lineage, AV is not just "sound plus image"; it includes apparatus, exhibition space, and viewer position.

### 舞台・パフォーマンス / Stage and Performance

Dumb Type の S/N のような作品では、身体、テキスト、音、映像、照明、舞台機構が同期し、ときに衝突します。ここでの AV は、情報提示ではなく、社会的・政治的テーマを身体化するための構成原理です。  
Works such as Dumb Type's S/N synchronize and collide body, text, sound, image, lighting, and stage machinery. Here AV is not information display, but a compositional principle for embodying social and political themes.

### 没入型インスタレーション / Immersive Installation

Bill Viola、Ryoji Ikeda、United Visual Artists などの作品では、スクリーン、音響、光、建築空間、鑑賞者の移動が一体化します。作品は単一の映像ファイルではなく、空間内で時間を経験する環境になります。  
In works by Bill Viola, Ryoji Ikeda, United Visual Artists, and others, screen, sound, light, architecture, and viewer movement are integrated. The work becomes an environment for experiencing time in space, not a single video file.

### データ・AI・生成 / Data, AI, and Generation

Refik Anadol の Machine Hallucinations のような作品では、大量の画像・都市データ・音響データが機械学習で処理され、没入的な映像・音響環境として提示されます。ここでは、研究側の機械学習と作品側の AV が交差します。  
In works such as Refik Anadol's Machine Hallucinations, large image, urban, and audio datasets are processed with machine learning and presented as immersive audiovisual environments. This is where ML research and AV artwork directly intersect.

## 代表作品 / Representative Works

| 作品 | 作家 | 年 | 形式 | 重要性 |
|---|---|---:|---|---|
| An Optical Poem | Oskar Fischinger | 1938 | 抽象映画、視覚音楽 | 音楽構造を抽象映像へ対応させる古典 |
| Seeing Sound series | Mary Ellen Bute | 1934-1953 | 抽象映画、電子的映像 | 女性実験映画作家による初期視覚音楽 |
| TV Buddha | Nam June Paik | 1974 | ビデオインスタレーション | テレビ、自己観察、閉回路の古典 |
| S/N | Dumb Type | 1994 | マルチメディア舞台 | 身体、音、映像、テキストによる批評的 AV |
| The Crossing | Bill Viola | 1996 | ビデオ/サウンドインスタレーション | 大規模映像と音響による没入的時間経験 |
| datamatics | Ryoji Ikeda | 2006- | AV ライブ、データアート | データ、ノイズ、電子音、映像を同期する代表例 |
| spectra | Ryoji Ikeda | 2004- | 光/音響インスタレーション | 都市・場所スケールの音と光 |
| Momentum | United Visual Artists | 2013 | キネティック/光/音響インスタレーション | 光、音、運動で空間を楽器化する作品 |
| Machine Hallucinations | Refik Anadol | 2019- | AI/data art、没入型展示 | 機械学習と AV 作品制作の交差点 |

構造化データは [../data/artworks.yaml](../data/artworks.yaml) にあります。  
Structured metadata is available in [../data/artworks.yaml](../data/artworks.yaml).

## 論文サーベイとの接続 / Connection to the Paper Survey

論文側の AV 研究は、主に「モデルが音と映像をどう学習するか」を問います。作品側の AV は、「人が音と映像をどう経験するか」「音と映像がどんな空間や社会的意味を作るか」を問います。  
The paper survey mainly asks how models learn from audio and vision. The works survey asks how humans experience sound and image, and what spatial or social meaning sound and image produce.

この二つは分離しているように見えますが、近年は AI/data art、生成モデル、リアルタイム映像生成、インタラクティブ展示によって接点が増えています。  
These two lineages may look separate, but AI/data art, generative models, real-time visuals, and interactive installations increasingly connect them.

## 今後追加すべき作品群 / Works to Add Later

- Visual music: Walter Ruttmann, Hans Richter, Viking Eggeling, Len Lye, Norman McLaren, Jordan Belson, John Whitney.
- Expanded cinema / live cinema: Gene Youngblood 周辺、live cinema、VJ culture。
- 日本のメディアアート: Dumb Type、坂本龍一 + 高谷史郎、YCAM 関連作品。
- 現代の AV ライブ: Alva Noto, Carsten Nicolai, NONOTAK, 404.zero など。
- 没入型・都市型作品: teamLab、United Visual Artists、Ryoji Ikeda、Refik Anadol。
