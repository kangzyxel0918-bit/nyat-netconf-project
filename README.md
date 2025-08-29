
# NYAT — NETCONF YANG Automation Testing (Consolidated)

包含：
- **IETF System** 端到端測試（edit-config / get-config / get / merge / remove / recreate / delete）
- **IETF ACL** 端到端測試（含合併、移除、刪除 ACL 以及 get/get-config 驗證）
- Allure 報告（自動附加 NETCONF Request/Reply）
- 連線設定：`192.168.169.58:830` / `admin` / `1234`（可在 `config/config.yaml` 調整）

## 安裝與執行
```bash
python -m venv venv
# Windows: venv\Scripts\activate
# macOS/Linux: source venv/bin/activate
pip install -r requirements.txt
pytest -q --alluredir=./allure-results
# 若需圖形化報告：
# allure serve ./allure-results
```
