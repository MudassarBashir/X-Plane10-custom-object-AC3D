An experiment to make a custom 3D object for the X-Plane flight simulator world. This would be helpful if making your own scenery package and not just merely placing premade library objects but making your own custom 3D objects to include in your scenery package.

I first created an object using AC3D, I first tried to create something exotic like a cube sitting on top of a sphere (this is why the file name 'CubeAndBall') but texturing that would have been complicated for such a simple proof of concept example so I resorted to modeling the surface of a quarter of a sphere. When I tried to export it using the X-plane obj export plugin, it complained that I must first texture it. This is required for X-Plane.

So, to that end, I then extracted it's surface texture map using the
texture coordinator tool within AC3D. I then opened this mapped texture file in MS Paint by copying it to the clipboard from Ac3D and pasting in MS Paint once it was open and applied some random color to it, some green and some red and saved this as Texture.png. I had to save this as square file (512x512) because otherwise Overlay editor wouldn't read the texture.

Using Overlay editor to place the object at KSEA-Seattle airport didn't work anyway so I used World Editor. It was weird, Overlay editor saw the object but compalined it couldn't find it's texture file which I had placed in the wrong directory. In the object's obj file itself I used the declaration: 

TEXTURE textures/Texture.png

so that it's texture file would be found when I placed the object in the KSEA_DemoArea scenery package and placed it's texture file in the custom scenery package's 'textures' subdirectory. But even when Overlay editor could find the texture it wouldn't let me add the object to the scenery stage. Weird. Bug? So, I decided to give World Editor (WED) a try.


Using WED I was able to place the object on the tarmac behind a large 747 boeing, it just looked like a rock sitting on the ground. But I had proof that I was able to create a custom object and import it into the X-Plane world. A screenshot is included herein.

In this package, the *.ac file is the AC3D file. The *.obj file is the X-Plane plugin's exported obj file. The PNG file is the texture I created to the obj file. This repository is mainly to save the work I did so that if I return to doing this again for a real scenery package, I could remember the procedure of things.

Tools and their versions used.
AC3D 7.0.11
AC3D X-plane export plugin(version 321r2) from X-Plane Developer blog 
X-Plan 10.32 was used.
WED 1.3