# Ex06-Redirecting-the-Scene

## Aim:
To Redirecting the scene in the unity engine.
## Algorithm:
Step 1: To open the unity engine.

Step 2: Create a new 3D project.

Step 3: Create plane and name it as ground and create cube and name it as player.

Step 4: Add WinText in Hierarchy.

Step 5: Create a C# Script and name it as playercontroller and add the script to player.

Step 6: Use the R button to change the level2

Step 7 Print the Output and end the program.
## Program:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class cubemovement : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("LEVEL2");
        }
    }
    private void OnTriggerEnter(Collider other)
    {
        if (other.gameObject.tag == "Cube")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}
```
## Output:
![Screenshot 2025-05-24 213730](https://github.com/user-attachments/assets/805c5f03-a0d5-4573-8e0b-0602a491843a)
![Screenshot 2025-05-24 213741](https://github.com/user-attachments/assets/df911004-d4e2-460c-9ee0-a069ae3e7c68)
![Screenshot 2025-05-24 213801](https://github.com/user-attachments/assets/87fb3632-adbe-42be-80e0-9107f9fa923d)

## Result:
Thus, the execution of above C# coding is successfully redirecting the scene in the unity engine.
