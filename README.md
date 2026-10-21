# 二十四史の医療の記事 原文・現代語訳

中国の正史（二十四史，『史記』〜『明史』）から医療に関わる記事を集め，句読点つきの原文と日本語訳・解説を付けたもの。

- (1) **医師列伝集**：方技伝・方術伝・芸術伝など18巻のうち，医療と関係のある人の伝（占い・呪術・仙薬・養生など，医療との境が曖昧な人も含む）。
- (2) **医療・疾病・薬物に関連する引用集**：(1) 以外の本紀・列伝などのうち，病気・治療・薬物に関わる箇所。

ウェブで読む：https://medicalcloud.github.io/24shi/ （目次は `index.md`）

## この資料について

### 二十四史とは

二十四史は，中国の24の正史をまとめた呼び名である。

> 史記・漢書・後漢書・三国志・晋書・宋書・南斉書・梁書・陳書・魏書・北斉書・周書・隋書・南史・北史・旧唐書・新唐書・旧五代史・新五代史・宋史・遼史・金史・元史・明史

正史とは，原則として，王朝が公式に編纂した歴史書である。多くは，次の王朝が前の王朝の歴史を，朝廷の事業としてまとめた（たとえば『明史』は清が編纂した）。『史記』や『漢書』のように，もとは個人の著作で，のちに正史とされたものもある。24の書を正史とする数え方は，清の乾隆年間に定められた。

### 正史の中の医療

正史は政治や戦争の記録が中心だが，医療に関わる記述も数多く含まれている。

- 医師や医療に関わった人の伝：『史記』扁鵲倉公列伝をはじめ，方技伝・方術伝・芸術伝などの巻にある。華佗・孫思邈・銭乙・劉完素・李杲・李時珍など。
- そのほかの記述：
  - 皇帝や官人の病気と治療。
  - 疫病への対策や，医官・薬局の制度。
  - 外国から献上された薬物。
  - 親の病を自分の身を削って治そうとした孝行の話。
  - 不老不死の薬を求めた帝王の話。

これらは，医書には書かれない，社会の中の医療の姿を伝えている。

### この資料の目的

この資料は，公式の歴史書の中に書かれた医学の歴史を，簡単に閲覧し，また検索できるようにするために作った。

- 中国医学の通史について調べたいことがあるときの助けになることを目指している。
- 24書の記事を，句読点つきの原文と日本語訳で，書ごと・人ごと・箇所ごとに読める。
- GitHub のリポジトリ全体を，テキストとして検索できる。人名・病名・薬名のほか，「鍼」「灸」「疫」などの字でも探せる。

### 医療と呪術の境界について

古い時代に遡るほど，医学と呪術・占い・神仙術の境界は曖昧になる。正史の方術伝・芸術伝にも，医者と並んで，占い師・天文家・仙人・方士が収められている。

この資料の編集では，資料としての網羅性を重視した。そのため，境界線上にあるものも含めている。

- 今日の尺度では医学とは言い難い呪術的なもの：祈祷・符水・巫術・仙薬・丹薬・占いなど。
- 割股（自分の股の肉を切って親に食べさせる）のような孝行の話。

これらは歴史の記録として収めたもので，その効果や正しさを認めるものではない。内容については，読む人それぞれが判断してほしい。また，訳と解説は LLM で作成したもので，誤りがありうる。医療上の判断の根拠にはしないこと。

## 構成

```
index.md                 目次
NN_書名/                 00_史記 〜 23_明史（書名は新字体）
  index.md               書の目次。(1) 医師列伝集（巻ごと），(2) 引用集 の順
  b001.md / b001.ja.md   (1) 人ごとの単位。長い伝は段落の境で約1,500字ずつに分けた（倉公（1）…）
  q001.md / q001.ja.md   (2) 箇所ごとの単位
```

- `NNN.md`：YAML と原文（`## 原文`）。
- `NNN.ja.md`：日本語訳（`## 原文の訳`）と解説（`## 解説`）。

(1) は166単位（約9.1万字），(2) は1,725単位（2,282箇所，約9.2万字）。字数は句読点を除いた原文。(1) の伝がない書（漢書・宋書・南史など）は (2) だけ。

