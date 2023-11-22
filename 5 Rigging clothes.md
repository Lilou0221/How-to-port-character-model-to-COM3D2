
## 1) Transfer weight paint and shape key

Welcome to the hardest part in character porting - transfer weight paint from COM body to your model. The progress requires resizing both COM body and your model as closely as possible, so we can get the best result from “high precision weight transfer” from CM3D2-Converter. After weight transfer, your model will automatically follow COM body movement.
My recommended method is to pose your model’s armature and sculpt your model to fit the COM body. Of course, this method require your model to have a working armature and a little bit of knowledge with sculpting. 

Basic workflow:
+ Resize your model to somewhat match the COM body
+ Posing 2 arms to T pose to match the COM body. Run “fix mirror mmd” to fix mirroring issues between 2 arms. Keeping in mind that this script only works for mmd armature
+ Use Sculpt brushes to sculpt the rest until your model completely fits COM body. The only 2 brushes you will need are elactric deform and draw brushes. Keep in mind you don’t have to sculpt the area that can be hidden by node hiding
+ When you make sure your model fits COM body, use “high predict vertex group transfer” to transfer weight paint from COM body to your model
+ The next step is to transfer the shape key from COM body to your model. Consider increasing the poly in the chest area by subdivision to avoid clipping in munel shape key
+ Apply armature modifier from your model to COM body’s armature, so you can pose your model by COM body’s armature
+ switch COM body back to its original pose. At this point, both of your model and COM body should switch to squat pose
+ your model should be ready to export to COM. Remember to check the Requirements for exporting the model before exporting 
+ the COM body was LOhighpoly body V2, so you need to equipped that body inside the game or clothes will have small clipping. Test your model inside the game and come to fix any clipping
  
[rig body video example](https://mega.nz/file/CL5yWTaY#2PdIf9Yv6lrl4hx1HcdMD_RI0Hg85VHpNfravaowQOA)



[For more sculpting tutorial watch from 10:03](https://www.youtube.com/watch?v=62k9seQdARA&ab_channel=TomCAT-Characters%2CArtandTutorials)


## 2) Rigging a skirt

Normally, you need to split the skirt from your model and transfer weight paint from a similar skirt from COM. The progress is easy if you have a completely separate skirt like in the picture

<img width="500" alt="image" src="https://github.com/Zoobot123/How-to-port-character-model-to-COM3D2/assets/151656570/426593fc-eb3d-4fde-8622-fa307341966b">

However, rigging a skirt that completely merges with the top like Nahida or Lisa's skirts is a different story. You are likely will have a lot of clipping issues in the pelvis area


<img width="300" alt="image" src="https://github.com/Zoobot123/How-to-port-character-model-to-COM3D2/assets/151656570/69989982-3e6a-4f83-b691-ad89924f1665">

Luckily, I came up with a method to help you cheese the skirts like Nahida or Lisa. This method will transfer the weight paint to the top and the skirt at the same time.

To rig any skirt:
+ Unhide Rigged skirt collection, and move your model to that collection
+ Pick one of 3 skirt bodies that are similar in size to your model provided inside Zoobot workflow.blend. Those are named “small skirt body”, “medium skirt body”, and “big skirt body”. I will use “medium skirt body” for example
+ split any pants, stock, or shoes from your model, and save them somewhere. You will have to rig them later
+ sculpt your model to fit “medium skirt body”. The skirt area doesn’t need to be perfectly aligned
+ transfer weight paint and shape key
+ Parent your model to “COM body armature”, so you can switch your model to a squat pose. Again, Parent your model to “COM body armature”, not “medium skirt body’s armature”. 
+ After successful switch your model to squat pose. You can parent your model to “medium skirt body’s armature” now. Remember to force apply any modifier on your model before export.

[rig medium skirt example](https://mega.nz/file/DfIyySrD#eNh9Z6u1soSjjCzuzMRcp1yZ6pE48ECRyjS1XDNK7DI)
