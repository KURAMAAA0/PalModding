## UE5を使用したMODファイルのパッケージ

この章の大部分は、[このガイド](https://www.abbiedoobie.com/2023/10/13/modding-robocop-rogue-city-and-other-ue-5-games/))に大きくインスパイアされています！とても参考になりました。

Unreal Engine 5.1.1を起動します。

<img width="195" alt="UE1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/ca1c0f4c-3d4d-4559-aded-fa5cd8c20c25">

新規プロジェクトを作成します： **Games** > **Blank project**, 名前を **"Pal "** にします。\
**プロジェクト名は必ず`Pal`にします。そうでないとMODがロードされません！**

プロジェクトのデフォルトを以下のように設定します。
- **ブループリント**
- ターゲット・プラットフォーム **デスクトップ**
- スターター・コンテンツ **チェックを無し**
- レイトレーシング **チェック無し**

<img width="897" alt="UE2" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/0782bbbe-9b49-4597-b530-9805e1f14561">

一番上の**プラットフォーム**をクリックし、次に**パッケージ化の設定**をクリックします。

<img width="245" alt="UESETTING" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/5c65653c-c1de-4f95-9e40-e08622395890">

loストアを使用のチェックを外し、チャンクの生成にチェックを入れます。

<img width="267" alt="UESETTING2" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/41cfcb81-5046-4388-bf5d-7fa8253f8f38">

検索バーで **すべてをクック** を検索し、**プロジェクトコンテンツディレクトリ内のすべてをクック(...)** をチェックします。

<img width="377" alt="UESETTING3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/2967a6ba-031e-4464-b245-b67ac9f140a8">

FModelのものと**同じ**フォルダ構造を作成します。コンテンツブラウザは既に "Content "から始まっているので、"Pal\Content\"は無視します。\
**例えば**、Depressoモデル、ボディ・テクスチャ、目のテクスチャを修正したので、これらのファイルにアクセスするためのフォルダ構造を作成する必要があります。

<img width="308" alt="UEPATH1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/e86dc337-3c7d-4918-8646-448bbd962089">

![UE3](https://github.com/KURAMAAA0/PalModding/assets/58988462/f737c24f-8954-411d-a51f-5545d5ec050c)

これで、すべての **MODIFIED** ファイルを対応するフォルダにドロップすることができます。\
可能であれば、1つのフォルダに入るファイルを一度にドロップします。\
Import Allをクリックし、FBXインポートエラーを閉じます。

![UE4](https://github.com/KURAMAAA0/PalModding/assets/58988462/bbbee6b6-fb03-4676-921c-4fecfde55c0b)

Blenderで同様の問題が起こったように目や口回りのテクスチャの見栄えはよくありません。\
これは、透明マテリアルを手動で設定する必要があるからです。\
画面中央や右のツリーからキャラクタを選択し、右下のウィンドからマテリアルのカテゴリを探します。\
通常**透明なテクスチャ（目、口など）**があるマテリアル（球体）をダブルクリックします。\
マテリアルの設定画面左からマテリアルの**Blend Mode**を**Translucent**に変更し、**A（アルファ）**を**オパシティ**に接続します。

<img width="941" alt="UE5" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/ec1e61ba-f8b8-4bd5-8b22-0588f51a4935">

必要なマテリアルに同じ処理をした後、保存することを忘れないでください\
右下隅に～が未保存ですの表示があります。

<img width="88" alt="UE6" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/85905fae-a8f9-4dda-bac6-7ee05b3c1011">

すべてのファイルがFModelで元々持っていたものと全く同じ名前を持っていることを確認してください。\
この例の場合は\
**DeprivedDepresso** は **SK_NegativeKoala** になります。\
**DeprivedDepresso_PhysicsAsset** は **PA_NegativeKoala_PhysicsAsset** になります。\
**DeprivedDepresso_Skeleton** は **SK_NegativeKoala_Skeleton** になります。\
SK_NegativeKoala_Skeletonは元々他のファイルと同じフォルダーになかったので、新しいフォルダーを作り、現在のフォルダーから移動させます。\
**パスとファイル名は非常に重要であることを常に念頭に置いてください。**

<img width="304" alt="UEPATH2" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/817dda65-6094-4bf3-9ff6-cec499f17592">

<img width="649" alt="UE4 5" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/2f0cfbef-06c0-4c18-b57b-d5f4d9dc899c">

UE5のウィンド右下の「すべてを保存」をクリックします。\
**Content**フォルダ(ツリーではなくフォルダ内)に戻り、右クリックから**その他**の**データアセット**をクリックします。

<img width="439" alt="UE7" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/a75cf69e-50d5-480b-b695-2fefde989276">

**PrimaryAssetLabel**を選択します。(検索すると便利です)

<img width="470" alt="UE8" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/ea81eeb5-4a13-407e-be31-9d01c842ae9f">

名前は`Label_YourModName`とします。\
私は`Label_DeprivedDepresso`としました。\
これをダブルクリックし、以下の変更を加えます。
- Priorityを**1以上**
- Chunk IDを**1000以上**\
  これはMODの.pakに記載されるので他の.pakファイルと区別するのに役立ちます。
- Cook Ruleを**Always Cook**
- Label Assets in My Directoryを**チェック**

設定が終わったらウィンド右下の「すべてを保存」をクリックします。\
画面上部のプラットフォームからWindows、シッピングの順にクリックします。\
次に**プラットフォーム, Windows, プロジェクトをパッケージ化**をクリックします。\
出力先のフォルダを作成または選択します。\
思ったよりも時間がかかるので、お茶でも飲んでください！
カップ麺もいけます。

<img width="360" alt="BLENDER3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/4be2947c-6056-4f43-9d9e-3c30fe1928b2">

パッケージ化が終わると「Windows」フォルダが作られます。
フォルダを開きWindows > Pal > Content > Paksフォルダの中に以下のファイルがあるはずです。
- pakchunk0-Windows
- pakchunk1000-Windows\
  1000はチャンク番号です。変更している場合は読み替えます。

次に、ゲームのローカルファイルに入る必要があります。

<img width="367" alt="STEAM1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/c8563873-11e1-4376-a6da-09df5fdd2c0e">

.pakファイルをあなたのゲームのインストール先にコピーします。\
例えば`D:\Palworld\Pal\Content\Paks`です。\
そしてファイル名をYourModName**_P**に名前を変更します。\
.pakファイルの名前は必ず`_P`で終わる必要があります！

それではあなたの作品を楽しんでください。

### 問題や修正

もしあなたが問題に遭遇し、それを解決することができたら、Discordの**kurama0**までDMをください！
