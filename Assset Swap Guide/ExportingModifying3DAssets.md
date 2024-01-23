<img width="398" alt="BLENDERSHADER3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/7ab04e2e-fc9b-4e58-b098-67c3a1b92bff"># Exporting and modifying 3D assets
In this section, you'll learn how to find the right files to export in order to modify 3D assets. You will not be taught how to use Blender.
## Finding and exporting 3D models of Pals
If you want to find a Pal 3D model, press Control + Shift + F in FModel, or click **Package** then **Search**, then in the search box, search for SK_*PalCodeName*.
##### To find the codename of any Pal, click **[HERE](https://github.com/KURAMAAA0/PalModding/blob/main/PalNamesCodeNames.txt "HERE")** and search for your wanted pal.

Double click on the first one, should be the one **without** "_Skeleton" at the end.\
Then go up one folder, meaning you shoud click on **"Folders"** at the top.
<img width="301" alt="FMODEL2" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/6c0d144c-5a52-465b-8d76-f404d6ab3474">\

Right click on your Pal's folder, click save Folder's Packages **Textures** (.png)\
Right click on your Pal's folder, click save Folder's Packages **Models** (.psk)\
Now you can go ahead and open **Blender**.\
\

## Importing the 3D models in Blender
In Blender, click on **File > Import > Unreal PSK (.psk/.pskx)**
<img width="360" alt="BLENDER1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/98e6e332-75d2-4c60-ad49-d557459ce8d4">\

Go to the output folder you set when changing FModel's settings, **Output** > **Exports**, > go through the folders until you find the SK_***PalCodeName*.psk** file and import it.\
The textures should be in the same folder as the .psk, apply them to the Pal model if you don't want to replace him, otherwise ignore.\
We'll make Depresso (code name: NegativeKoala) into a completely sleep deprived Depresso by editing his model.\
We will also change his textures, go to **this section** if you want to learn how to replace/edit images (same process as replacing/editing textures).\
\

## Modifying/Replacing the 3D models in Blender
If you only want to modify your Pal 3D model, you can keep the model present in the viewport and do the modifications directly on it.\
If your model has a black background for his eyes and mouth, select the texture(s) with the issue, go to the **Shader Editor**, plug the **Alpha** channel of the texture into the **Alpha** property of the Principled BSDF.
<img width="367" alt="BLENDERSHADER1" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/22aab63c-6c56-469e-ba56-30b8b6483777">\

Then in the Material Properties tab change the **Blend Mode** to **Alpha Blend** and the **Shadow Mode** to **None**.
<img width="166" alt="BLENDERSHADER2" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/8eefd16f-c2ee-4ee7-b3db-d10c931f30b8">\

Your Pal is fixed!
<img width="398" alt="BLENDERSHADER3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/d0b93d38-ea6d-4a27-9ac4-14beab123f1f">\



Here's the poorly made "Sleep Deprived Depresso", as well as his textures changed.
<img width="360" alt="BLENDER3" src="https://github.com/KURAMAAA0/PalModding/assets/58988462/3cd4b1f6-17d9-4160-8c04-d0acc640ce92">\

\
To export, simply go to **File > Export > FBX (.fbx)** and choose where you want to export it.\
\
Let's proceed with the final step, packaging the file in UE5 to get a mod file!
