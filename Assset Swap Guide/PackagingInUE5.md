
## Packaging final mod file through UE5
Most of this section is heavily inspired by [this guide](https://www.abbiedoobie.com/2023/10/13/modding-robocop-rogue-city-and-other-ue-5-games/)! Was incredibly helpful.\

Launch Unreal Engine 5.1.1.

<img width="195" alt="UE1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/ca1c0f4c-3d4d-4559-aded-fa5cd8c20c25">

Create a new project: **Games** > **Blank project**, name it exactly **“Pal”** **(Very important that the project name is "Pal" or the mod won't load!)**
The Project Defaults should be:
- **Blueprint**
- Target Platform: **Desktop**
- Starter Content: **unchecked**
- Raytracing: **unchecked**
- 
<img width="897" alt="UE2" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/0782bbbe-9b49-4597-b530-9805e1f14561">

Click on **Platforms** towards the top, then **Packaging Settings**

<img width="245" alt="UESETTING" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/5c65653c-c1de-4f95-9e40-e08622395890">

Uncheck **Use Io Store** and check **Generate Chunks**.

<img width="267" alt="UESETTING2" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/41cfcb81-5046-4388-bf5d-7fa8253f8f38">

Search for **Cook everything** in the search bar and check **Cook everything in the project content directory (…)**.

<img width="377" alt="UESETTING3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/2967a6ba-031e-4464-b245-b67ac9f140a8">

Create a folder structure **matching** the one from FModel. Ignore “Pal\Content\” as the Content Browser already starts in “Content”.
**For example**, since I modified Depresso model, body texture and eyes texture, I need to create the folder structure to get to these files.

<img width="308" alt="UEPATH1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/e86dc337-3c7d-4918-8646-448bbd962089">

![UE3](https://github.com/KURAMAAA0/PalModding/assets/58988462/f737c24f-8954-411d-a51f-5545d5ec050c)

You can now drop all your **MODIFIED** files into their corresponding folder. If possible, drop the files that go into a single folder all at once. Click Import All, close the FBX import error(s).

![UE4](https://github.com/KURAMAAA0/PalModding/assets/58988462/bbbee6b6-fb03-4676-921c-4fecfde55c0b)

Now as you can see, our textures don’t look good. That is simply because we need to manually set transparent materials.
Double click on the material (sphere) with your *normally* transparent texture (eyes, mouth, etc..)
Change the **Blend Mode** to **Translucent**, and connect **A** (alpha) to **Opacity**.

<img width="941" alt="UE5" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/ec1e61ba-f8b8-4bd5-8b22-0588f51a4935">

Do that on any material you need, then dont forget to save everything (bottom right corner).

<img width="88" alt="UE6" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/85905fae-a8f9-4dda-bac6-7ee05b3c1011">

Make sure that all your files have the EXACT same name they originally had in FModel.
In my case:
**DeprivedDepresso** becomes **SK_NegativeKoala**
**DeprivedDepresso_PhysicsAsset** becomes **PA_NegativeKoala_PhysicsAsset**
**DeprivedDepresso_Skeleton** becomes **SK_NegativeKoala_Skeleton**
Note that SK_NegativeKoala_Skeleton was originally not in the same folder as the other files, so we have to create new folders and move it from its current folder.
Always keep in mind that paths and filenames are very important.

<img width="304" alt="UEPATH2" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/817dda65-6094-4bf3-9ff6-cec499f17592">

<img width="649" alt="UE4 5" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/2f0cfbef-06c0-4c18-b57b-d5f4d9dc899c">

Save everything (bottom right corner).
Go back to your **Content** folder, right click, hover over **Miscellaneous**, click on **Data Asset**.

<img width="439" alt="UE7" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/a75cf69e-50d5-480b-b695-2fefde989276">

Select **PrimaryAssetLabel**.

<img width="470" alt="UE8" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/ea81eeb5-4a13-407e-be31-9d01c842ae9f">

Name it “Label_YourModName”. I named mine “Label_DeprivedDepresso”.
Double click it, and make the following changes:
Priority set to **1 or more**
Chunk ID set to **1000 or more**, this will be in your final mod .pak to help you differentiate it from other .pak files.
Cook Rule set to **Always Cook**
Label Assets in My Directory **checked**.
Save everything (bottom right corner).
Click on **Platforms, Windows, Shipping**
Then click on **Platforms, Windows, Package Project**
Your mod will start packaging, this will take a while so grab a cup of tea!

<img width="360" alt="BLENDER3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/4be2947c-6056-4f43-9d9e-3c30fe1928b2">

Or coffee..
Once packaging is done, you’ll have 	a “Windows” folder made, go in through folder: Windows > Pal > Content > Paks.
In the Paks folder, you’ll most likely have two .pak files, **pakchunk0-Windows** and yours.
Mine is pakchunk1000-Windows because I set the Chunk ID to 1000.
You now need to go into your game local files.

<img width="367" alt="STEAM1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/c8563873-11e1-4376-a6da-09df5fdd2c0e">

Copy your .pak file to **D:\Palworld\Pal\Content\Paks**.
Rename it to *YourModName***_P** launch Palworld, and that’s it!
**(YOUR .PAK FILENAME SHOULD END WITH “_P’, ELSE IT WON’T LOAD.)**
Enjoy your beautiful creation.


### Issues & Fixes
If you run into issues that you manage to fix, DM me on Discord **kurama0** so I can potentially add the issue & fix here!
