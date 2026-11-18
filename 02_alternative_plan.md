# 02 HOLD理由 → 代わりの案（Gemini）

**入力**：`samples/gate_check_hold.json` と `samples/business_data.json`

```
AIDE ARK GATE が次の理由で配車を HOLD（保留）しました。
業務データの範囲内で、実行可能な代わりの案を最大3つ、JSONで提案してください。

ルール：
- 契約の範囲内・空き枠のある選択肢を優先し、おすすめを1つ示してください。
- 各案に、承認が必要な人（権限データにある役割）を書いてください。
- 案は提案です。実行してはいけません。"executes": false を含めてください。
- 採用された案は、AIDE ARK GATE が再照合してから実行されます。

[HOLDの理由]
（gate_check_hold.json の内容を貼る）

[業務データ]
（business_data.json の内容を貼る）
```

**出力例**：`samples/gemini_alternatives.json`
