<div align="center">
  <img src="https://github.com/TCML-Team/.github/blob/main/resources/Icon-Transparent-1024.png" width="300vh">
  <h1 style="font-family: Fira Sans">- &nbsp; Tears of the Kingdom Mod Manager &nbsp; -</h1>
</div>

<p align="center" style="text-align: center;">
  <a href="https://github.com/TCML-Team/Tcml/releases">
    <img src="https://img.shields.io/github/v/tag/TCML-Team/Tcml?style=for-the-badge&logoColor=C71B42&color=C71B42&labelColor=2A2C33&logo=github&label=Version" alt="Releases' YouTube"/>
  </a> &nbsp;
  <a href="https://discord.com/invite/w7qGa5RyMc">
    <img src="https://img.shields.io/discord/1179611100183011429?style=for-the-badge&logoColor=3b83c8&color=3b83c8&labelColor=2A2C33&logo=discord&label=discord" alt="Discord"/>
  </a> &nbsp;
  <a href="https://github.com/TCML-Team/Tcml">
    <img src="https://img.shields.io/github/stars/TCML-Team/Tcml?style=for-the-badge&logoColor=FFCB41&color=FFCB41&labelColor=2A2C33&logo=github" alt="Stars"/>
  </a>
</p>

[![]("https://gamebanana.com/wips/embeddables/81203?type=medium")](https://gamebanana.com/wips/81203)

**TKMM**, an acronym for **T**ears of the **K**ingdom **M**od **M**anager, is a versatile tool crafted to streamline modding across multiple platforms for the game *Tears Of The Kingdom*. **TKMM** utilizes and seamlessly integrates with various mod merging tools, delivering a quick and satisfying experience for modders, and end users alike.

<p>
  <a href="https://github.com/TCML-Team/Tcml/issues">
    <img src="https://img.shields.io/github/issues/TCML-Team/Tcml?logoColor=red&color=red&logo=github&style=flat&labelColor=2A2C33" alt="Issues"/>
  </a> &nbsp;
  <a href="https://github.com/TCML-Team/Tcml/pulls">
    <img src="https://img.shields.io/github/issues-pr/TCML-Team/Tcml?style=flat&labelColor=2A2C33&logoColor=blue&color=blue&logo=github" alt="Open Pull Requests"/>
  </a> &nbsp;
  <a href="https://github.com/TCML-Team/Tcml/pulls">
    <img src="https://img.shields.io/github/issues-pr-closed/TCML-Team/Tcml?style=flat&labelColor=2A2C33&logoColor=5751FF&color=5751FF&logo=github" alt="Closed Pull Requests"/>
  </a>
</p>

## Mod Merging

TKMM integrates with multiple mod merging tools to support the seamless combination of various file types.

### Current Supported File Types

* **ResourceSizeTable** [LordBubbles's](https://github.com/MasterBubbles) branch of [dt12345]()'s restbl tool has been curated for maximum efficiency, and convienience!
* **RSDB** *(Tag.Product, PouchActorInfo, GameActorInfo, etc.)* inspired by [Legend5v's](https://gamebanana.com/members/2731522)'s original code, [Lord Bubbles's](https://github.com/MasterBubbles) [RSDB merger](https://github.com/MasterBubbles/rsdb-merge) is easy to use, and very efficient.
* **Localization (Mals)** created by [Arch Leaders](https://github.com/ArchLeaders), his [MalsMerger](https://github.com/ArchLeaders/MalsMerger) is lightning fast, ensuring you recieve your merged files as fast as possible.
* **SARC Archives (.pack)** created by [Mika](https://github.com/okmika), his [SARC and BYML Merger](https://github.com/okmika/TKMM-SARC) is fast, efficient, and well written.
* > **BYML Files (.byml, .bgyml)**  
* **ShopParam Exceptions** created by [Mika](https://github.com/okmika), [Bubbles](https://github.com/MasterBubbles), and [5th](https://github.com/The5thTear), the ShopParam handler will prevent errors in regards with too many shop entries, allowing users to order their overflow shops and keep their mods from breaking.
  
### Potential Future File Type Support
    
* **BFRES:** Models (texture frame anims?)
* **TXTG:** Textures (pixel by pixel merging?)
* **.bntx:** SARC image archives

> Note: Priority-based merging for specific file types (e.g. bfres, txtg).

## Usage

### For Creators:

If you are a mod creator, and would like your mod to be fully supported by TKMM, here are the steps you can follow:

> *This is required by TKMM, but you can package old mods that aren't in TKCL format (directly in the app), and then they will work just fine.*

# Using The .TKCL Packager

The .TKCL Packager is simple and easy to use, designed with end users in mind. TKMM will handle the annoying backend stuff while you can have a seamless experience.

## Input Fields:

The Input Fields for the .TKCL Packager include:
  
- Output Path (C:\TotK\ExportedMod.TKCL)
- Input Mod Folder (the mod you want to package...)
- Mod Name (the name of the mod...)
- The MOD Version (not the game version, but the version of the mod)
- Author Name (the main authors name...)
- Mod Description (the description of the mod)
- Thumbnail Path/Url (the path of the thumbnail you would like to use)

## Packaging With The .TKCL Packager

Packaging with TKMM is simple. After setting up the [input fields](#input-fields), even end users will be able to package mods.

Simply press the "Create Package" button located directly beneath the input fields, and the tool will automatically generate changelogs for you.

If you encounter any errors, feel free to join the discord and report it in #bug-reports

## info.JSON Structure
  ```jsonc
    {
    "Id": "00000000-0000-0000-0000-000000000000", - GUID, DO NOT MAKE ANY GUID'S MATCH
    "Name": "Insert Mod Name Here",
    "Version": "Mod Version, Not Game Version",
    "Author": "Main Author Goes Here",
    "Contributors": [
        {
        "Name": "Contributor 1",
        "Contributions": ["Contributions"]
        },
        {
        "Name": "Contributor 2",
        "Contributions": ["Contributions"]
        }
    ],
    "Description": "Description Goes Here",
    "ThumbnailUri": "thumbnail name or url goes here."
    }
  ```

---

# Merging Mods

```
1. Import All Mods Using Mod > Import, or dragging and dropping TKCL package's onto the program.

2. Configure the priority list (the higher up the mod, the higher the priority).

3. Merge All Mods Using Mod > Merge

4. Your Merged Mods Will Be Located In "insert final path here"
```

# ShopParam Exceptions

#### ShopParam Parameter files break after being overloaded with more than 111 entries.

To combat this, a system has been set in place to supply the overflowing entries with a place to go.
  
On the right side of the screen, located in settings, users can re-order every shop in the game (priority wise), to determine which files get filled first, second, and so on.
  
> Sometimes this is neccesary, but the team has your back covered!

# KAREN: Needs To Speak To The Manager

**Karen, or**

**K** - Key  
**A** - Archival  
**R** - Resource  
**E** - Execution  
**N** - Network  

is the codename for the backend merging and packaging logic for TKMM (The KAREN Mod Manager).

## Overview

Karen operates silently behind the scenes as the central system within TKMM, managing and executing the complex tasks of merging and packaging mods. Its primary purpose is to streamline the process, making it user-friendly and efficient, handling all the intricate details that typically burden the end-user.

## Merging Process

Karen's merging process is a multi-step procedure designed to handle various mods with precision and care.

#### 1. RSDB:
   - **Priority Handling**: Pass the priority list through Karen to determine the order of mod application.
   - **Reverse Priority Application**: Apply through reverse priority to ensure the correct layering and compatibility of mods.
   - **Output Handling**: Pass the results through Karen to the ModOutput folder, ensuring a clean and organized structure.

#### 2. SARC:
   - **Argument Conversion**: Convert the modlist to acceptable args through Karen, ensuring compatibility and correct formatting.
   - **Changelog Rebuilding**: Rebuild changelog SARC's to keep a detailed record of changes and updates.
   - **Output Management**: Pass the results through Karen to the ModOutput folder, maintaining a streamlined process.

#### 3. Mals:
   - **Argument Conversion and Handling**: Convert modlist to acceptable args through Karen, similar to the SARC process.
   - **Mals Rebuilding**: Rebuild Mals through Karen using the changelogs, ensuring a clean and updated merge.
   - **Result Integration**: Pass the results through Karen to the ModOutput folder, finalizing the merge.

#### 4. General (priority merging):
   - **Priority List Management**: Pass the priority list through Karen for efficient handling.
   - **Unmergable File Detection**: Transfer unmergable files (detected with Karen) to ensure a clean and error-free merge.

#### 5. RSTB:
   - **Resource Table Generation**: Pass the ModOutput Folder and generate a fresh ResourceSizeTable using Karen, ensuring all resources are correctly accounted for.

## Packaging Process

The packaging process ensures that all components are properly assembled, and ready for distribution.

#### 1. RSDB:
   - **Folder Search**: Search for the RSDB Folder to locate all relevant files.
   - **Changelog Generation**: Generate changelogs through Karen for a clear record of all changes.
   - **File Cleanup**: Delete old RSDB files to maintain a clean and up-to-date system.

#### 2. Mals:
   - **Changelog Generation**: Generate changelogs through Karen, similar to the RSDB process.
   - **File Cleanup**: Delete old Mals files, ensuring only the latest and most relevant files are retained.

#### 3. SARC:
   - **Package Generation**: Generate packages through Karen, preparing the mods for distribution and use.

#### 4. General:
   - **Info File Creation**: Generate info.json using user input through Karen, providing essential information and metadata.
   - **Thumbnail Handling**: Copy the thumbnail into the temporary folder for visual identification.
   - **Compression**: Compress files through Karen for efficient storage and distribution.
   - **File Renaming**: Change file extension through Karen, ensuring compatibility and recognition.

## Conclusion

Karen is an integral part of the TKMM software, designed to handle the most challenging aspects of mod merging and packaging. Its optimized code and user-friendly design make it an indispensable tool for a seamless modding experience.

![Karen Diagram](https://github.com/TCML-Team/.github/blob/main/resources/Karen-Diagram.png)


---

# Contributions and Special Thanks

```
Arch Leaders - UI Support + Development, Understanding and Major Help. New BYML Lib, MalsMerger, fixing MessageStudio, being good and genuine.  

Lord Bubbles - RSDB Merger, RSTB Calculator, Feedback, Being Awesome.

Mika - SARC + BYML Merger, Speed.

Aster - Graphic Design, original idea, feedback, fun.

The5thTear - UI, and Tool Dev, Documentation, screaming for help.

Alciel - moderation, beta testing.

Godzilla4 - moderation, beta testing.

mr.the - Beta Testing + Feedback.

Legend5v - Original RSDB-Merger Code.

Watertoon - Documentation.

dt12345 - Extensive Knowledge, TotK Script Repo :).

tom (gamebanana staff) - One-Click Install Support.

xPretorianx - Supporter.

vintii - Supporter.

Mindstormman - Supporter.

King Of The Gnomes - Beta Testing.

Rennai - Affiliation/Promotion.
```

<!--
TODO: Add MIT license?
e.g. https://github.com/ArchLeaders/MalsMerger/blob/master/License.md
-->

<!--[![License](https://img.shields.io/badge/License-MIT-blue.svg)](License.md)-->

*Join our Discord community [here](https://discord.com/invite/w7qGa5RyMc) if you'd like to contribute to the development of **TKMM**. Your insights and collaboration are highly valued!*
