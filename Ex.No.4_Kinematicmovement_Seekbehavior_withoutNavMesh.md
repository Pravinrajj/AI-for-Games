# Ex.No: 4  Implementation of Kinematic movement -seek behavior in Unity
### DATE:                                                                            
### REGISTER NUMBER : 212222240080
### AIM: 
To write a program to simulate the process of seek behavior in Unity without NavigationMeshAgent. 
### Algorithm:
1. Create a New Unity Project by Open the  Unity Hub and create a new 3D Project,Name the project (e.g., SeekBehaviorDemo).
2. Create the Moving Object
   In the Hierarchy, right-click → 3D Object → Cube (or Sphere).
   Rename it to Seeker and Reset its position:Select the Seeker, go to Inspector → Transform → Set Position to (0,0,0).
3. Create the Target Object
   Right-click in the Hierarchy → 3D Object → Sphere (or any other shape).
   Rename it to Target. Move it away from Seeker, e.g., set Position to (5, 0, 5).
   Select the Target, add a Material, and change the color. (if needed) 
4. Adding the Seek Behavior Script
   Create the Script-In the Project Window, go to the Assets folder.
   Right-click → Create → C# Script.
5. Write a script for seek behavior and save it
6. Attach the Script
   Select Seeker in the Hierarchy - Drag & Drop the SeekBehavior script onto the Inspector Panel.
   Drag & Drop the Target from the Hierarchy into the "Target" field in the script component.
12. Run the game 
13. Stop the program
    
### Program:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Script : MonoBehaviour
{
    // Start is called before the first frame update
    public Transform target;  // The object to seek
    public float speed = 5f;  // Movement speed
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        if (target == null) return;  // Exit if no target is assigned

        // Calculate the desired direction
        Vector3 direction = (target.position - transform.position).normalized;

        // Move the object towards the target
        transform.position += direction * speed * Time.deltaTime;
    }
}
```
### Output:
![423383693-eaa695c2-16eb-4fbf-a4be-0a7fac41be1b](https://github.com/user-attachments/assets/58ff4268-0236-43f9-b579-2a4b8e56f8c8)
![423383738-fd4fcb60-2da3-416e-946c-c43d366d42ae](https://github.com/user-attachments/assets/3f69a374-8010-488e-bbe9-bf170fa26f1b)
![423383788-98453693-1187-40c0-ad84-a604332389fb](https://github.com/user-attachments/assets/b0fe61b3-d5aa-4b65-8ca7-e00a21c73abe)
![Uploading 423383874-b13eabc2-5dd7-49d2-9a1e-f1501a9c54ac.png…]()


### Result:
Thus the simple seek behavior was implemented successfully.
