# Markdown記述の演習
Markdown記述の演習として使い方をまとめる。

# Markdown（マークダウン）とは
Mardown（マークダウン）とは、「#見出し」など、シンプルな書き方で文書構造を明示でき、装飾されたHTML文書に変換できる軽量マークアップ言語である。

Markdownの基本的な要素としては以下のようなものがある。
- 段落
- 改行
- 見出し
- 引用
- リスト
- コード
- 水平線
- リンク
- 強調
- 画像
- バックスラッシュによるエスケープ

以降、Markdownの基本的な内容についてまとめている。

# 見出し
1～6個のシャープで見出しを記述する。

※シャープと見出し文字の間には半角スペースを1つ入れること

## 記述例
~~~
# 見出し1
## 見出し2
### 見出し3
#### 見出し4
##### 見出し5
###### 見出し6
~~~

## 表示例
# 見出し1
## 見出し2
### 見出し3
#### 見出し4
##### 見出し5
###### 見出し6

# 改行
テキストに挿入された改行は最終的な結果から取り除かれる。これは、画面の大きさに応じて改行を行う処理はWebブラウザが担当すべきであるという設計思想による。強制的に改行したい場合は、行末に2つの半角スペースを挿入すればよい。

# テキストカラー（文字色）
Markdown記法では、テキストカラーの変更は対応していないため、文字色を変更したい場合は、以下のように直接HTMLタグを記述する必要がある。

## 記述例
~~~
これは<span style="color:red; ">赤文字</span>です
~~~

## 表示例
これは<span style="color:red; ">赤文字</span>です

# チェックリスト
行頭に`- []`, `- [x]`を付けるとチェックリストになる。

## 記述例
~~~
- [ ] これからやるタスク
- [x] 完了したタスク
~~~

## 表示例
- [ ] これからやるタスク
- [x] 完了したタスク

# ファイルの挿入
`![代替テキスト](URL)`でファイルが表示される。

