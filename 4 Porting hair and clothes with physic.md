Before starting, make sure to have nkk mod inside the mod folder or hair menus will not work. The fastest way to port any hair is to create a vertex group name “hair” and set the weight to 1 for all vertices, then parent it to “COM hair armature” but the hair will be rock hard because it has no physic.

[hair no physic video example](https://mega.nz/file/Z2VR1SDB#tVu-HOZRCsf80nH8VsrWL-nr-c4Zpd5npbsDq0ls6Kw)

To add physic to the hair, or any other piece of clothing, all bones of your model need to be renamed to “yure”, and its head bone (the bone that moves all other bone in pose mode) need to be renamed to “hair_0”. This guide teaches you how to progress with 3 scripts inside the Zoobot workflow.blend. If you want to do it manually, check [this guide](https://github.com/luvoid/COM3D2-All-Bout-Bones/blob/main/wiki/Dynamic-Bones.md)

  ## 1)	physic in clothes

-To add yure physic to clothes:

+ Move all bone out of the first layer, and make sure to deselect all when finished
+ Run ”yure rename” script to rename all bones to yure. Make sure your model still has the modifier with its armature
+ Parent your piece of clothes that needs to add physic to “Spine COM armature” or “Pelvis COM armature”. So the clothes can be stuck to spine or pelvis area
+ Run the “print bone list” script to get the bone list from your model, and delete unnecessary bones by “convert bone clothes” script. 
+ Rename your model mesh inside the blender, so it matches the model files inside COM mod folder
+ Copy the temporary .py files inside :temp/phy and also rename them, so they match the model files inside COM mod folder. Always refresh the mod folder when you add any new file to mod folder


[clothes physic for spine area video example](https://mega.nz/file/g200iQQY#Yvl6eWUqDW4w0JV7bi645vR2-ZZzzbl9RS26w8P8a4M)


## 2)	Physic for hair

In most case, the script ”convert bone hair” are used for convert hair physic. The goal is to rename the Vertex group and its bone with the most weight paint to hair_0 and the rest to yure

<img width="500" alt="image" src="https://github.com/Zoobot123/How-to-port-character-model-to-COM3D2/assets/151656570/f5200495-0a13-4e1b-83e1-729c7e446b2e">

If ”convert bone hair” fails. You can also try ”convert bone clothes” for your hair.

-To add yure physic to hair:

+ Move all bone out of the first layer, and make sure to deselect all when finished
+ Run ”yure rename” script to rename all bones to yure. Make sure your model still has the modifier with its armature
+ Parent your hair to “COM hair armature”
+ Run “print bone list” script to get the bone list from your model, and delete unnecessary bones by “convert bone clothes” script or “convert bone hair”. 
+ Rename your model mesh inside blender, so it matches the model files inside COM mod folder
+ no need to edit the .py 

[hair physic ”convert bone hair” video example](https://mega.nz/file/dn9BRYrS#dq68s_YdJ2mDWsRe1RwG-UdjwS3ykHC5NjxcSY08BCk)

[hair physic ”convert bone clothes” video example](https://mega.nz/file/k7lG1A6B#cG5JHfKK6NgjwzuLBjTSIo5PPgcE-a5lV0KEAIkTiPQ)


## 3)	physic for headdress

Porting headdresses are the same as porting hair because both require to stick in the head, not the body. However, only “convert bone clothes” script will able to handle the jobs.

[hair physic ”convert bone clothes” video example](https://mega.nz/file/k7lG1A6B#cG5JHfKK6NgjwzuLBjTSIo5PPgcE-a5lV0KEAIkTiPQ)
