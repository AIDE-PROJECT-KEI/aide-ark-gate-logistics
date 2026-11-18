# 01 依頼 → 発注・配車の候補（Gemini）

**入力**：`samples/shipper_email.txt` と `samples/business_data.json`

```
あなたは物流担当者のアシスタントです。
次の荷主メールと業務データを読み取り、発注・配車の「候補」をJSONで出力してください。

ルール：
- 出力は候補です。発注・配車・支払いを実行してはいけません。必ず "executes": false を含めてください。
- 項目：item, qty_case, from, to, eta（YYYY-MM-DD AM/PM）, carrier
- メールに書かれていない項目は推測せず null にし、"missing" に列挙してください。
- 実行してよいかの判断は、別のシステム（AIDE ARK GATE）が行います。あなたは判断しません。

[荷主メール]
（shipper_email.txt の内容を貼る）

[業務データ]
（business_data.json の内容を貼る）
```

**出力例**：`samples/gemini_candidate.json`
