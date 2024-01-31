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

パル3Dモデルを修正するだけなら、ビューポートにモデルを表示したまま直接修正することができます。

### テクスチャの適用

3Dモデルを読み込んだだけでは白色のモデルが表示されるだけです。\
前の章で出力したテクスチャ(png)を適用することでカラフルなモデルを表示できます。\
テクスチャの適用は必須ではありません。不要な場合はこの章の作業は不要です。

テクスチャを表示するためにまず表示を切り替えます。\
画面上の`Viewport Shading`をクリックします。

<img alt="BLENDERTEXTURE1" src="https://github.com/rinjugatla/PalModding/assets/12833645/80e7c6e9-7e2c-4f41-a82f-f5c6a522e0bd">

右上のツリーから`SK_NegativeKoala.001`を選択します。

<img alt="BLENDERTEXTURE2" src="https://github.com/rinjugatla/PalModding/assets/12833645/b0722dfc-5b57-4a4f-b650-b37a4c136755">

次に右下のメニューから`Material Properties`をクリックします。\
`Base Color`の横の黄色い丸をクリックします。\
`Image Texture`をクリックします。

<img alt="BLENDERTEXTURE3" src="https://github.com/rinjugatla/PalModding/assets/12833645/a754498f-0e0a-46a4-a8c9-a40bbfa7ef2d">

`Open`をクリックします。\
エクスポート済みのテクスチャをすべて選択して読み込みます。

<img alt="BLENDERTEXTURE4" src="https://github.com/rinjugatla/PalModding/assets/12833645/2f947352-d30e-4fb3-b89a-bf9717af6b7c">

3Dモデルの各部位に適切なテクスチャを割り当てます。

<img alt="BLENDERTEXTURE4" src="https://github.com/rinjugatla/PalModding/assets/12833645/a628a7a0-8548-4148-9106-ec91b898368f">

テクスチャを割り当てていくとモデルの目や口に黒い背景が表示されます。

<img alt="BLENDERTEXTURE5" src="https://github.com/rinjugatla/PalModding/assets/12833645/20514987-6644-4afb-939f-5b7e15b83c61">

画面上部の`Shading`をクリックします。\
`Slot`から問題のあるテクスチャを選択します。

<img alt="BLENDERTEXTURE5" src="https://github.com/rinjugatla/PalModding/assets/12833645/a2934903-0730-4019-bfa8-136a4b32f0ac">

テクスチャの**Alpha**チャンネルをPrincipled BSDFの**Alpha**プロパティに差し込みます。

<img width="367" alt="BLENDERSHADER1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/c988b8db-3d1a-48ed-b597-8beda449cfb8">

次に、マテリアルのプロパティタブで、**Blend Mode**を**Alpha Blend**に、**Shadow Mode**を**None**に変更します。

<img alt="BLENDERSHADER2" src="https://github.com/rinjugatla/PalModding/assets/12833645/0461a3d0-6fbb-4c5a-93b6-5f6d901733c0">

パルの完成です！

<img width="398" alt="BLENDERSHADER3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/d0b93d38-ea6d-4a27-9ac4-14beab123f1f">

元のンダコアラと寝ぼけたンダコアラです。

<img width="360" alt="BLENDER3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/3cd4b1f6-17d9-4160-8c04-d0acc640ce92">

エクスポートするには、`File > Export > FBX (.fbx)`と進み、エクスポート先を選択するだけです。

最後のステップ[UE5でファイルをパックしてMODを作る](https://github.com/KURAMAAA0/PalModding/blob/main/Assset%20Swap%20Guide%20JA/PackagingInUE5.md)に進みましょう！
