# Mitakihara Records Platform

見滝原市を参照自治体とする、自治体向け「事業型公文書管理基盤」の参照実装です。

> **Status:** Initial repository preparation / pre-Codex handoff

## Purpose

本プロジェクトは、自治体が保有・管理するオープンデータ、公文書、地理空間情報、文化資料、観測記録、劣化・旧媒体等を分断せず、行政活動との関係を保ちながら管理・検索・保存・公開するための基盤を検討・実装します。

主分類は組織図ではなく、次の連続した行政活動を軸とします。

**行政機能 → 政策 → 施策 → 事業 → 案件 → 情報資源**

組織は主分類そのものではなく、担当・管理・検索条件・履歴等として扱います。

## Design baseline

後継開発では Version 5 の画面構成・操作仕様・VIを参照しつつ、以下を独立した履歴モデルとして扱います。

- 情報資源と複数の表現物・ファイル・物理媒体
- 行政主体、担当組織、権利主体、保有主体、管理主体、公開主体等
- 権利、公開範囲、再利用条件
- 作成・取得・移管・変換・補正・公開・訂正・復元等の来歴
- 地理空間・時間情報
- 人／機械それぞれの判読可能性
- 保存状態・復元・長期保存
- AIによる入力支援と人による確定・監査

## CKAN positioning

CKANは必須条件ではありません。採用する場合も中核データモデルそのものではなく、公開カタログ／検索入口として利用し、中核モデルとはAPIまたは同期処理で連携する方針です。

## Planned repository structure

```text
docs/                 Design, architecture, standards and handoff documents
assets/brand/         Mitakihara VI, emblem/logo masters and color specifications
prototype/            Version 5 reference/prototype assets
src/                  Successor implementation
tests/                Acceptance and regression tests
.github/              CI and contribution workflows
```

ディレクトリは必要な成果物を配置する段階で作成します。空ディレクトリ維持のためのダミーファイルは原則置きません。

## Development phases

1. 語彙・識別子・コード体系
2. 中核カタログ
3. GISビューア
4. 保存管理
5. 公開連携
6. 都市OS連携

## Current preparation tasks

- [x] GitHub repository initialized
- [x] Project purpose and design baseline documented
- [x] CKAN positioning documented
- [ ] Rename repository from `mitakihara-records-platform-` to `mitakihara-records-platform`
- [ ] Import approved Version 5 design documentation
- [ ] Import Mitakihara VI / Web Guidelines and approved brand masters
- [ ] Define detailed architecture and implementation boundary
- [ ] Establish CI and acceptance tests

## Important

見滝原市・神浜県およびデモ環境の行政情報・案件・所在地等は架空設定です。実在する自治体の内部情報を示すものではありません。

実装開始前に、設計資料・VI資産・Version 5参照実装を正式な基準資料として固定します。
