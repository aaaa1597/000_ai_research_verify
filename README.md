# 目標
狙った構図で、  狙った姿勢で、  狙った位置関係で、  同一人物で、  複数人の画像を出力する

## tips
- [【Stable Diffusion】背景のみ消して背景透過の画像を作る方法とは](https://romptn.com/article/1268#:~:text=%E3%81%BE%E3%81%9A%E3%81%AF%E3%80%81txt2img%E3%81%A7%E7%94%BB%E5%83%8F%E7%94%9F%E6%88%90,%E3%81%99%E3%82%8B%E3%82%8C%E3%81%B0%E5%AE%8C%E4%BA%86%E3%81%A7%E3%81%99%EF%BC%81)
	- Stable Diffusionで生成した画像・イラストから背景のみを切り抜いて、背景なしにしたい
	- Stable Diffusionで生成した画像・イラストの背景を透過させたり単色(一色)や無地にしたい
	- Stable Diffusionで背景のみの画像を出力するプロンプトを知りたい！
- (完了)~~ABG_extension, rembg, sd_katanuki~~  
  → stable diffusionのはあんまりいけてなかった。ABGだけしか使ってないけど。

## 環境構築編
### Paperspare Gradient
- [ゼロから始めるPaperspace Gradient【Google Colab代替サービス】](https://qiita.com/kunishou/items/dccb44848e5b572619bc)

## ポーズを頑張る系
~~- [画像から呪文(プロンプト)を生成・抽出できる機能](https://romptn.com/article/11938)~~  
	~~→ 一応できた。たまにいいのが出るけどガチャがつらい。~~


- (完了)~~"i2iでラフ図から生成"をやってみる。~~
	- (完了)~~Denoising strength~~
	- (完了)→ 一応できた。線画になるけど。

- \\1000 [【Stable Diffusion】openposeでポーズを指定できる画像まとめ（50枚）](https://note.com/yuyutoto/n/n7cb92fc1d23b)
- [Stable diffusionのOpenPose Editorを使ってみた](https://hastaluegoblog.hatenablog.com/entry/2023/07/17/172411)
- [【Stable Diffusion】ゼロからポーズを作る『Openpose Editor』の使い方！](https://freeblog-video.com/stable-diffusion_extensions_openpose-editor/)
- [【超便利】Openpose Editorで棒人間を作ろう！ （Stable iffusion Web UI）](https://resanaplaza.com/2023/08/19/%E3%80%90%E8%B6%85%E4%BE%BF%E5%88%A9%E3%80%91openpose-editor%E3%81%A7%E6%A3%92%E4%BA%BA%E9%96%93%E3%82%92%E4%BD%9C%E3%82%8D%E3%81%86%EF%BC%81-%EF%BC%88stable-iffusion-web-ui%EF%BC%89/)
---
- [【ControlNet】元絵から,写真から同じ姿勢(ポーズ)を作るopenposeの使い方。画像生成AIイラスト生成のやり方♪](https://nagi.blog/ai-illustration-openpose-picture/)
- [【ControlNet】骨(棒人間)から希望の姿勢(ポーズ)を作るopenposeの使い方。画像生成AIイラスト生成♪](https://nagi.blog/ai-illustration-openpose/)
- [DesignDoll https://gigazine.net/news/20230216-stable-diffusion-controlnet/](https://gigazine.net/news/20230216-stable-diffusion-controlnet/)

	### 画像からプロンプトを生成
	- Interrogate DeepBooru ... img2img -> 画像をアップ -> 箱っぽいアイコンのボタンを押下

## 同一人物系
- [【画像生成AI】アバターを色んな角度できっちり同一人物にする！](https://jp.open-fashion.com/blogs/article/image-generation-ai-ensuring-avatar-consistency-from-various-angles)

## その他
- [画像変形　Imagic](https://note.com/tukkidney/n/n7528826d3dc7)

	### ビジネス構想
	- [Stable Diffusion Web UI でマネキンの画像から雑誌モデル風の画像を生成してみる（ControlNet 利用）](https://zenn.dev/kobayasd/articles/8511afa5f5c70e)

	### モデルをマージ
	- [【Stable Diffusion】モデルをマージ(融合)する方法を解説](https://runrunsketch.net/sd_modelmerge/)
	- [【Stable Diffusion】Scribbleで落書きがステキな絵に大変身！](https://runrunsketch.net/sd-controlnet-scribble/)


## よしなしごと
- 完成系を作るというより、多種多様な試作品を大量に生成するのに向いてる。
- 倉本圭造
	- [AIで人間の仕事はそう簡単にはなくならなさそうな理由（AIは神か？パートナーか？）](https://note.com/keizokuramoto/n/n17601da1cec6)
	- ファッション提案 ... AIは完成度7割だからね。
	- 独居老人の話し相手
	- 3Dアニメ美女と延々と恋愛トークできる。
- [【Stable Diffusion】映える構図作りの基礎知識](https://kaguluna.com/?p=574)

# アイテム
## 画像生成AIツール
- [SeaArt AI](https://www.google.com/search?sca_esv=36ab8804a141efdc&sxsrf=ACQVn08q-x-GcwPXi-LbknaOjAa0SYYnxQ:1711537587680&q=seaart&spell=1&sa=X&ved=2ahUKEwjPvLuvppSFAxUpQPUHHQ8EAZwQBSgAegQIMBAC&biw=1924&bih=1709&dpr=1)
- [Layer Diffusion 使い方](https://www.google.com/search?q=layer+diffusion+%E4%BD%BF%E3%81%84%E6%96%B9&sca_esv=36ab8804a141efdc&sxsrf=ACQVn094qKbZoaRqmdds18_IFQonEggCSA%3A1711536386520&ei=AvkDZuKxH8Onvr0P3p6mqAE&oq=layyer+diffu&gs_lp=Egxnd3Mtd2l6LXNlcnAiDGxheXllciBkaWZmdSoCCAIyExAAGIAEGA0YsQMYgwEYsQMYgwEyBxAAGIAEGA0yBxAAGIAEGA0yBxAAGIAEGA0yBxAAGIAEGA0yBxAAGIAEGA0yBxAAGIAEGA0yBxAAGIAEGA0yBxAAGIAEGA0yBxAAGIAEGA1IwC1QAFjZIXAAeAGQAQCYAbEBoAHZCqoBBDEuMTG4AQPIAQD4AQGYAgygApALwgIKECMYgAQYigUYJ8ICBBAjGCfCAgsQABiABBixAxiDAcICCBAAGIAEGLEDwgIKEAAYgAQYigUYQ8ICDRAAGIAEGIoFGEMYsQPCAhAQABiABBiKBRhDGLEDGIMBwgIFEAAYgATCAgcQABiABBgKwgIKEAAYgAQYChixA8ICDRAAGIAEGAoYsQMYgwHCAgwQABiABBgNGEYY_wHCAhgQABiABBgNGEYY_wEYlwUYjAUY3QTYAQHCAgYQABgeGArCAggQABgIGB4YCpgDALoGBggBEAEYE5IHBDEuMTGgB58u&sclient=gws-wiz-serp)

## 優先
- [2つの画像を結合して1つの画像を生成する - Stable Diffusion](https://www.ipentec.com/document/stable-diffusion-combine-two-iillustration-images)
- [2人のキャラクターが背中合わせに手をつなぐ画像を生成する - Regional prompter の利用 - Stable Diffusion](https://www.ipentec.com/document/stable-diffusion-generate-holding-hands-back-to-back-using-regional-prompter)
- [「X/Y/Z Plot」の使い方！モデルやプロンプトを比較検証しよう！【Stable Diffusion Web UI】](https://shigurepictorialbook.com/entry/2023/06/17/000000)


## 画像合成
- [簡単！StableDiffusionWebuiで画像合成　背景ざっくり雰囲気編](https://note.com/gufutokuku/n/nf7f92a3c013c)
- [簡単！StableDiffusionWebuiで画像合成　背景・人物どっちも雰囲気大切編](https://note.com/gufutokuku/n/nf7f92a3c013c)
- [Stable Diffusion2人、複数人、群衆、人混み、数指定するプロンプトと手法](https://kindanai.com/tips-multiple-people-display-guide/)
- [Stable Diffusionで複数人別々にプロンプトとポーズを指定する](https://tenpamk2-blog.netlify.app/stable-diffusion%E3%81%A7%E8%A4%87%E6%95%B0%E4%BA%BA%E5%88%A5%E3%80%85%E3%81%AB%E3%83%97%E3%83%AD%E3%83%B3%E3%83%97%E3%83%88%E3%81%A8%E3%83%9D%E3%83%BC%E3%82%BA%E3%82%92%E6%8C%87%E5%AE%9A%E3%81%99%E3%82%8B/)
- [Stable Duffusion – Latent Couple extensionで複数キャラを描き分ける](https://chitose-nanase.com/stable-duffusion-latent-couple-extension/)

## 表情差分
- [Stablediffusionで、表情差分のイラストを作成する。](https://qiita.com/itohdaigo/items/3fc0e0c6647aac04f74f)
- [Stable Diffusionで表情差分を作成する方法について解説](https://ai-illust-kouryaku.com/?p=9745)
- [【Stable Diffusion Web UI】ADetailerで表情差分を作成する方法（表情変更）](https://soroban.highreso.jp/article/article-085)
- [表情の呪文の一覧【Waifu Diffusion・NovelAI】](https://gamedev65535.com/entry/prompt_facialexpression/)
- [【プロンプト解説】Stable Diffusionで照れた表情の人物の画像を生成する方法](https://bocek.co.jp/media/stable-diffusion-formula/person-stable-diffusion-formula/4306/)
- [stable diffusion afterdetailer で表情を変更](https://qiita.com/ma7ma7pipipi/items/86c80efb1527fa5ba16d)

## アップスケール
- [Stable Diffusionで画質を爆上げするテクニック【txt2imghd】を紹介](https://qiita.com/Yasu81126297/items/752df11a1e5e70c8b9fe)

## DreamBooth
- [Diffusion Model のおもしろい技術：DreamBoothについて](https://qiita.com/xxyc/items/6bb5257be3cc1027f98a)
- [AIに自分のペットの絵を描かせてみた（StableDiffsuion, dreambooth）](https://qiita.com/ski2_1116/items/c66c65dce5559f6f727c)

## その他
- [【Stable diffusion】コスプレ呪文23選！リアル&アニメ系どちらでも使えるコスプレプロンプトを紹介](https://ai-pencil.com/stable-diffusion-prompt-cosplay/)
- [【初心者向け】Stable Diffusionのプロンプトガイド！！！](https://blogcake.net/stable-diffusion-prompt/)
