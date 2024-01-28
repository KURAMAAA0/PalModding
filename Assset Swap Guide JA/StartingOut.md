# MOD作成の準備

## FModelにPalworldを追加

FModelを開くと、**Directory Selector**ウィンドウが開きます。\
もし Palworld が最初の選択肢になければ、矢印のマークをクリックしてPalworldを追加してください。

<img width="323" alt="FMODEL1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/5bced3f7-22dd-4ae7-b67c-854199bec4ed">

Nameを**Palworld**など好きな名前にしてください。\
DirectoryをPalworldの実行フォルダに変更します。Palworldの実行フォルダは通常以下の通りです。

```text
C:\Program Files (x86)\Steam\steamapps\common\Palworld
```

もし見つからない場合は以下の手順でも同じフォルダパスを取得できます。

1. Steamライブラリを開く
2. Palworldで右クリック
3. 管理をクリック
4. ローカルファイルを参照をクリック
5. 開いたフォルダパスをFModelに入力

入力を終えたら**OK**をクリックします。

## FModelの設定

FModelの上部のメニュー**Settings**から設定画面を開きます。\

### Generalタブの設定

1. 必要があれば**Output Directory**を任意の位置に変更します。\
   大きなファイルが出力される可能性があるので容量に余裕があるドライブを推奨します。
2. **UE Versions**を**GAME_UE5_1**に変更します。\
   これはPalworldのUEバージョンと一致します。
3. **ADVANCED**セクションの**Local Mapping File**にチェックを入れます。
4. **Mapping File Path**に先ほどダウンロードした[Palworld mapping file](https://github.com/KURAMAAA0/PalModding/raw/main/Assset%20Swap%20Guide/Mappings.usmap "Palworld mapping file")ファイルパスを設定します。

### Modelsタブの設定

1. 設定の左側にある**Models**タブをクリックします。
2. 必要があれば**Model Export Directory**を任意の位置に変更します。\
   大きなファイルが出力される可能性があるので容量に余裕があるドライブを推奨します。
3. Mesh Formatを**ActorX(psk/pskx)**に変更します。
4. Texture Formatを**PNG**に変更します。

入力を終えたら**OK**をクリックします。

### 設定の適用

念のためすべての設定を終了した後にFModelを再起動します。

## アセット探検の開始

ついにゲームファイルの探索とエクスポートを自由にできるようになりました。\
どのファイルをエクスポートするかは、ガイドの以下のセクションのいずれかを参照してください

- [3Dアセット(パル、アイテムなど)のエクスポートと変更](https://github.com/KURAMAAA0/PalModding/blob/main/Assset%20Swap%20Guide/ExportingModifying3DAssets.md "Exporting and modifying 3D assets (Pals, items, etc..)")
- [[WIP] 3Dアセット(パル、アイテムなど)のエクスポートと置換](https://github.com/KURAMAAA0/PalModding/blob/main/Assset%20Swap%20Guide/ExportingReplacing3DAssets.md)
- [[WIP] 2Dアセット（アイコン、HUD要素、画像）のエクスポートと修正](https://github.com/KURAMAAA0/PalModding/blob/main/Assset%20Swap%20Guide/ExportingModifying2DAssets.md)
- アニメーション？可能かどうかわかりません、まだ試していません。WIP。
