
# Ex06-Redirecting-the-Scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
Step 1:
To open the unity engine.

Step 2:
Create a new 3D project.

Step 3:
Create plane and name it as ground and create cube and name it as player.

Step 4:
Add WinText in Hierarchy.

Step 5:
Create a C# Script and name it as playercontroller and add the script to player.

Step 6:
Use the R button to change the level2

Step 7
Print the Output and end the program.

## Program:

```
Developed by : G.Jayanth.
Reg no :212221230030.

```

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;


public class PlayerController : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinTXT;
    // Start is called before the first frame update
    void Start()
    {
        rb=GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.W))
        {
            SceneManager.LoadScene("Level2");
        }
    }
    private void OnCollisionEnter(Collision Other)
    {
        if (Other.gameObject.tag=="Destroy")
        {
            Destroy(Other.gameObject);
            WinTXT.SetActive(true);
        }
    }
}
```

## Output:
#### Mini Game
![image](https://github.com/JayanthYadav123/Ex06-Redirecting-the-Scene/assets/94836154/0f924d5e-00eb-4744-9e77-9435c691e84c)

#### lEVEL 2
![image](https://github.com/JayanthYadav123/Ex06-Redirecting-the-Scene/assets/94836154/f8465921-7303-4d14-b0af-4e0deeacc2d7)

## Result:

The above C# coding is successfully redirecting the scene in the unity engine.
