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
