---
title: Prime Engine Dimension Flip Demo
permalink: /projects/prime-engine
---

[<< Back to home](/)

# Prime Engine Dimension Flip Demo

{% include image.html url="/images/prime_engine.png" %} 

<table>
    <tbody>
    <tr>
      <td><strong>Dates</strong></td>
      <td>Fall 2022</td>
    </tr>
    <tr>
      <td><strong>Role</strong></td>
      <td>Engineer</td>
    </tr>
    <tr>
      <td><strong>Team</strong></td>
      <td>Individual</td>
    </tr>
    <tr>
      <td><strong>Development Software/Tools</strong></td>
      <td>Prime Engine (C++), Maya, Lua</td>
    </tr>
    <tr>
      <td><strong>Summary</strong></td>
      <td>
        <ul>
            <li>
            Created gameplay demo for Game Engine Development course project at USC
            </li>
            <li>
            Demo developed in C++ based Prime Engine
            </li>
            <li>
            Replicated dimension flip mechanic of Super Paper Mario
            </li>
            <li>
            Implemented basic 2D and 3D physics and colliders, perspective and orthographic cameras 
            </li>
            <li>
            Adapted to working in a mostly undocumented workspace
            </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

<br>

{% include youtube.html id="upYdVAee_C8" %}
<br>
The first part of the video demonstrates switching between perspective and orthographic cameras. The second part shows its application to a dimension-flipping mechanic. The player can switch the camera between 3D behind-the-player and 2D sideview. Doing so also changes collision detection between 2D and 3D.

## Project overview
This demo was created as the course project for the Game Engine Development class at USC. I developed the demo using Prime Engine, a C++ based engine created by professor Artem Kovalovs. The engine uses the DirectX interface and comes with its own event-handling architecture, as well as tools to import 3D models, textures, and animations from Maya files. 

In the demo, I emulate a dimension-flipping mechanic seen in Super Paper Mario: the player can swap both the camera and collision detection between 2D and 3D to navigate a puzzle. To achieve this, I implemented an orthographic camera. I transition between views by linearly interpolating between the projection matrices of the perspective and orthographic cameras. I combined this with an interpolation between behind-the-player and sideview camera positions to generate the dimension flip effect. I then created two sets of character controls and physics with gravity and box colliders. When the event is sent to swap camera modes, it also changes which controls and collision detection to use. As seen in the demo, the player can swap dimensions in order to pass behind what would be a wall in 2D, and walk over what would be a gap in 3D. 

Through the demo, I learned to manipulate the 3D math behind game engine features like cameras and hit detection. The biggest challenge was navigating Prime Engine, since it is a custom low-level engine built from the ground-up by the professor, and thus lacks outside documentation. Even adding simple objects or new events required deep dives into the event handlers and the Lua scripts used to import Maya objects. Thus, I gained experience parsing a new development environment, as might be required when joining a pre-existing project.
