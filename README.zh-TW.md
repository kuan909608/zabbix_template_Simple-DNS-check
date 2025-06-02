[English](README.md) | [繁體中文](README.zh-TW.md)

# Zabbix 模板 - 簡易 DNS 檢查

此專案提供一個用於 Zabbix 的 YAML 模板，透過外部檢查的方式監控 DNS 查詢的可用性與回應時間，適用於簡單的 DNS 健康監控情境。

## 功能

- 檢查 DNS 查詢是否成功（回傳結果）
- 測量 DNS 回應所需時間
- 觸發 DNS 查詢失敗或超時警報
- 相容於 Zabbix 6.0 LTS 或更新版本

## 匯入方式

1. 登入 Zabbix Web Console。
2. 前往 `設定` > `模板`。
3. 點擊右上角的 `匯入`。
4. 選擇 `zabbix_template_simple-dns-check.yaml` 檔案。
5. 勾選需要的選項，點選 `匯入`。

## 使用說明

1. 將模板套用到指定主機。
2. 確保主機能使用 `dig` 或 `nslookup` 指令。
3. 根據需求修改 Item 中的 DNS 查詢參數（例如要查的網域）。
4. 可依據環境需求新增/調整觸發條件與圖表。

## 注意事項

- 請確保 Zabbix Server 或 Proxy 有設定好 `ExternalScripts` 目錄。
- 執行 DNS 查詢的工具需安裝於該主機上（建議使用 `dig`）。
- 若為內部 DNS，可自訂查詢目標 IP。

## 授權

本專案以 MIT License 授權，歡迎自由修改與使用。
