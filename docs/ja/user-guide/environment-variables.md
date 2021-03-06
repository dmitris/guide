---
layout: main
title: 環境変数
category: User Guide
menu: menu_ja
toc:
- title: 環境変数
  url: "#環境変数"
  active: 'true'
- title: ビルド固有
  url: "#ビルド固有"
- title: ディレクトリ
  url: "#ディレクトリ"
- title: 環境変数
  url: "#環境変数_1"
- title: ソースコード
  url: "#ソースコード"
- title: URLs
  url: "#urls"
- title: 継続的インテグレーション
  url: "#継続的インテグレーション"
---

# 環境変数

Screwdriverはビルドの過程で利用できる環境変数をエクスポートしています。

*メモ: 1つのジョブに対して設定した環境変数は他のジョブでは参照できません。ジョブ間で値を渡すには、[metadata](./configuration/metadata)を利用してください。*

## ビルド固有

Name | Value
--- | ---
SD_PIPELINE_ID | パイプラインのID
SD_JOB_NAME | ジョブの名前 (例: main)
SD_BUILD_ID | ビルド番号 (例: 1, 2, など)
SD_PULL_REQUEST | プルリクエスト番号 (プルリクエストでない場合は空)
SD_TOKEN | ビルド用のJWTトークン

## ディレクトリ

Name | Value
--- | ---
SD_SOURCE_DIR | チェックアウトされたコードのディレクトリ
SD_ARTIFACTS_DIR | ビルド･生成されたファイルのディレクトリ

## 環境変数

Name | Value
--- | ---
<environment_variable> | [screwdriver.yaml](configuration/)の"environment"の項目で設定された環境変数

## ソースコード

Name | Value
--- | ---
SCM_URL | チェックアウトされたSCMのURL

## URLs

Name | Value
--- | ---
SD_API_URL | Screwdriver APIのURLへのリンク
SD_STORE_URL | Screwdriver StoreのURLへのリンク

## 継続的インテグレーション

Name | Value
--- | ---
SCREWDRIVER | `true`
CI | `true`
CONTINUOUS_INTEGRATION | `true`
