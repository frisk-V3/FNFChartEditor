# FNF Psych Engine Chart Editor (Web Version / 1-File Edition)

ブラウザだけで動く **FNF Psych Engine 用 譜面エディタ** です。  
1つの HTML ファイルだけで完結しており、ローカルで開くだけで使用できます。

-  オーディオ読み込み  
-  4レーン譜面編集  
-  ノーツ追加 / 削除 / 選択  
-  BPM に基づくビートライン  
-  Psych Engine 形式の JSON 出力  
-  JSON 読み込み（セクション自動復元）  
-  再生しながら譜面確認  

---

## 🚀 使い方

### 1. ファイルを開く
`editor.html` をブラウザで開くだけで起動します。

### 2. 曲を読み込む
サイドバーの **Audio File** から音楽ファイルを選択。

### 3. ノーツを置く
- キャンバスをクリック → ノーツ追加  
- レーンはクリック位置で自動判定  
- 長押しは「Hold Length(ms)」で設定  
- ノーツをクリック → 選択  
- Delete ボタンで削除  

### 4. 再生しながら確認
- ▶ 再生  
- ⏸ 一時停止  
- ⏹ 停止  
- タイムラインスライダーで移動  

### 5. JSON 出力
`JSON ダウンロード` を押すと  
**Psych Engine 互換 JSON** が生成されます。

### 6. JSON 読み込み
`JSON 読込` → `.json` を選択すると  
セクション構造を自動復元して読み込みます。

---

## 📁 JSON 形式（出力例）

```json
{
  "song": {
    "song": "TestSong",
    "bpm": 150,
    "notes": [
      {
        "sectionNotes": [
          [500, 0, 0],
          [750, 1, 0],
          [1000, 2, 150]
        ],
        "mustHitSection": true
      }
    ]
  }
}
