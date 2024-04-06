![SPRITENATOR (1920 x 1300 px)](https://github.com/christinec-dev/NavPath2D/assets/87696858/c4455408-ffcd-4fcf-a4f0-6bb66a33a796)
![4](https://github.com/christinec-dev/NavPath2D/assets/87696858/71456c8f-11ee-4184-9008-7b02c0379bad)
![5](https://github.com/christinec-dev/NavPath2D/assets/87696858/531e49dd-a40b-4ac2-ac86-ad6098b2ab8b)

---

# Overview
NavPath2D is a GUI-based tool designed to simplify the creation and management of navigation paths for 2D entities in Unity. It allows you to draw paths (that entities such as your AI should follow) directly in your Unity Editor scene. 

These paths can then be saved as prefabs and assigned to entities. These entities will then randomly select a path to move on, eliminating the need for complex A* pathfinding algorithms. 

This package is particularly suitable for simpler cases where detailed pathfinding is not required, offering a straightforward alternative to more complex solutions. You also have the flexibility to expand upon the basic functionality, making it adaptable to various genres and project requirements.

---

# Table of Contents
- [Links](#links)
- [Features](#tool-features)
- [Instructions](#usage-instructions)

---

# Links
- [Download Package](https://github.com/christinec-dev/NavPath2D/tree/main/Package)
- [GitBook](https://oops-i-devd.gitbook.io/christinec-dev)
- [Join My Discord](https://discord.gg/4N6b4bkC8h)
- [Support Me](https://ko-fi.com/christinedevs)
- [Unity Package](https://assetstore.unity.com/packages/slug/281705)
  
---

# Tool Features
- **GUI-based Path Creation:** Users can draw paths directly in the Unity Editor scene, providing a visual and intuitive way to define movement paths for 2D entities. This feature allows for the creation of paths that can navigate around obstacles, follow specific routes, and more, offering flexibility in how paths are formed.
- **Multiple Path Selection:** Once paths are created, they can be saved as prefabs. This functionality facilitates easy reuse and assignment to different entities within the project. Additionally, entities can be assigned multiple paths, enabling them to randomly decide which path to follow, adding an element of unpredictability to their movement.
- **Entity Movement Along Paths:** Entities can be assigned paths, enabling them to move along the defined waypoints. This feature eliminates the need for complex A* pathfinding algorithms, simplifying path management for 2D games and making it easier to implement straightforward movement patterns.
- **Simplified Pathfinding for 2D:** This package addresses the lack of a built-in NavMesh feature for 2D in Unity by offering a straightforward solution for pathfinding. It provides a simple yet effective way to manage entity movement in 2D environments.
- **Customizable and Expandable:** The package is designed to be a simple solution for basic pathfinding needs but also allows for expansion and customization to fit more complex scenarios. Users can add their movement customizability by defining more randomization in movement, animations, and more, making the package adaptable to a wide range of gameplay requirements.

---
# Usage Instructions
### Download and Import:
Download the NavPath2D package and import it into your Unity project.

![Screenshot 2024-04-06 150555](https://github.com/christinec-dev/NavPath2D/assets/87696858/501c3c09-c697-482c-893e-52e46b073d77)

## Setup AI Entity: 
Ensure you have an AI entity set up in your Unity project.

![image](https://github.com/christinec-dev/NavPath2D/assets/87696858/37fa3371-87c0-4601-af34-e852420f26ee)

## Create Path GameObject:
In your game scene, add a new empty GameObject and rename it to something like "Path_01".

![Screenshot 2024-04-06 150623](https://github.com/christinec-dev/NavPath2D/assets/87696858/c126fa7c-0cb0-48b8-bf2b-f704c96058b3)
![Screenshot 2024-04-06 150633](https://github.com/christinec-dev/NavPath2D/assets/87696858/be1e03b9-e14a-4af3-b01d-59539b75787e)

## Add Path Script:

Attach the `Path.cs` script to this GameObject. This script (which can be found in the Scripts/Navigation folder) allows you to draw paths onto your scene via the `PathEditor.cs` (found in ssets/Editor/NavPath2D/) Editor script as it holds the Waypoints that we add.

![Screenshot 2024-04-06 150640](https://github.com/christinec-dev/NavPath2D/assets/87696858/7cbe91c8-1c0a-40e7-a8bb-f66ed8dff0fb)
![Screenshot 2024-04-06 150645](https://github.com/christinec-dev/NavPath2D/assets/87696858/214479ae-2727-469e-9b7c-d6c442219f10)

## Manage Waypoints: 
With the GameObject selected, you can start adding, removing, and moving waypoints. 
- To add a waypoint, SHIFT-click in the scene window.
- To move a waypoint, click on the waypoint gizmo in the scene window.
- To remove a waypoint, CTRL-click on the waypoint gizmo in the scene window.
- To add a waypoint to an existing waypoint, select it and SHIFT-click a new waypoint.


![Screenshot 2024-04-06 150656](https://github.com/christinec-dev/NavPath2D/assets/87696858/9aa596eb-9287-4480-b452-5f87ea9a9912)
![Screenshot 2024-04-06 150710](https://github.com/christinec-dev/NavPath2D/assets/87696858/ccaf0e58-536f-4d71-9175-97d123230430)
![Screenshot 2024-04-06 150716](https://github.com/christinec-dev/NavPath2D/assets/87696858/d192ae77-311c-495c-a5d8-3b84d0bfbf3f)
![image](https://github.com/christinec-dev/NavPath2D/assets/87696858/d5b0c001-87a2-4dd5-8b09-a77a8504e403)

You can add multiple GameObjects with the `Path.cs` script added to it to create multiple paths.

![Screenshot 2024-04-06 150757](https://github.com/christinec-dev/NavPath2D/assets/87696858/a2c1e9cc-fd5d-44d9-b7b1-e1d38e59c6fd)

## Save Path as Prefab:
Once you're done creating paths, drag the GameObject into your directory to turn it into a Prefab. This allows you to assign it to your entity. You can remove this prefab from the scene hierarchy.

![Screenshot 2024-04-06 150832](https://github.com/christinec-dev/NavPath2D/assets/87696858/2ba5cde5-404d-4125-9c33-e5f18d510279)
![Screenshot 2024-04-06 150836](https://github.com/christinec-dev/NavPath2D/assets/87696858/b9d7d9e3-97be-40bd-b08c-2441f05d268b)
![Screenshot 2024-04-06 155655](https://github.com/christinec-dev/NavPath2D/assets/87696858/73aca94e-b0f1-4122-b273-db07152986a2)

## Assign Path to Entity: 
Select your entity and attach the `Walker.cs` (which can be found in the Scripts/NavPath2D folder) script to it. This is a demo script which allows you to assign the path prefabs to your entity, enabling it to randomly move along the paths. You can expand this script to include logic for breaks within movement, animations, etc., or combine it with your existing scripts. 

In the script:

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class RandomWalker : MonoBehaviour
{
    private Path currentPath; // path it chooses to walk on
    private int currentWaypointIndex = -1; // waypoint index
    public float speed = 2f; //entity speed - how fast it will move
    public float waypointTolerance = 1f; //how close it stays to path - the lower this value, the more accurate it is (do not set to 0).
    public List<GameObject> pathPrefabs; //path options entity can select from 
    
    void Start()
    {
        // Randomly choose and instantiate a path from the path prefabs addded
        GameObject pathGO = Instantiate(pathPrefabs[Random.Range(0, pathPrefabs.Count)]);
        currentPath = pathGO.GetComponent<Path>();
    }

    void Update()
    {
        // Move entity randomly on the waypoints of chosen path
        if (currentPath.waypoints.Count == 0) return;
          if (currentWaypointIndex == -1 || Vector3.Distance(transform.position, currentPath.waypoints[currentWaypointIndex].position) < waypointTolerance)
          {
              if (currentWaypointIndex == -1)
              {
                  currentWaypointIndex = Random.Range(0, currentPath.waypoints.Count);
              }
              else
              {
                  int nextWaypointIndex = currentPath.waypoints[currentWaypointIndex].GetRandomConnectedWaypointIndex(); // found in Waypoint.cs
                  if (nextWaypointIndex != -1) 
                  {
                      currentWaypointIndex = nextWaypointIndex;
                  }
                  else
                  {
                      currentWaypointIndex = Random.Range(0, currentPath.waypoints.Count);
                  }
              }
          }
          Vector3 waypointPosition = currentPath.waypoints[currentWaypointIndex].position;
          transform.position = Vector3.MoveTowards(transform.position, waypointPosition, speed * Time.deltaTime);
      }
  }
}
```

![Screenshot 2024-04-06 150815](https://github.com/christinec-dev/NavPath2D/assets/87696858/2091f3cf-05f1-4f8b-8d94-b6478bc32258)

## Add Paths to Entity:
Now add the path prefabs that you created to the waypoint list on the script attached to your Entity.

![Screenshot 2024-04-06 150852](https://github.com/christinec-dev/NavPath2D/assets/87696858/fa394338-33d2-462d-9385-f71fd6d80813)


## Run Your Scene: 
Finally, run your scene. Your entity should now choose a path to move on and move between the waypoints. Remember, the lower the waypointTolerance variable value, the closer the entity will walk to the waypoint path.

![Screenshot 2024-04-06 151036](https://github.com/christinec-dev/NavPath2D/assets/87696858/4b4810a2-c74a-4791-ac0c-2b413812fd9d)
![Screenshot 2024-04-06 151015](https://github.com/christinec-dev/NavPath2D/assets/87696858/aed4d7f1-e6d7-46b6-a072-7f57551a1f20)
