# laser Cutter

Things you should know about the Laser Cutter.

## Make and Model
There are two [Black Cat Labs 90 Watt CO2 Lasers](https://www.blackcatlabs.xyz/laser-cutters) at Seattle Makers.
They use an Ruida controller and [Lightburn Software](https://lightburnsoftware.com/) to control.

![Light Burn Software](static/img/Title_LightBurn_360x.jpg)

## Materials

- Max material size: 20.75″x33.75″ (53cm x 86cm)
- Max design size: 20.25″x33.25″ (52cm x 85cm)
- Max cut thickness: 1/4”
- Engraving Max material thickness: 8”

### Allowed Materials
 
- Cut: acrylic, wood, paper, leather, some plastics, some foams
- Engrave / etch: the materials above plus glass, anodized aluminum
- [Full list of laserable materials](static/files/Laser-cut-and-dont-cut-materials-list.pdf) (list courtesy of ATX Makerspace)

### Disallowed Materials
You may hurt yourself, the machine, our just ruin your materials.

- Can’t cut: polycarbonate, metal, glass, PVC, most plastics
- [Full list of non-laserable materials](static/files/Laser-cut-and-dont-cut-materials-list.pdf) (list courtesy of ATX Makerspace)


## Usage Rules

1. You must have completed the [Laser Certification class](https://seattlemakers.org/catalog#lasercert).
1. Safety Procedures
    - Make note of the nearest fire extinguisher.
    - Small Fire: If your material starts burning, press pause and move the laser away from the area. It will usually go out on its own. You can then press resume to continue your cut.
    - Large Fire or other OMG.Situation.. hit the big red button.

## Pricing

Laser cutter time is charged in 15-minute increments.
[Buy time](https://seattlemakers.org/store/time-laser/) and [schedule time](https://seattlemakers.org/schedule/#lasers) on our website.

## How-To's Tips and Tricks

### Designing your project

A Laser uses 2D graphics files (as opposed to a 3D CAD file) as the information to control the machine. In the certification class you will learn to use LigthBurn to make a design. You can also use other software, as long as those programs can create SVG, DXG or AI files.

> Supported File types: .svg, .dxf, .ai files (Adobe Illustrator – but only files with ONE artboard)

You can design on the PCs at Seattle Makers or at home on your own computer. Assuming you design at home, once you're done, you will bring the file to the lab on a USB drive or email it to the lab. 

### Step By Step Process

#### Material Setup

1. You should use "masked" materials to get the highest quality output for your projects. The masking is a paper covering on the material which protects the material from smoke damage during the cutting process. This is true for woods and plastics.
1. Secure your material in the machine using the hold-downs supplied at Seattle Makers.

#### Machine Setup

1. Open Lightburn on the on the Laser Cutter's PC and **Import** the file from your USB Drive.
1. Check that your file looks as you expect.
1. Zero the Laser
1. Home the Laser
1. Check for Laser Gnomes
1. 


### Additional Resources

 - The Seattle Makers Slack has a Laser-Cutter channel. Stop on by for help or to help others.
 - [LightBurn Software YouTube Channel](https://www.youtube.com/c/LightBurnSoftware/playlists) has tutorials and demos.
 - [Boxes.py](https://festi.info/boxes.py/) is an Online and Open Source box generator written in Python.
 - [MakeABox.io](https://makeabox.io/) is an Online front end to the [laser-cutter Ruby gem](https://github.com/kigster/laser-cutter)
 - [MakerCase](https://www.makercase.com) is a web-based application for designing boxes or project cases for laser cutters and CNC routers. 
