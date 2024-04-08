[モデル一覧](C:/stable-diffusion)

# 目標
狙った構図で、  狙った姿勢で、  狙った位置関係で、  同一人物で、  複数人の画像を出力する  

一般的にイラスト系は、背景の描写やポーズ、アングルなど、リアル系より出やすい、つまり自由度が高い特徴がある。
この特徴を利用して、まずは好みのポーズやアングル等をこちらで生成してから、ControlNet / Depthで奥行き情報に変換し、
そちらを元に今度は3次元リアル系Modelで再度生成することで、リアル系が苦手なポーズ、アングルなどをある意味力技で何とかすることも可能だ。

## tips
- [【Stable Diffusion】背景のみ消して背景透過の画像を作る方法とは](https://romptn.com/article/1268#:~:text=%E3%81%BE%E3%81%9A%E3%81%AF%E3%80%81txt2img%E3%81%A7%E7%94%BB%E5%83%8F%E7%94%9F%E6%88%90,%E3%81%99%E3%82%8B%E3%82%8C%E3%81%B0%E5%AE%8C%E4%BA%86%E3%81%A7%E3%81%99%EF%BC%81)
	- Stable Diffusionで生成した画像・イラストから背景のみを切り抜いて、背景なしにしたい
	- Stable Diffusionで生成した画像・イラストの背景を透過させたり単色(一色)や無地にしたい
	- Stable Diffusionで背景のみの画像を出力するプロンプトを知りたい！
- (完了)~~ABG_extension, rembg, sd_katanuki~~
	→ 一旦完了。Stable Diffusionのはイケてなかった。
- **SDXL:** 高解像度の方法1
	**SDXL** を使って1,280x1,920の画像を作りたい  
		→ 一旦推奨値の832x1,216で作成 → Upscale 1.6x(1,331x1,945)する。※Upscaler、Denoising strength値がコツ。
- **SDXL:** 高解像度の方法2
	Deep Shrink Hires.fixで、いきなり1,280x1,920で生成
- **SDXL:** from below(下からの)は効きが悪いらしい。
- **SDXL:** from behind(後ろから)よりback viewの方が効きがいいらしい。
- **SDXL:** from side(横から)よりside viewの方が効きがいいらしい。
- 画像からプロンプトを生成
	- Interrogate DeepBooru ... img2img -> 画像をアップ -> 箱っぽいアイコンのボタンを押下
- [【Stable Diffusion】映える構図作りの基礎知識](https://kaguluna.com/?p=574)

## 環境構築編
### Paperspare Gradient
- [[生成ai][無料]Stable Diffusionを使う時の自分なりの最適解。](https://zenn.dev/rg687076/articles/0ad4da437d4782)

## ポーズを頑張る系
~~- [画像から呪文(プロンプト)を生成・抽出できる機能](https://romptn.com/article/11938)~~  	→ 一応できた。たまにいいのが出るけどガチャがつらい。

- (完了)~~"i2iでラフ図から生成"をやってみる。~~ → 一応できた。線画になるけど。

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

## Action アイテム
###  Stable Diffusion 三面図
- [【プロンプト解説】Stable Diffusionで三面図を作成する方法](https://bocek.co.jp/media/midjourney-formula/person/6083/)
- [【超簡単キャラデザ】Stable Diffusionでプロンプトだけでキャラクターデザインを作る方法](https://note.com/koresugo/n/n62601015f7b4)
### DreamBoothで鬼滅の刃の蟲柱の服をナウシカに着てもらう事は可能か？
- [DreamBoothで鬼滅の刃の蟲柱の服をナウシカに着てもらう事は可能か？](https://webbigdata.jp/post-16331/)
- [ai漫画 作り方](https://www.google.com/search?q=ai%E6%BC%AB%E7%94%BB+%E4%BD%9C%E3%82%8A%E6%96%B9&sca_esv=6457b5ff455aa099&sca_upv=1&sxsrf=ACQVn08dF4xFO49KR8BIlsAmap0o0iNhjQ%3A1712576873400&ei=adkTZviJGPyo2roPreq64A8&ved=0ahUKEwi44sGBxrKFAxV8lFYBHS21DvwQ4dUDCBA&uact=5&oq=ai%E6%BC%AB%E7%94%BB+%E4%BD%9C%E3%82%8A%E6%96%B9&gs_lp=Egxnd3Mtd2l6LXNlcnAiEmFp5ryr55S7IOS9nOOCiuaWuTIIEAAYBxgEGB4yChAAGAgYBxgEGB4yBRAAGIAEMgoQABgIGAcYBBgeMgoQABgIGAcYBBgeSK0IUOcGWOcGcAF4AZABAJgBd6ABd6oBAzAuMbgBA8gBAPgBAZgCAqACfsICChAAGEcY1gQYsAOYAwCIBgGQBgqSBwMxLjGgB8wC&sclient=gws-wiz-serp)

## Stable Diffusionの小技系
- []()

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





# (24.03.28)ネガティブプロンプトの調査
easynegative, ng_deepnegative_v1_75t, negative_hand-neg,  bad-hands-5, (ugly face:0.8),cross-eyed,sketches, (worst quality:2), (low quality:2), (normal quality:2), lowres, normal quality, ((monochrome)), ((grayscale)), skin spots, acnes, skin blemishes, lowres, bad anatomy, bad hands, text, error, missing fingers, extra digit, fewer digits, cropped, worstquality, low quality, normal quality, jpegartifacts, signature, watermark, username, blurry, bad feet, cropped, poorly drawn hands, poorly drawn face, mutation, deformed, worst quality, normal quality, jpeg artifacts, signature, watermark, extra fingers, fewer digits, extra limbs, extra arms,extra legs, malformed limbs, fused fingers, too many fingers, long neck, cross-eyed,mutated hands, polar lowres, bad body, bad proportions, gross proportions, text, error, missing fingers, missing arms, missing legs, extra digit, extra arms, extra leg, extra foot, ((repeating hair))  
(醜い顔:0.8)、寄り目、スケッチ、(最悪品質:2)、(低品質:2)、(通常品質:2)、低解像度、標準品質、((モノクロ))、((グレースケール)) 、肌のシミ、ニキビ、肌の傷、悪い解剖学、低解像度、悪い手、テキスト、エラー、指の欠落、余分な指、余分な指、少ない桁、切り取られた、最悪の品質、低品質、通常品質、jpegartifacts、署名、透かし、ユーザー名、ぼやけた、悪い足、切り取られた、下手に描かれた手、下手に描かれた顔、突然変異、変形、最悪の品質、通常の品質、jpeg アーティファクト、署名、透かし、追加指、指の数が少ない、余分な手足、余分な腕、余分な脚、奇形の手足、融合した指、多すぎる指、長い首、寄り目、変異した手、極低解像度、悪い体、悪いプロポーション、全体的なプロポーション、テキスト、エラー、指が欠けている、腕が欠けている、足が欠けている、余分な指、余分な腕、余分な脚、余分な足、((繰り返しの髪))

# (24.03.28)お試しコマンド
nsfw, 1boy and 1girl,cum in pussy,sex, hetero, clothed female nude male CFNM, normal body type, small hips, big breasts, (happy:1.2), (blush stickers), middle age lady,30-year-old,


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

## 同一人物
- [【画像生成AI】アバターを色んな角度できっちり同一人物にする！](https://jp.open-fashion.com/blogs/article/image-generation-ai-ensuring-avatar-consistency-from-various-angles)

## DreamBooth
- [Diffusion Model のおもしろい技術：DreamBoothについて](https://qiita.com/xxyc/items/6bb5257be3cc1027f98a)
- [AIに自分のペットの絵を描かせてみた（StableDiffsuion, dreambooth）](https://qiita.com/ski2_1116/items/c66c65dce5559f6f727c)


## ネガティブ プロンプト
- [Stable Diffusionのおすすめ『embedding』を紹介！使い方も解説](https://romptn.com/article/20564)
easynegative, negative_hand, (big breasts:0.9), anal, interlocked fingers
https://romptn.com/article/20564

## その他
- [【Stable diffusion】コスプレ呪文23選！リアル&アニメ系どちらでも使えるコスプレプロンプトを紹介](https://ai-pencil.com/stable-diffusion-prompt-cosplay/)
- [【初心者向け】Stable Diffusionのプロンプトガイド！！！](https://blogcake.net/stable-diffusion-prompt/)


## ポジティブプロンプト
beautiful lady, (big breasts:0.8)
nsfw,1girl,1boy,cum in pussy,sex, hetero, clothed female nude male CFNM, normal body type, small hips, big breasts, ahegao
nsfw,1girl,1boy,cum in pussy,sex, hetero, clothed female nude male CFNM, normal body type, small hips, big breasts, happy, full-face blush

## Embedding ネガティブ プロンプト
①EasyNegative		EasyNegative
②bad_prompt		(bad_prompt:0.8)
③bad-hands-5
④badhandv4
Deep Negative	NG_DeepNegative_V1_75T
bad-artist

## モデル
- BRAV5(Beautiful Realistic Asians V5)
- BracingEvoMix
- yayoi_mix
- BracingEvoMix_v1
- BracingEvoMix_Fast_v1
- BracingEvoMix_Another_v1
- sweetmuse_v01
- realbeautymix_v15
- yayoi_mix_v20
- minaduki_mix

SDXL用
- cherryPickerXL v2.7
- photopediaXL Type 1
- realisticStockPhoto v1.0
- SoraAni25XL | Anime & 2.5D v1.0

### モデルのポーズ
- standing(立つ)
- sitting(座る)
- looking at viewer(視線こっち)
- lie down(寝転ぶ)

### カメラの撮影位置
- from front(前から)
- from above(上から)
- from below(下から)
- from behind(後ろから)
- from side(横から)

### 構図
- full body(全身)
- half body(またはupper body/上半身)
- portrait(バストアップ)
- thigh focus(膝上)

### openpose
- openpose_full
- openpose_hand

#### [グラビアをグラビアカメラマンが作るとどうなる？](https://www.techno-edge.net/special/560/recent/%E7%94%9F%E6%88%90AI%E3%82%B0%E3%83%A9%E3%83%93%E3%82%A2%E3%82%92%E3%82%B0%E3%83%A9%E3%83%93%E3%82%A2%E3%82%AB%E3%83%A1%E3%83%A9%E3%83%9E%E3%83%B3%E3%81%8C%E4%BD%9C%E3%82%8B%E3%81%A8%E3%81%A9%E3%81%86%E3%81%AA%E3%82%8B%EF%BC%9F?page=1)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第一回：実在モデルで学習・LoRAでキャッチライト付加 (西川和久)](https://www.techno-edge.net/article/2023/07/11/1580.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第二回：「アジア美女」最新モデルBRAV6作例とネガティブプロンプトの基礎](https://www.techno-edge.net/article/2023/07/18/1612.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第三回：実際の撮影とポーズ/構図の関係。openpose_handで指問題解決？ (西川和久)](https://www.techno-edge.net/article/2023/07/25/1645.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第四回：高品質画像生成AI「SDXL 1.0」リリース！導入方法と作例](https://www.techno-edge.net/article/2023/07/27/1655.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第五回：Stable Diffusionの基本1 / Checkpointとリアル系モデルの遷移 (西川和久)](https://www.techno-edge.net/article/2023/08/08/1719.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第六回：Stable Diffusionの基本2 / LoRAの概要と6つの例を紹介 (西川和久)](https://www.techno-edge.net/article/2023/08/22/1780.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第七回：自分で始める環境作りとお薦め機材 / AUTOMATIC1111を動かしてみる (西川和久)](https://www.techno-edge.net/article/2023/09/25/1974.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第八回：シンプルで高機能なSDXL専用インターフェースFooocusとFooocus-MREの使いかた (西川和久)](https://www.techno-edge.net/article/2023/09/29/2004.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第九回：Fooocus-MREでimage-2-imageやControlNetを試す (西川和久)](https://www.techno-edge.net/article/2023/10/11/2064.html)  
	→ image-2-image / Upscale  
	→ ControlNetのCannyとDepth  
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第十回：実在モデルからSDXL用顔LoRAを作る (西川和久)](https://www.techno-edge.net/article/2023/10/18/2106.html)
	→ LoRAの作り方
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第11回：Stable Diffusion 1.5の注目ModelやLoRAを紹介+α版 (西川和久)](https://www.techno-edge.net/article/2023/10/25/2138.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第12回：SDXL用ModelやLoRAをピックアップ+α版。寝転びポーズや「東京駅」で撮影など (西川和久)](https://www.techno-edge.net/article/2023/11/09/2229.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第13回：SDXLでのControlNet活用方法その1+α版（西川和久）](https://www.techno-edge.net/article/2023/11/20/2296.html)  
	→ ControlNet  
		→ Cannyで構図と人を固定する。  
		→ OpenPose(openpose、openpose_face、openpose_faceonly、openpose_full、openpose_hand)で構図と人を固定する。  
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第14回：2023年下半期まとめ+α　13回分を振り返る (西川和久)](https://www.techno-edge.net/article/2023/12/14/2454.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第15回：SDXLでのControlNet活用方法その2＋ 衣服を固定できるOutfit Anyone (西川和久)](https://www.techno-edge.net/article/2023/12/19/2488.html)  
	→ ControlNet  
		→ Reference(reference_only(顔似), reference_adain(構図似), reference_adain+attn(両方))  
			Referenceは、文字通りリファレンス。つまり指定した画像をリファレンスとして、似ている画像を生成する。
		→ **SDXL:** Revision(revision_clipvision(プロンプト), revision_ignore_prompt(画像情報のみ))  
		→ IP-Adapter  
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第16回：指問題解決！？Hand Refiner (西川和久)](https://www.techno-edge.net/article/2024/01/21/2661.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第17回：新技術をすぐ試せるComfyUIのインストール・使いかた (西川和久)](https://www.techno-edge.net/article/2024/01/31/2720.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第18回：バレンタイン編。ComfyUIの環境を整える (西川和久)](https://www.techno-edge.net/article/2024/02/14/2802.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第19回：ComfyUIで最新のStable Cascadeを試す＋アナログ風の後処理ProPost (西川和久)](https://www.techno-edge.net/article/2024/02/27/2870.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第20回：MシリーズMacでもComfyUI+フロントUIが動く！ComflowySpaceの使い方(西川和久)](https://www.techno-edge.net/article/2024/03/24/3032.html)
- [生成AIグラビアをグラビアカメラマンが作るとどうなる？第21回：ComfyUI応用編。ControlNetでポーズ・構図を指定する (西川和久)](https://www.techno-edge.net/article/2024/03/31/3081.html)

