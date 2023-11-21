1) Required files
   
Basic COM modding requires having menu, model, and tex files inside your mod folder
 + Model is the files you export your model from blender
 + Tex are the files converted from diffuse texture files. Converting by texttool.exe
 + Menu are txt files provided inside temp folder found in Zoobot's modding tools. Those .txt files need to be converted to .menu by [CM3D2]menu←→txt Converter.exe

2) Requirements for exporting your model from Blender-CM3D2-Converter
   
If get any error before exporting your model to COM from Blender, check if you meet all the requirements listed below:
+ Convert all material to COM material
+ Apply all transforms (ctr+A > All transforms) to your model AND its armature
+ Apply all modifiers, only keep COM armature modifier
+ Make sure to parent your model to COM armature
+ Unhide your model’s armature before export
+ For armature inside zoobot workflow.blend, always pick export as Armature, not as Armature data. Also Type "Auto" in based bone
<img width="500" alt="image" src="https://github.com/Zoobot123/How-to-port-character-model-to-COM3D2/assets/151656570/3831d5d2-43fa-41b2-8e24-a9a449bdb0cd">

