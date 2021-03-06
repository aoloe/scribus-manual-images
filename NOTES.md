# Scribus and images

- Raster and vector images
- Image resolution
- Contour lines and flow of the text around images.
- Using the clipping path
  - <http://wiki.scribus.net/canvas/How_to_Isolate_an_image_and_create_a_clipping_path_for_text_flow>


At this time I have one little but very annoying problem : when I import an image in an image frame it always load with the wrong orientation.  
garryP:  
I'm fairly sure that Scribus ignores any orientation information in the image file and always displays an image - unless you manually rotate it - as though the orientation didn't matter. I've never seen it auto-rotate or ask whether it should. Unfortunately there's nothing you can do about that, at the moment at least.  
There might be some software that can "batch-change" your images prior to putting them in Scribus but you'd have to look for it. (This might be a good place to start: http://www.imagemagick.org/script/command-line-options.php#auto-orient )

jpg oder tiff sind meistens die bessere formate, um bilder in scribus zu laden...

psd könnte funktionieren, ist meistens aber nicht die beste wahl.  
ich sehe grundsätzlich keine vorteile, odg zu gebrauchen

und wie kommen die bilder in einem scribus-dokument?

- bildrahmen zeichnen (ein button dafür gibt's in der toolbar...)
- auf dem bild rechtsklicken
- "Bild laden..."

so sollte es gehen.

ghostscript brauchst du dafür nicht.

## Aligning the images inside of the frame

Generally speaking, it's not a good idea to put images in a frame without filling the whole frame.

The preflight verifier will give you a warning in such cases, because there is a risk that you miss wrong alignments when you start doing so.

The solution to your problem seems to be to slightly change your workflow, resize the frames to their content, and then use the guides and the alignment tool to place your frame.

Of course, through scripting you can get Scribus to help you center the image in the frame. [This one](https://wiki.scribus.net/canvas/Align_an_Image_in_its_Frame) does it, but You will need Tcl/Tk installed (of course it's easy to change the script do only do the image centering without using any dialog).