## 記述例
~~~
![フクロウ](https://notepm.jp/assets/img/apple-touch-icon-120x120.png)
~~~

## 表示例
![フクロウ](https://notepm.jp/assets/img/apple-touch-icon-120x120.png)

# 注釈
文中に注釈を入れることができる。

## 記述例
~~~
テキスト[^1]
[^1]:注釈の内容
~~~

## 表示例
テキスト[^1]

[^1]:　注釈の内容

# 箇条書きリスト
ハイフン、プラス、アスタリスクのいずれかで箇条書きリストを記述可能。

※ハイフン、プラス、アスタリスクと箇条書きの項目の間には半角スペースを1つ入れること

## 記述例
~~~
- リスト1
    - ネスト　リスト1_1
        - ネスト　リスト1_1_1
        - ネスト　リスト1_1_2
    - ネスト　リスト1_2
- リスト2
- リスト3
~~~

## 表示例
- リスト1
    - ネスト　リスト1_1
        - ネスト　リスト1_1_1
        - ネスト　リスト1_1_2
    - ネスト　リスト1_2
- リスト2
- リスト3

# 番号付きリスト
数値+半角ドットで番号付きリストを記述可能。

番号の内容は何でもいい。実際に表示される際に適切な番号で表示される。

そのため、一般的にはすべて１．内容で記載すると変更に強く楽である。

※数値+半角ドットと箇条書きの項目の間には半角スペースを1つ入れること

## 記述例
~~~
1. 番号付きリスト1
    1. 番号付きリスト1_1
    1. 番号付きリスト1_2
1. 番号付きリスト2
1. 番号付きリスト3
~~~

## 表示例
1. 番号付きリスト1
    1. 番号付きリスト1_1
    1. 番号付きリスト1_2
1. 番号付きリスト2
1. 番号付きリスト3

# 引用
「>」を入れることで引用を表現できる。

## 記述例
~~~
> お世話になります。xxxです。
> 
> ご連絡いただいた、バグの件ですが、仕様です。
~~~

## 表示例
> お世話になります。xxxです。
> 
> ご連絡いただいた、バグの件ですが、仕様です。

# 二重引用
「>>」を入れることで二重引用を表現できる。

## 記述例
~~~
> お世話になります。xxxです。
> 
> ご連絡いただいた、バグの件ですが、仕様です。
>> お世話になります。yyyです。
>>
>> あの新機能バグってるっすね
~~~

## 表示例
> お世話になります。xxxです。
> 
> ご連絡いただいた、バグの件ですが、仕様です。
>> お世話になります。yyyです。
>>
>> あの新機能バグってるっすね

# pre記法（スペース4 or タブ）
半角スペース4個もしくはタブで、コードブロックをpre表示できる

## 記述例
~~~
# Tab
class Hoge
    def hoge
            print 'hoge'
        end
    end

---

    # Space
    class Hoge
       def hoge
            print 'hoge'
        end
    end
~~~

## 表示例
    # Tab
    class Hoge
        def hoge
            print 'hoge'
        end
    end

---

    # Space
    class Hoge
       def hoge
            print 'hoge'
        end
    end

# code記法
バッククォートで文字列を囲むことでコードの一部を表示可能にする

## 記述例
~~~
インストールコマンドは`gem install hoge`です
~~~

## 表示例
インストールコマンドは`gem install hoge`です

# 強調：em
アスタリスクもしくはアンダースコア1個で文字列を囲むことで強調する。

見た目は斜体になる。

## 記述例
~~~
normal *italic* normal
normal _italic_ normal
~~~

## 表示例
normal *italic* normal

normal _italic_ normal

# 強調：strong
アスタリスクもしくはアンダースコア2個で文字列を囲むことで強調する。

見た目は太字になる。

## 記述例
~~~
normal **bold** normal
normal __bold__ normal
~~~
## 表示例
normal **bold** normal

normal __bold__ normal

# 強調：em+strong
アスタリスクもしくはアンダースコア3個で文字列を囲むことでemとstrongによる強調を両方適用する。

見た目は斜体かつ太字になる。

## 記述例
~~~
normal ***bold*** normal
normal ___bold___ normal
~~~
## 表示例
normal ***bold*** normal

normal ___bold___ normal

# 水平線
アンダースコア、アスタリスク、ハイフンなどを3つ以上連続して記述することで水平線を表示する。

※連続するハイフンなどの間にはスペースがあっても良い

## 記述例
~~~
***
___
---
* * *
~~~

## 表示例
***
___
---
* * *

# リンク
[表示文字](リンクURL)形式でリンクを記述できる

## 記述例
~~~
[Google先生](https://www.google.co.jp/)
~~~

## 表示例
[Google先生](https://www.google.co.jp/)

# 定義参照リンク
Markdownの文書の途中に長いリンクを記述したくない場合は、同じリンクの参照を何度も利用する場合は、リンク先への参照を定義することができる。

## 記述例
~~~
[こっちからgoogle][google]
その他の文章
[こっちからもgoogle][google]
[google]:https://www.google.co.jp/
~~~

## 表示例
[こっちからgoogle][google]
その他の文章
[こっちからもgoogle][google]

[google]:https://www.google.co.jp/

# GitHub Flavored Markdown(GFM)
GitHub Flavored Markdown(GFM)はGitHubの独自仕様を加えたMarkdown記法である。

以降、GFMと記載する。

# GFM:リンクテキスト簡易記法
URLは記述するだけで自動的にリンクになる。

## 記述例
~~~
https://www.google.co.jp/
~~~

## 表示例
https://www.google.co.jp/

# GFM:取り消し線
チルダ2個で文字列を囲むことで取り消し線を利用できる。

## 記述例
~~~
~~取り消し線~~
~~~

## 表示例
~~取り消し線~~
# GFM:pre記法（チルダ×3）
## 記述例
~~~
    ~~~
    class Hoge
        def hoge
            print 'hoge'
        end
    end
    ~~~
~~~

## 表示例
~~~
    class Hoge
        def hoge
            print 'hoge'
        end
    end
~~~

# GFM:pre記法（バッククォート×3）

## 記述例
~~~
    ```
    class Hoge
        def hoge
            print 'hoge'
        end
    end
    ```
~~~

## 表示例
```
class Hoge
    def hoge
        print 'hoge'
    end
end
```

# GFM:pre記法（シンタックスハイライト）
チルダ、もしくはバッククォート3つの後ろに対象シンタックスの言語名を記述する。

## 記述例
~~~
    ~~~ruby
    class Hoge
        def hoge
            print 'hoge'
        end
    end
    ~~~
~~~

## 表示例
~~~ruby
class Hoge
    def hoge
        print 'hoge'
    end
end
~~~

# GFM:表組み

## 記述例
~~~
|header1|header2|header3|
|:--|--:|:--:|
|align left|align right|align center|
|a|b|c|
~~~

## 表示例
|header1|header2|header3|
|:--|--:|:--:|
|align left|align right|align center|
|a|b|c|

# GFM:ページ内リンク
GitHubのMarkdownを利用すると、見出し記法を利用した際にアンカーが自動的に作成される。

そのアンカーを利用したページ内リンクを簡単に作成できる。

## 記述例
~~~
## menu
* [to header1](#header1)
* [to header2](#header2)

<!-- some long code -->

[return to menu](#menu)
### header1
### header2
~~~

以下のHTMLになる。
~~~html
<h2><a name="user-content-menu" href="#menu">menu</a></h2>
<a href="#header1">to header1</a>
<a href="#header2">to header2</a>

<!-- some long code -->

<a href="#menu">to menu</a>
<h3><a name="user-content-header1" href="#header1">header1</a></h3>
<h3><a name="user-content-header2" href="#header2">header2</a></h3>
~~~

# バックスラッシュによるエスケープ
Markdownが書式化コマンドとして解釈する文字は、バックスラッシュを加えることによって、その文字そのものとして解釈させることができる。

## 記述例
~~~
\*
~~~

## 表示例
\*

# 参考リンク
参考リンクについて以下に示す
- [Markdown記法/書き方（見出し・表・リンク・画像・文字色など）](https://notepm.jp/help/how-to-markdown)
- [Markdown記法 サンプル集](https://qiita.com/tbpgr/items/989c6badefff69377da7)
