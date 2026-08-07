# Ex.No: 6  Implementation of Jumping  behaviour- Unity
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
To write a program to simulate the process of jumping in Unity.
### Algorithm:
```
1. Create a new 3D Unity project
2. Add a Plane
3. Right-click Hierarchy → 3D Object → Plane → Rename to Ground
4. Add a Cube (Player)
5. Right-click Hierarchy → 3D Object → Cube → Rename to Player
6. Set Position: (0, 0.5, 0)
7. Add a Rigidbody to the Player
8. With the Player selected: Inspector → Add Component → Rigidbody
9. Set Constraints > Freeze Rotation X, Z (optional for stability)
10.Create the Jump Script and Apply the Script Player
11.Run the game
Press Play
Press Spacebar to jump
Your cube should only jump when touching the ground
```
###
**Program **
```
using UnityEngine;

public class PlayerJump : MonoBehaviour
{
    private Rigidbody rb;
    public float jumpForce = 5f;
    
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space) )
        {
            rb.AddForce(Vector3.up * jumpForce, ForceMode.Impulse);
            
        }
    }

   
}
```
### Output:
<img width="1261" height="710" alt="Screenshot 2026-08-07 140306" src="https://github.com/user-attachments/assets/af6e9cf5-b9a4-47a6-bcb3-3bfb53ad1fc4" />
<img width="1265" height="670" alt="Screenshot 2026-08-07 140318" src="https://github.com/user-attachments/assets/c3639cd8-5f21-48ac-8483-475d40d3a43e" />









### Result:
Thus the simple jumping behavior was implemented successfully.
