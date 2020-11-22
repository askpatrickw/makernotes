# Wood CNC Mill

![Seattle Makers Shapeoko CNC](../static/img/cnc-mill/seattlemakers_shapeoko.png)

## Make & model

[![Carbide 3D Logo](../static/img/cnc-mill/carbide3D.png)  
Carbid3D Shapeoko CNC](https://carbide3d.com/shapeoko/)

- [GRBL Controller](https://docs.carbide3d.com/shapeoko-faq/controller-firmware-information/)
- [T-Track and Clamp Modification](https://shop.carbide3d.com/collections/accessories/products/t-track-table?variant=5175720706078)
- [Z-Plus Upgrade](https://shop.carbide3d.com/collections/accessories/products/shapeoko-z-plus?variant=31524471144509)

Size:

- 30in x 30in bed (762 mm x 762mm)
- Max material thickness: 2.5″ (63.5mm)
- Max cut thickness: up to 2.5″(63.5mm), varies by router bit

What it can do: 

- Subtractive manufacturing
- Engraving
- Sign making
- Furniture prototyping

## Materials

### Allowed

- Wood: MDF, plywood, regular wood
- Polycarbonate (with special bit)

### Disallowed Materials

- Metal
- glass

## Usage Rules

Certification: [Vectric VCarve Pro design class](https://seattlemakers.org/catalog#vcarve) and [CNC-Mill machine certification](https://seattlemakers.org/catalog#CNCcert) are both required in order to use the machine solo.  
File type: .svg, .dxf

## Pricing

Time on this machine will be charged in 30-minute increments. [Buy time](https://seattlemakers.org/store/items/machine-time/) and [schedule time](https://seattlemakers.org/schedule/) on the Seattle Makers website.

## Designing and Milling your project

Seattle Makers uses [Vectric's VCarve Pro](https://www.vectric.com/products/vcarve-pro) for designing and generating the g-code for you project 
![VCarce Logo](../static/img/cnc-mill/vcarve_pro.png)
> Note: VCarve only runs on Windows.

> NOTE: You will be able use the Trial version of VCarve indefinitely for your designs when you have completed the certification.

[CNCJS](https://cnc.js.org/) is used for controlling the Shapeoko based on the g-code created in VCarve.
![CNCJS Bannner](../static/img/cnc-mill/cncjs.png)

### VCarve Designing

**Job Setup**
Assuming a Single Sided project or "Job Type" as it is called in VCarve:
- Configure your job Size dimensions: width (x axis), length (y axis) and your material thickness.
- Set Z Zero Position to be Material Surface
- Set Datum Position to be Material Surface  
![VCArve Job Setup](../static/img/cnc-mill/vcarve_job_setup.png)

**Draw your Project**

In your Vcarve Class, you will learn how to make a basic design. We won't go into too much more about that here. See the Additional Resources for links to more tutorials, especially the Vectric YouTube channel.

**Specify Toolpaths**

For each element of your design, you need to specify the bit (tool) and any other parameters for its cutting process.

### VCarve Tips

- **Tabs**
    - If you're cutting through your material with this tool path, you need to add the through cut amount back to your tabs. For example: If your cutting to a depth of 15mm to cut all the way through your 12 mm material, you should add those 3mm back to your tabs. So a 9mm thick tab would actualy be 6mm. 
    - Use 3-D Tabs as a preferred setting.
- **Profile Toolpaths**:
    - Enable Add Ramps to toolpaths to prevent burning of your material where the bit plunges repeatedly
    - To leave some material for sandig or other finishing work, you can use the offset allownce in the Machine Vectors.
    - When setting up a profile toolpath, also select "Seperate Last Pass" to get a better final cut quality.
        - The last pass will remove your material allowance if you don't also have and allowance on the last pass as well.
    
- **3-D or Toolpath Preview**: 
    - If the preview doesn't look like you expect, click "Reset Preview" and then replay the preview.
- **2D Toolpath alignment**:
    - Show your toolpaths and be sure they are properly lined up (on top of your drawing). If not re-calculate your toolpaths to align your toolpaths with any design changes you've made. In this example you can see the toolpath for "Door" is below where it should be. As opposed to the pefectly aligned toolpath for the circle below it.  
![2D Toolpath Alignment](../static/img/cnc-mill/2d_toolpath_alignment.png)

### Bits

There are 1/4" End Mills and 1/2" 90 Degree V-Bits for general use at Seattle Makers.

For higher quality cuts and speciality bits, [McMaster-Carr is a great sours of router bits](https://www.mcmaster.com/standard-router-tools).

> Note: The Shapeoko will accept 1/4" or 1/8" shank bits.

## Additional Resources

**Software**
- [Vectric VCarve Pro ](https://www.vectric.com/products/vcarve-pro) Product Site
- [Vectric's YouTube Channel](https://www.youtube.com/user/Vectric)
- [CNCJS](https://cnc.js.org/) Project Site 
- [CNCJS Documentation](https://cnc.js.org/docs/)
- [Demonstration of different router bits](https://www.youtube.com/watch?v=2FjXsZKrobQ)