## YAML

| キー | 内容 |
|---|---|
| book | 「二十四史 医療の記事」 |
| chapter | 書の番号（0〜23） |
| chapter_title | 書名 |
| unit | 単位の番号（b001…，q001…） |
| kind | bio（(1) 医療者の伝），quote（(2) 引用） |
| name | 人名，または引用元の本紀・列伝の名 |
| juan | (1) の巻と篇名（例：史記 巻105 扁鵲倉公列伝） |
| part | (1) で伝を分けたときの何番目か（例：2/5） |
| id | (2) の箇所の番号（作業の記録との対応） |
| title | 見出し |
| punctuated | 句読点を付けたもの |

## 原文

- 漢籍リポジトリ（Kanripo，https://github.com/kanripo ）の各書（史記は TLS の版，ほかは文淵閣四庫全書本）。Kanripo で途中の巻までしかない書（三国志・晋書・北斉書・隋書・北史・旧唐書・新唐書）は，欠けている巻を Wikisource で補った。
- 字体は [字体と変換の方針](字体と変換の方針.md) により新字体にそろえた（新字体 → 旧字体 → 繁体字）。字形を確かめていない外字は ［KRnnnn］（Kanripo の外字の番号）のまま残した。
- 句読点は，句読点のない底本にこのプロジェクトで付けた（字は変えていない）。句読点のある資料（Wikisource など）はその句読点によった。割注は（　）に入れた。
- 底本の誤字と思われる字もそのままにした。
- (2) の1単位の中で段落が分かれているのは，同じ伝の離れた箇所である。

## 範囲の決め方

- (1)：18巻の伝を段落ごとに読み，医療と明らかに関係のない人の段落を除いた。
- (2)：(1) 以外で医療の字（医・医・薬・鍼・針・砭・灸・診・療）を含む箇所を集め，前後を読んで治療の話の始めと終わりを決めた。(1) の伝と同じ話，比喩・人名・地名などの別の意味，毒による自殺・処刑，医者が人物として出るだけで治療の話のない箇所は除いた。

## 訳の書き方

- (1)：伝の最初に，どの王朝のどのような人物かを解説に記し，伝はすべて訳した。
- (2)：最初に，どの時代のどのような伝からの引用かを解説に記した。
- 話の途中の政治・人事など医療と関係のない部分は全訳せず，「（この箇所は，医療と関係のない…であるため省略した：…）」の形で要約した。貢ぎ物の一覧などで薬が他の品物と並んでいるものも同じ。
- 呪術・巫術・仙薬・丹薬の話は，医療と関係がなさそうでも訳した。
- 毒殺や仮病の話は訳さず，「【訳出しない（…）】」として内容を一行で記した（原文は残した）。
- 〔　〕は補った語，【　】は注記（【同じ伝の少しあと】など），〔注：…〕は割注の訳。割注は医療に関わるものだけ訳した。
- 訳と解説は LLM（Claude）で作成した。人物の特定などに誤りがありうる。

## ライセンス

古典の文はパブリックドメイン。句読点・訳・解説など，このプロジェクトで新しく作成したものは CC BY-SA 4.0。詳しくは [LICENSE](LICENSE)。

## English summary

Medical records from the Twenty-Four Histories of China (Shiji to Mingshi): (1) biographies of physicians and other practitioners (from the fangji / fangshu / yishu chapters), and (2) passages on illness, treatment and drugs from other annals and biographies. Each unit has the punctuated classical text (`NNN.md`) and a Japanese translation with notes (`NNN.ja.md`). Classical texts are public domain (Kanripo, with gaps filled from Wikisource); new material is CC BY-SA 4.0. Translations were produced with an LLM and may contain errors. The Twenty-Four Histories are the official dynastic histories of China, mostly compiled under imperial commission. This collection aims to make the history of medicine recorded in them easy to browse and search, as an aid to research on the general history of Chinese medicine. Because the boundary between medicine and magic becomes blurred in earlier periods, and because completeness was given priority, it also includes divination, incantation, elixirs and other practices that would hardly be called medicine today; readers should judge the content for themselves.
