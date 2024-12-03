---
layout: page
title: DnD5e Conversion Tutorial
permalink: /documentation/conversion-tutorial
---

This tutorial will walk you though the process of converting several DnD5e compendiums in depth. In this example we will be bringing the classes, equipment, and spells from the DnD5e SRD into Black Flag.

The conversion is handled by the [Black Flag Roleplaying Content Tools](https://github.com/koboldpress/black-flag-tools) module. Follow the instructions on the module's page to install it before continuing.

### 1. Set up Environment

The first step is preparing everything for conversion. Ensure you have the latest version of the DnD5e and Black Flag systems installed as well as the latest version of this module. You will also need to set up a series of compendiums to receive the content. Compendiums can be in either the world or a module, but in this case the instructions assume you are using a custom module to hold the converted content. Follow the [Module Maker instructions](https://foundryvtt.com/article/module-maker/) on the Foundry site for information on this general process.

For this conversion I have created three compendiums within a newly created module. One will contain the classes, subclasses, and class features, a second will contain the equipment, and a third for the spells:

![](assets/images/conversion/compendium-setup.jpg)

You will also need to have a DnD5e world and a Black Flag world set up with the "Black Flag Roleplaying Conversion Tools" module enabled in both.

### 2. Export from DnD5e

Next you will want to head into the DnD5e world to export and convert the content. In the Compendium Packs sidebar locate the compendiums you wish to export, in this case "Classes (SRD)", "Subclasses (SRD)", "Class & Subclass Features (SRD)", "Items (SRD)", and "Spells (SRD)". Right click on each of these packs and select "Export for Black Flag":

![](assets/images/conversion/sidebar-export-for-black-flag.jpg)

This will convert the contents of the compendium to Black Flag data and download a `.json` file for each pack. For larger compendiums such as the "Items (SRD)" pack this may take some time, so be patient for it to complete. Once you have repeated this process for all of the packs, you should find several `.json` files in your computer's downloads folder:

![](assets/images/conversion/exported-json.jpg)

### 3. Import into Black Flag

Now head over to the Black Flag world to import the content. In the Compendium Packs sidebar locate the compendium you wish to begin with, in this case the "D&D SRD Classes" compendium created in the custom module. Right click on that compendium and select "Import from DnD5e":

![](assets/images/conversion/sidebar-import-from-dnd5e.jpg)

This will bring up a file selection window. Use this window to select the first of the `.json` files from your downloads folder that you wish to import into this compendium:

![](assets/images/conversion/file-selection-dialog.jpg)

Once you hit "Import", a new dialog will pop up with a summary of how many documents were found, an import button, and potentially some additional options:

![](assets/images/conversion/importer-classes.jpg)

The options under the "Compendium Pack Remapping" header allow automatically changing links from the old compendium packs to new ones. Each of the listings has a name for a specific dnd5e pack, in this case `dnd5e.classfeatures` for the "Class Features (SRD)" compendium, `dnd5e.subclasses` for the "Subclasses (SRD)" compendium, and `dnd5e.rules` for the "Rules (SRD)" compendium.

The drop down on the right includes a list of all packs available in the current world. Selecting a pack here will cause any UUIDs used within the imported items to be replaced with references to the specified pack:

![](assets/images/conversion/pack-remapping-dropdown.jpg)

Since we have created a single compendium for storing classes, subclasses, and their features, the dropdowns for `dnd5e.classfeatures` and `dnd5e.subclasses` should be changed to point to the new "D&D SRD Classes" compendium:

![](assets/images/conversion/pack-remapping-complete.jpg)

Once all of these fields have been set, click the "Import Documents" button to complete the process. Again this may take some time to create all the documents, especially for larger compendiums like "Items (SRD)" which contains hundreds of documents to import.

When the importing is complete, repeat the process with all the other `.json` files exported earlier. Each file may have slightly different options for the pack remapping, such as these for the "Class && Subclass Features (SRD)" compendium:

![](assets/images/conversion/importer-class-features.jpg)

### 4. Enjoy

Now everything should be fully imported over! Note that the importer will try its best, but certain things might need manual adjustment. Its always a good idea to give you newly imported content a review to ensure everything is set up how you like it. If anything seems to have obviously imported incorrectly, feel free to file an issue on the [bug tracker](https://github.com/koboldpress/black-flag-tools/issues).

![](assets/images/conversion/imported-content.jpg)
