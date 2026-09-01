# Laysi One 法規更新來源

修法後的費率、級距與上限，供已安裝的 Laysi One 自行取用。系統管理員在
「法規版本」按「檢查法規更新」，安裝端會讀取本儲存庫的 `manifest.json`，
寫入該資料庫尚未收過的版本。

一則修法只送一次。已經收過的版本，以及管理員手動刪除的版本，都不會再寫入。

## manifest.json

```json
{
  "updates": [
    {
      "file": "2026-01-01_vat.sql",
      "domain": "vat",
      "version": "2026.1",
      "effective_from": "2026-01-01",
      "effective_to": null,
      "source_note": "加值型及非加值型營業稅法第 10 條",
      "payload": { "rate": "0.05" }
    }
  ]
}
```

`file` 是安裝端記住的識別字，發布之後不再更動。

本檔由 `Laysi/laysi-one` 的 `regulation-feed` 工作流程產生，請勿手動編輯。
