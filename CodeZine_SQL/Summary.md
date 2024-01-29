### 3 値論理と NULL

- 3 値論理とは、真(true)、偽(false)、不明(unknown)の 3 つの値を持つ論理。
- NULL には、値が不明であること（未知）を表す意味と、値が存在しないこと（適用不能）を表す意味の 2 つがある。
- NULL との比較演算は、常に不明(UNKNOWN)になるため、NULL の判定は、IS NULL または IS NOT NULL を使用する。
- 真偽値における unknown と NULL の一種の UNKNOWN とは異なる。
  - unknown と unknown の比較は TRUE になるが、UNKNOWN と UNKNOWN の比較は unknown になる。
    - unknown は状態を表すものであり、True、False と同レベルのもの。
- 排中律（排中律）：ある命題が真であるか偽であるかのいずれかであること。
  - 3 値論理では、排中律が成り立たない。
  - 3 値論理では、真でも偽でもない不明な状態が存在するため、排中律が成り立たない。
- CASE 式において、WHEN 句 に NULL を指定しても、NULL との比較は不明になるため、THEN で指定した値はセットされず、ELSE 句 が実行される。
  - ELSE 句 がない場合は、NULL が返される。
- NOT IN と NOT EXISTS は NULL を含む場合に注意が必要。
  - NOT IN は、NULL を含む場合、NULL との比較は不明になるため、NULL が返される。
  - NOT EXISTS は、NULL を含む場合、NULL との比較は不明になるため、NULL が返されるが、NULL は偽として扱われるため、NOT EXISTS は常に真になる。
- Null を防ぐためには
  - テーブル定義に NOT NULL 制約を付与する。
- Oracle の NULL と 空文字 に関するローカルルール
  - 原則として、NULL と空文字は同じものとして扱う。
  - 文字連結の時だけは NULL を空文字として扱う。
  - 文字連結で両方 NULL の場合は NULL を返す。
    `「Oracle は、 長 さが 0（ ゼロ） の 文字列 を NULL として 処理 し ます が、 長 さが 0（ ゼロ） の 文字列 を 別 の オペランド と 連結 する と、 その 結果 は 常に もう 一方 の オペランド になり ます。 結果 が NULL に なる のは、 2 つ の NULL 文字列 を 連結 し た とき のみ です。 ただし、 この 処理 は Oracle Database の 今後 の バージョン でも 継続 さ れる とは かぎり ませ ん。」

ミック. 達人に学ぶ SQL 徹底指南書 第 2 版 初級者で終わりたくないあなたへ (p.144). 株式会社翔泳社. Kindle 版. `

- NULL を扱うための特別な関数
  - COALESCE: NULLw を指定した値に置き換える。
  - NULLIF: 特定の条件に合致した場合に NULL を返す。

### EXISTS 述語 の 使い方
