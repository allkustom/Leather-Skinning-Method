# Leather-Skinning-Method

Unwrap the 3D model's surface with offset(thickness of the leather) for patterning the leather and stitching on the surface.
Also can be used on attaching paper with pattern or graphics on the surface.

## Required Tools
1. Fusion 360 (Can be any other 3D modeling program)
2. Blender
3. [Export Paper Model, Blender Add-on](https://extensions.blender.org/add-ons/export-paper-model/?utm_source=blender-5.0.0)
4. Adobe Illustrator


## Process Order, Brief
1. Apply stitch hole on the model
2. Offset surface with the thickness of leather
3. Export the offset surface as an OBJ and import into Blender
4. Enter Edit mode and mark Seam
5. Unfold via 'Export Paper Model' and export as SVG
6. Clean up SVG via Adobe Illustrator
7. Insert SVG on the Fusion 360 sketch
8. Use template and stitch

---

# Process Order, Detail
## 1. Apply Stitch hole on the model

Craete the model in Fusion 360.
(Below it the sample model with curves)
![Fusion Base Model](/0%20assets/fusion%20base%20model.png)


Create stitch hole on the model with 45 degree angle.
And apply path following pattern with least 2mm distance between each holes.
*[!] For the paper attaching, doesn't need to apply stitch holes*

![Fusion Hole](/0%20assets/fusion%20hole.png)
![Fusion Hole Pattern](/0%20assets/fusion%20hole%20pattern.png)

And add marks for the seam for the later unfolding process.
In my case, I add small triangles.
![Fusion Mark](/0%20assets/fusion%20mark.png)

## 2. Offset Surface
Apply 'Offset Surface' on the surface which you want to skin the leather.
Offset amount has to be same or 10% less than the thickness of the leather.
In my case, I used 1.5T leather.
![Fusion Offset](/0%20assets/fusion%20offset.png)

*[!] For the paper attaching, set the offset with the thickness of the paper*


## 3. Export Offset and Import
Export the offset surface as OBJ.
![Fusion Export](/0%20assets/fusion%20export.png)

Depends on the complexity of the surface mesh, adjust the export quality options.
![Fusion Export Setting](/0%20assets/fusion%20export%20setting.png)

And import exported OBJ into Blender
![Blender Import](/0%20assets/blender%20import.png)

## 4. Enter Edit mode and mark Seam

Imported OBJ's mesh must be unclean and tangled.
Just enter the edit mode and use 'kinfe tool'(Shortcut K) to make seam line.
Previous triangle marks I applied on Fusion 360 used on this stage to snap the kinfe tool.
![Blender Seam](/0%20assets/blender%20seam.png)

## 5. Unfold via 'Export Paper Model' and export as SVG

Install [Export Paper Model](https://extensions.blender.org/add-ons/export-paper-model/?utm_source=blender-5.0.0) add-on and activate it.
You can enter Edit mode to mark seam via this add-on. (Can be done via right-click and select Mark Seam)

![Blender Addon](/0%20assets/blender%20addon.png)

Click 'Unfold' and click 'Export Paper Model'. (Depends on the complexity of the mesh, both might takes few minutes. Be patient)


Keep the Model Scale as '1.0'.
Paper size setting has to be bigger than the unfolded mesh, but doesn't have to be accurately fit. 

We will use only SVG later.
But if the paper size is smaller than the unfolded mesh, exporting fails.

![Blender Export](/0%20assets/blender%20export.png)


Change the below setting
1. **Format:** SVG
2. **Tabs:** None
3. **Numbers:** None

Then export SVG

![Blender Export Details](/0%20assets/blender%20export%20detail.png)


## 6. Clean up SVG via Adobe Illustrator

Import SVG into Adobe Illustrator. (Can be any software which can edit SVG as a vector file)

![Illust Import](/0%20assets/illust%20import.png)

Patterns on SVG are grouped and compounded. Double-click the object several times to enter the individual vector mode.

Now you can delet unwanted vectors.
Make sure to clean it up, so make extruding in Fusion 360 can be easy.

![Illust Individual](/0%20assets/illust%20individual.png)

![Illust Clean up](/0%20assets/illust%20clean%20up.png)

## 7. Insert SVG on the Fusion 360 sketch

Fusion 360, 'Insert SVG' on the new component.
Apply some offset on the outline.

![Fusion2 insert](/0%20assets/fusion2%20inser%20svg.png)

Extrude the parts which needs to be marked on the leather as a 3D printed template.

![Template](/0%20assets/fusion2%20extrude.png)

## 8. Use template and stitch

3D print the template, fix on the leather with the masking tape, and apply some presure(I used hammer) to mark it on the leather.

Then, cut and punch the leather.
3D printed template is only for marking, not punching.

![Leather](/0%20assets/result%20template.jpg)

Stitch the leather on the 3D printed model(with stitch holes).

![Result1](/0%20assets/result%201.JPG)
![Result2](/0%20assets/result%202.JPG)

---

Below is the example of paper attaching.

You can just print directly from SVG. With some patterns and graphics.

![Paper1](/0%20assets/paper%201.JPG)
![Paper2](/0%20assets/paper%202.JPG)
![Paper3](/0%20assets/paper%203.JPG)