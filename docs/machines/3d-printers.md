### Moving forward, all g-code files for printing at Seattle Makers will be created using PrusaSlicer.

##### **Awesome reasons for the change:**

- You can test slicing (preparing prints) files at home.

- It's free.

- Competitive feature-wise as compared to Simplify3D.

- If you slice on-site on your laptop, you can wirelessly send print jobs to the printers. No touching of SD cards or the public computer.

ℹ️ **Note**: You may need to be re-certified, but many of the lessons
you've learned about our previous printers will still be relevant.
Printing will be easier than ever before. If needed, Simply3D is still
on the computer here at the space, but it will not be the preferred
method.

* * * * *

# **First Time Setting up PrusaSlicer** 

## **PrusaSlicer Software** 

![View of PrusaSlicer](https://seattlemakers.org/wp-content/uploads/2020/08/2020-08-08_14-48-53.png)

## [Download PrusaSlicer software here.](https://www.prusa3d.com/prusaslicer/)

This link will take you to the Prusa Website to download the correct version for your operating system 

**If you're new to PrusaSlicer,** [check out their awesome documentation for getting started.](https://help.prusa3d.com/en/article/first-print-with-prusaslicer_1753) We also cover how to use it in our 3D Printer certification course.  

### **Setting up Printer Profiles & Settings**

Our Prusa MK3s printers are stock, so using the default profiles that come with PrusaSlicer should work fine. However, we also have some non-Prusa printers that have some specialized profiles. Franklin, our large format printer, is one example. We have our profiles online for download, so you can install them for your use.

## [Download our custom profiles for our other printers here.](https://github.com/dorfman2/SeattleMakersPrinterProfiles/archive/master.zip)

- Unzip the file
- Open PrusaSlicer and click on `File => Import => Import Config Bundle`.
- Select the file `SeattleMakers_config_bundle.ini` to import all the profiles for our printers.
- If they import successfully, congratulations!

![Import Config Bundles](https://seattlemakers.org/wp-content/uploads/2020/08/2020-08-08_14-50-12.png)

* * * * *

# **How to Print!**

## 1. Slice Your File

To ensure that our printers continue to operate at peak efficiency please use our [profiles](https://github.com/dorfman2/SeattleMakersPrinterProfiles).

#### Default Printer Profiles & Setting 

These are the recommended starting settings for our printers.

ℹ️ **Note**: The rest of this sections assumes you have installed our profiles. Please see above for instructions on installing our printer profiles. 

**Jinja & Ada**- Prusa MK3s

    Print Settings: 0.20mm QUALITY
    Filament: eSun PLA+
    Printer: Original Prusa i3 MK3S - Jinja

**Franklin**- FolgerTech FT5

    Print Settings: 0.20mm Layer - Franklin
    Filament: eSun PLA+ - Franklin
    Printer: Folger FT5 - 0.6 Nozzle - Franklin

**Sawyer** - Duplicator i3 (Prusa MK3S Extruder)

    Print Settings: 0.20mm SPEED - Sawyer
    Filament: eSun PLA+ - Sawyer
    Printer: Duplicator i3 - 0.4 Nozzle - Sawyer

  After choosing the preferred settings in PrusaSlicer:

-   Import your model (STL, OBJ, AMF, 3MF)
-   Arrange on build plate
-   Make necessary changes to layer height or other settings.
-   Slice your file
-   Repeat as necessary

**ℹ️ Note**: If you need to make any changes to your object or slicer
settings after slicing, use these buttons to switch between views in
order to do so.  

## 2. Prepare The Printer

1. Check the printer bed for previous print, please ask a Maketeer or the printing member if a print is complete to remove it from the bed. Please don't be responsible for breaking someone elses' print.
1. Clean/Prepare the bed
    1. Ensure the bed is clear of debris
    1. Wipe the bed down with the microfiber cloth and glass cleaner/isopropyl alcohol
1. Ensure filament is loaded and is the correct color
    1. To Un-Load Filament
        1. Using the wheel on the printer, navigate to "Un-Load
            Filament"
        1. It will ask for filament type, choose PLA
        1. Wait for the printer to heat up.
        1. Press the Button to unload (Franklin will unload automatically when it reaches temp)
        1. Remove roll carefully, ensuring it doesn't become unwound.
        1. Clip off the very end of the filament to remove the blob.
    1. To Load Filament
        1. Place roll of filament on printer
        1. Clip off the very end of the filament is there is a blob.
        1. Insert filament into extruder head
        1. For Prusa
            - It will detect there is filament.
        1. For Franklin
            - Using the wheel on the printer, navigate to "Load Filament"
        1. It will ask for filament type, choose PLA
        1. Wait for the printer to heat up.
        1. Press the Button to load (Franklin will load automatically when it reaches temp)
        1. If filament is flowing correctly
            - For Prusa: *Extruding Correctly?* Yes
            - For Franklin: *Continue Purge?* No
        1. Remove extruded filament from nozzle.

## 3. Send G-Code To Printer (Start Printer)

**No longer will you have to transfer your files to an SD card,** and then manually insert the card into the printer. Using a raspberry pi and a program called [OctoPrint](https://octoprint.org/), we now can send our G-Code directly from the slicer or web interface to the printer. 

ℹ️ **Note**: If you are having trouble with an Octoprint Interface, please ask a Maketeer. SD cards can be used as a backup, but please defer to them to make that determination.

### There are **two** ways to send your print.

#### Directly from PrusaSlice 

This requires you to install an API Key in PrusaSlicer. Please contact Jeff on Slack (@Jeff) to get the API key. This allows you to send files to OctoPrint and start your print without using the web browser. After you've finished slicing:

1. Double check you have the correct printer.
2. Click the tiny button in the lower right corner "G\>."

![](https://seattlemakers.org/wp-content/uploads/2020/08/2020-08-08_15-43-42.png)

3. If desired, check "Start Printing after upload."
4. Click "OK."

![Print Click "OK"](https://seattlemakers.org/wp-content/uploads/2020/08/2020-08-08_15-47-07.png)

#### Upload via web browser (When on-site)

After you've finished slicing:

1. Export your sliced file to the desktop.
2. Ensure you're on Seattle Makers Wifi.
3. Open a web browser and travel to Octoprint page.
    -   Convention for webpage is **http://octopi*{name of printer}*.local/** (example: [http://octopifranklin.local/](http://octopifranklin.local/) allows you to get to Printer "Franklin")
4. Login to OctoPrint (case sensitive).
    -   Login: **member**
    -   Pass: **letsprint**
5. Drag your file onto the OctoPrint web page. The page will change while dragging, and aim for the left side where it says "Upload Locally."

![OctoPrint Upload](https://seattlemakers.org/wp-content/uploads/2020/08/2020-08-08_16-09-48.png)

6. Check the name to make sure it's your file, and click the print icon
    on your Print!
    -   If it's helpful, you can click the small wrench to change to
        "sort by upload date."

![Octoprint start print](https://seattlemakers.org/wp-content/uploads/2020/08/2020-08-08_16-13-10.png)

* * * * *

How to Install the OctoPrint API' 
----------------------------------

(Coming Soon)
