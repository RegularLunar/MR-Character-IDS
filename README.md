# Marvel Rivals Modding Guide

### Main Static AES Key

`0x0C263D8C22DCB085894899C3A3796383E9BF9DE0CBFB08C9BF2DEF2E84F29D74`

---

### Additional Keys

- **Marvel Rivals (pakchunkMoviesS0_1):** `0xF959B39D10C93808116F4D0C5583E1D11CBCCD428E737A48B75D40EC87FBF9D8`
- **Marvel Rivals (pakchunkMoviesS0_2):** `0xFCFC4D709BC395492703482C50DC423744B5931272587ACCD78B0E57D7215BDD`
- **Marvel Rivals (pakchunkMoviesS0_3):** `0x9F3F11DA58B6DD43266CE124F60E955C4A6BE7D5E4B23B69E63EFB0718DA952B`
- **Marvel Rivals (pakchunkMoviesS0_4):** `0xD7BA72F24C18357A2384399D98ACF9DB40DD03A55ED4128A396D3D7697930FB5`

---

## Important

- Sometimes not all of a characters textures will appear in FModel
- For instance, if you go to Spiderman `Content\Marvel\Characters\1036\1036001\Texture`
- You will see a `44` on the Texture folder, but nothing inside except 1 more folder
- In order to see his textures, you have to right click that Texture folder and `Save Folders Packages Textures`
- This will throw everything into your Output folder as pngs
- There's several other characters that have this issue, so if something looks missing, try doing this

---
## Replacing Textures

### Steps to Extract and Replace Textures

1. **Download FModel**  
   [Download here](https://fmodel.app/)

2. **Setup FModel**

   - Open FModel. Navigate to **Help > Releases** and download the latest version.
   - Set up the directory for the game under **Add Undetected Game**:
     - Name: `Marvel Rivals`
     - Path: `Steam\steamapps\common\MarvelRivals\MarvelGame\Marvel\Content\Paks`
   - Configure settings:
     - Set **Output Directory** to your desired folder.
     - Set **Archive Directory** to the same path as above.
     - In **UE Versions**, select `GAME_MarvelRivals (GAME_UE5_3)`.

3. **Add AES Keys**

   - Navigate to **Directory > AES Keys** and input the relevant keys.

4. **Extract Textures**

   - Under **Archives**, select **All** for the loading mode and click **Load**.
   - Switch to the **Folders** tab to explore game files.
   - Locate the texture (e.g., `Marvel\Characters\1031\1031001\Texture\T_1031001_Body_D.uasset`), right-click, and choose **Save Texture (.png)**.

5. **Edit Textures**

   - Edit the `.png` file in an image editor like Photoshop, maintaining original dimensions. Save your edits as `.png`.

6. **Reimport Textures**

   - Install Unreal Engine 5.3.2 from the [Epic Installer](https://www.unrealengine.com/en-US/download).
   - Create a new project named `Marvel`.
   - Recreate the original folder path (e.g., `Marvel\Characters\1031\1031001\Texture\`) and import your modified `.png` files.

7. **Pack Textures**

   - Use the updated pak creation method in Unreal Engine:
     - Enable **Use Pak File** and **Generate Chunks** under **Packaging**.
     - Assign a Chunk ID to your files under **Asset Actions**.
     - Package the project for Windows.

8. **Place Mod Files**
   - Rename the `.pak` file with a `_P` suffix (e.g., `MODNAME_P.pak`).
   - Place it in a `~mods` folder under `Steam\steamapps\common\MarvelRivals\MarvelGame\Marvel\Content\Paks`.

---

## Viewing Texture Replacements in Blender

1. **Download Blender 4.2.4 LTS**  
   [Direct Download](https://www.blender.org/download/release/Blender4.2/blender-4.2.4-windows-x64.zip)

2. **Install PSK Plugin**  
   [Download Plugin](https://extensions.blender.org/add-ons/io-scene-psk-psa/)

3. **Export Model**

   - Use FModel to locate the model (e.g., `SK_10250_1025001.uasset`) and save it as a `.psk` file.

4. **Import Model into Blender**
   - Import the `.psk` file and apply your edited textures to view changes instantly.

---

## Replacing Sounds (WIP)

### Steps to Replace Audio

1. **Extract Audio Files**

   - Use FModel to locate `.bnk` files for voices or sound effects. Extract raw data.

2. **Convert `.bnk` to `.wem`**

   - Use the [SoundMod Tool](https://mega.nz/file/N1xU0DzY#oNFpGzf-MGUYC8vZ6MAgIMYJeHvkaYsfMSA3D7924oY) to process `.bnk` files and extract `.wem` audio files.

3. **Edit Audio**

   - Replace or modify the audio files in `.wav` format. Convert back to `.wem` using [Wwise](https://www.audiokinetic.com/en/products/wwise/).

4. **Repack and Replace**

   - Use the SoundMod tool to rebuild the `.bnk` file with your custom `.wem` audio.

5. **Create and Place Mod Files**
   - Follow the pak creation steps outlined in the texture replacement section.

---

### Character ID List


- **1011**: Hulk
- **1014**: The Punisher
- **1015**: Storm
- **1016**: Loki
- **1017**: Human Torch
- **1018**: Dr.Strange
- **1020**: Mantis
- **1021**: Hawkeye
- **1022**: Captain America
- **1023**: Rocket Racoon
- **1024**: Hela
- **1025**: Dagger
- **1026**: Black Panther
- **1027**: Groot
- **1028**: Ultron
- **1029**: Magik
- **1030**: Moon Knight
- **1031**: Luna Snow
- **1032**: Squirrel Girl
- **1033**: Black Widow
- **1034**: Ironman
- **1035**: Venom
- **1036**: Spider-Man
- **1037**: Magneto
- **1038**: Scarlet Witch
- **1039**: Thor
- **1041**: Winter Soldier
- **1042**: Peni Parker
- **1043**: Star Lord
- **1044**: Blade
- **1045**: Namor
- **1046**: Adam Warlock
- **1047**: Jeff!!!!
- **1048**: Psylocke
- **1049**: Wolverine
- **1050**: Invisible Woman
- **1051**: The Thing
- **1052**: Iron Fist
- **4017**: Galacta

# CREDITS @bruhlookatthis ON DISCORD
