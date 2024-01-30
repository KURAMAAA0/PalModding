# 3Dアセットのエクスポートと修正

このセクションでは、3Dアセットを修正するためにエクスポートする正しいファイルを見つける方法を学びます。\
Blender の使い方は学びません。

## パルの3Dモデルを探してエクスポートする

パルの3Dモデルを見つけたい場合は、FModelで`Control + Shift + F`を押すか、**Package** をクリックしてから **Search** をクリックし、検索ボックスで SK_*PalCodeName* を検索してください。

#### 任意のパルのコードネーム(Code Name)を見つけるには、[この資料](https://github.com/KURAMAAA0/PalModding/blob/main/PalNamesCodeNames.txt "HERE")から目的のパルを検索します。

検索結果の最初のファイルをダブルクリックします。\
名前の最後に`_Skeleton`がないものを選びます。\
検索結果のファイルの1つ上のフォルダ、つまり上のタブの**Folders**をクリックします。

<img width="301" alt="FMODEL2" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/6c0d144c-5a52-465b-8d76-f404d6ab3474">

パルのフォルダを右クリックし、Save Folder's Packages **Textures** (.png)をクリックします。\
パルのフォルダを右クリックし、Save Folder's Packages **Models** (.psk)をクリックします。\
これでパルの3Dモデルを**Blender**を開くことができます。

## Blenderで3Dモデルをインポート

Blenderで、`File > Import > Unreal PSK (.psk/.pskx)`をクリックします。\
ここでメニューに項目がない場合は[DarklightGames' psk/psa importer](https://github.com/DarklightGames/io_scene_psk_psa/releases)が導入されているか確認します。\
Add-onsにインストールした後にチェックを入れて有効化することを忘れないでください。

<img width="360" alt="BLENDER1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/98e6e332-75d2-4c60-ad49-d557459ce8d4">

FModelの出力フォルダ、`Output > Exports`に移動し、SK_***PalCodeName**.psk**ファイルが見つかるまでフォルダを移動し、インポートします。\
テクスチャは.pskと同じフォルダにあるはずなので、パルモデルに差し替えたくなければ適用し、そうでなければ無視します。\
ンダコアラ（コードネーム：NegativeKoala）のモデルを編集して、完全に寝ぼけたンダコアラにします。\
また、彼のテクスチャも変更します。画像の置き換え/編集の方法を学びたい場合は**このセクション**をご覧ください（テクスチャの置き換え/編集と同じ手順です）。

## Blenderによる3Dモデルの修正

パル3Dモデルを修正するだけなら、ビューポートにモデルを表示したまま直接修正することができます。\
モデルの目や口に黒い背景がある場合、問題のあるテクスチャを選択し、**Shader Editor**に移動して、テクスチャの**Alpha**チャンネルをPrincipled BSDFの**Alpha**プロパティに差し込みます。

<img width="367" alt="BLENDERSHADER1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/c988b8db-3d1a-48ed-b597-8beda449cfb8">

次に、マテリアルのプロパティタブで、**ブレンドモード**を**アルファブレンド**に、**シャドウモード**を**なし**に変更します。

<img width="187" alt="BLENDERSHADER2" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/41e5a112-f107-468d-b69b-e38b9a36bfce">

パルの完成です！
<img width="398" alt="BLENDERSHADER3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/d0b93d38-ea6d-4a27-9ac4-14beab123f1f">

元のンダコアラと寝ぼけたンダコアラです。
<img width="360" alt="BLENDER3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/3cd4b1f6-17d9-4160-8c04-d0acc640ce92">
\
エクスポートするには、`File > Export > FBX (.fbx)`と進み、エクスポート先を選択するだけです。
\
最後のステップ[UE5でファイルをパックしてMODを作る](https://github.com/KURAMAAA0/PalModding/blob/main/Assset%20Swap%20Guide%20JA/PackagingInUE5.md)に進みましょう！
