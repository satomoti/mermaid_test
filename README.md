# 課題
Mermaidを触ってみよう

マークダウンファイルを編集して、Mermaidで図を描いてみよう

# 取り組み方
* 本プロジェクトをforkしてください。
* README.mdを編集して、Mermaidを使いこなしてください
* できたらプルリクエストを出します

# 課題項目
## 流れ図
### 条件
- 開始と終了ノードをつける
- 条件分岐を組み込む
- 5ノード以上
- カッコいいほど高得点

## 解答
```mermaid
flowchart LR;
  A([開始]) --> B[/入力/];
  B -->C{判断};
  B -- キャンセル --> G([終了]);
  C -- 真 --> D[[プログラム実行]];
  D --> E[[結果表示]];
  E --> B;
  C -- 偽 --> F[[エラー表示]];
  F --> G;
```

## シーケンス図
### 条件
- 3人以上
- メッセージをやり取りしない人がいないように
- 自己呼び出しを含むこと
- カッコいいほど高得点

## 解答
```mermaid
sequenceDiagram
    actor M
    actor U
    actor K
    M ->> U: おはよう！
    activate U
    U -->> M: おはよお～
    activate K
    K ->> U: おはようございまーす！
    U -->> K: おはよお～
    M ->> K: おはよう！
    K -->> K: おはようございまーす！
    deactivate U
    deactivate K
    M ->> U: Uちゃん、最近何やった？俺、鬼退治！
    deactivate M
    activate U
    U -->> M: 僕はカメさんに乗って釣りしてたよ～
    deactivate U
    activate M
    M ->> K: Kちゃんは最近何やった？
    deactivate M
    activate K
    K -->> M: 山の動物たちと相撲してた！
    deactivate K
```

## クラス図

### 条件
- 3つ以上
- 汎化と集約を含むこと
- カッコいいほど高得点

## 解答
```mermaid
classDiagram
    サトモチ o-- アイテム
    サトモチ :人間
    サトモチ :１０～２０代
    アイテム :筆箱
    アイテム :眼鏡
    筆箱 *-- 筆記用具
    筆記用具 :鉛筆
    筆記用具 :消しゴム
    筆記用具 :シャープペンシル
    サトモチ--|>所属
    所属:大学
```
