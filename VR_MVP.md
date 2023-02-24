# VR MVP
As of Unity 2021.3.10f1, here are the minimum requirements to get Head and Hand tracking setup in VR, with a PC-connected Oculus Quest CV1.

1. Using the Unity Package Manager (UPM), download Unity's VR Feature, which includes two packages:
  - Oculus XR Plugin
  - OpenXR Plugin

![image](https://user-images.githubusercontent.com/8541667/220855089-405d779a-73a8-4d75-9e62-a062cd20dd92.png)
    
2. In `Player Settings > XR Plug-in Management`, enable `OpenXR` for PC standalone builds.

![image](https://user-images.githubusercontent.com/8541667/220855794-5d6e032d-1ce2-4617-a6fc-60fc055e3751.png)

3. In `Player Settings > XR Plug-in Management > OpenXR > Interaction Profiles`, click the `+` to add a new interaction profile and select `Oculus Touch Controller Profile`:

![image](https://user-images.githubusercontent.com/8541667/220855880-77d7640f-051f-421f-bdf4-c86b53d1e610.png)

4. Using the UPM, download the "XR Interaction Toolkit"

5. In a new scene, right-click the `Hierarchy` and create `XR > XR Origin (Action-based)`

![image](https://user-images.githubusercontent.com/8541667/220856537-88dd392f-f755-4cbd-af05-d63fd8ebf30c.png)

6. In the UPM, select the "XR Interaction Toolkit", expand the `Samples` tab, and Import the "Starter Assets".
7. From your Project panel, navigate to `Assets/Samples/XR Interaction Toolkit/<version>/Starter Assets/XRI Default Input Actions`
8. In the Hierarchy panel, select the newly created "XR Origin". Then, from the Inspector, navigate to the `Input Action Manager` component. 
9. Increase the `ActionAssets` array size to `1`, then drag+drop the `XRI Default Input Actions` component into this new entry

![image](https://user-images.githubusercontent.com/8541667/220859011-eda4899e-72ce-4d2a-83e8-535756835133.png)

10. In the Hierarchy panel, expand down to `XR Origin > Camera Offset > LeftHand Controller` and select. Right-click the `XR Controller (Action-based)` component, and select `Remove Component`. Do the same for `XR Origin > Camera  Offset > RightHand Controller`

![image](https://user-images.githubusercontent.com/8541667/220864294-1d248b13-c05f-4074-a51a-507939b34c6d.png)

11. From your Project panel, navigate to `Assets/Samples/XR Interaction Toolkit/<version>/Starter Assets/XRI Default Left Controller`. Drag+drop this asset into the Hierarchy panel, `XR Origin > Camera Offset > LeftHand Controller`
12. Do the same with `Assets/.../XRI Default Right Controller` and `XR Origin > Camera Offset > RightHand Controller`

![image](https://user-images.githubusercontent.com/8541667/220862460-ad61d6d4-c581-4d04-9786-a463b6906d93.png)

13. Press Play! Your head and hands in the Sample Scene should track with the HMD and controllers

