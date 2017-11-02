# oomlout-LAZE  
Instructions on how to get files to oomlout for laser cutting. 

## Laser Cutter Details  
Model: HPC Laser 1290 [Buy Online](http://hpclaser.co.uk/index.php?main_page=product_info&cPath=1&products_id=2)  
Cutting Area: 1200 mm x 900 mm (Best to leave a 5cm border to leave room to hold down material)  
	  
## Document Style  
Our laser cutter differentiates between different cut powers/styles by using the objects outline colour.   
	  
* Colour Space: RGB	 
* Fill: None  
* Line Width: Doesn't matter  
* Line Colour: Varies with cut style    
  
### Traditional Cuts
| Cut Type 	| Colour 	| RGB 			| Code		| Cut Order		| Description 				  
| ----		| ----		| ----			| ----		| ----			| ----  
| Cut		| Black		| (0,0,0)		| CUTT-01	| 03			| Simple cut all the way through the material.  
| Etch		| Blue		| (0,0,255)		| ETCH-01	| 02			| Vector etch. (Like a line drawing)  
| Engrave	| Magenta	| (255,0,255) 	| ENGR-01	| 01			| Raster engrave. (Scans the image line by line)  
| No Cut	| Cyan		| (0,255,255) 	| NOCU-01	| 04			| Used for guidelines etc, anything you want in the drawing but don't want the laser to cut.
  
### Special Cuts 
| Cut Type 		| Colour 	| RGB 			| Code		|	Cut Order	|	Description 				 
| ----			| ----		| ----			| ----		| ----			| ----  
| Dashed Cut	| Green		| (0,255,0)		| DASH-01	| 04			| Cuts a dashed line. This means the parts remain in a sheet and can be popped out. Cut and gap distances vary by material.  
| Cut Last		| Red		| (255,0,0)		| LAST-01	| 05			| When not cutting fully closed objects. Use this style to cut last (ie. leave a bounding box until last, or a part that falls out and fouls others)  
| Heavy Engrave	| Pink		| (255,153,204)	| ENGH-01	| 06			| A very deep engrave.
| Start Dashed	| Brown		| (102,51,51)	| STDA-01	| 07			| Start with a space, this can be used to make sure small pieces don't fall through.

## Materials 
Will be filled in with available materials and cut speeds for reference.  
	
## Export Settings
Details on how to export files from various programmes, and list of known issues.   
	  
We bring files into Corel Draw (X4) then export as a dxf. Other direct methods are possible but have their own issues that need figuring out.  
  
#### Illustrator (PDF-Corel-LaserCut)
Publish as PDF. --> (Use 'Press Quality' other versions add compression)
##### Issues
* Patterned brushes do not work.
* Sometimes obejects with white fill are included, these hide lines that the laser will still cut.	

#### Illustrator (Direct)   
1. Create a new file. (Use RGB colour space)  
2. Copy and paste the parts you want to cut.  
3. Expand all text.  
4. Ungroup all expanded text.  
5. Make sure all colours are true RGB values (ie blue 255,0,0)  
6. Export  
  1. File format (Autocad - DXF).
  2. Maximum editability  
  3. Version 2010-2011-2012.  (Or 2004-etc.)  
  4. Units inches.  
  5. Scale factor (1:1) (If using 2004 scale=0.0394 units=0.0394)
  6. Export selected only.


####  Issues
* Text needs to be expanded and ungrouped. Otherwise imports as black only.
* Scaling is an issue. The laser cutter expects inches, and you need to keep a 1:1 ratio when exporting from illustrator.
	
##### Post Processing
* Import into Corel
* Ungroup
* Set fill to none. (often white is used to hide objects)
* Make sure scale looks right and things are nto a miss
* Export as DXF.
	
#### Inkscape (PDF-Corel-LaserCut)
Publish as pdf. 
##### Issues
* Sometimes lines have double start points. This results in the lines being cut twice. (no solution yet)
	
##### Post Processing in Corel
* Import into Corel
* Ungroup
* Select All
* Set fill as None (sometimes lines have fills which results in problems)
* Export as DXF

## Readable File Formats

Corel Draw --> (.cdr) --> upto X4 (14)
Adobe Illustrartor --> (.ai) --> Upto version 10 (Turn off compression)


## Examples
Example template files, and pictures of results to follow.
	