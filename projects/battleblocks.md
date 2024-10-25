---
title: Battle Blocks
permalink: /projects/battle-blocks
published: true
---

[<< Back to home](/)

# Battle Blocks (Spring 2020)

{% include image.html url="/images/battle_blocks_title.jpg" %} 

{% include itchlink.html url="https://katiemoulton.itch.io/battle-blocks" name="Battle Blocks" %}

<table>
    <tbody>
    <tr>
      <td><strong>Dates</strong></td>
      <td>Spring 2020</td>
    </tr>
    <tr>
      <td><strong>Role</strong></td>
      <td>Main Design, Main Engineer</td>
    </tr>
    <tr>
      <td><strong>Team</strong></td>
      <td>Pair</td>
    </tr>
    <tr>
      <td><strong>Development Software/Tools</strong></td>
      <td>Unity</td>
    </tr>
    <tr>
      <td><strong>Summary</strong></td>
      <td>
        <ul>
            <li>
            Game created with partner as main project for Intermediate Game Design & Development class at USC
            </li>
            <li>
            First experience with full production of a game, from prototyping to gold master
            </li>
            <li>
            Developed and documented custom Unity editor to allow designers to easily create, edit, and assign attacks to animations
            </li>
            <li>
            Collaborated with outside usability testers and composers
            </li>
            <li>
            Learned Unity concepts that proved useful in later projects
            </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% include youtube.html id="6rH1WSwHxZM" %}

A local multiplayer game where you arrange blocks to build robots that duel each other in physics-based 2D combat.

I designed and engineered this game with [Katie Moulton](https://katiemoulton.itch.io/) during the Spring 2020 semester for the Intermediate Game Design & Development class at USC.

This was the first project where I was involved with the full production of a game: from prototyping to vertical slice, alpha, beta, gold master, and trailer production. Katie and I also collaborated with usability testers at USC and music/SFX students from the Berklee School of Music. 

Battle Blocks was developed in Unity. I mostly handled implementing the building mechanics, one challenge being implementing the data structures used to keep track of the robot shape. Information that needed to be stored included which sides of a block could be attached to other blocks, which blocks they are attached to, and their health/attack attributes. 

Blocks that have no path to the robot's electrical core lose power and get destroyed, so I also needed to be able to determine whether one block being destroyed would disconnect other blocks. I solved this by treating the robots as a graph where blocks are vertices and connections are edges, then performing depth-first search to determine which blocks were reachable from the core. For example, in the following image the red nodes are no longer reachable from the core:

{% include resized_image.html url="/images/battle_blocks_graph.png" height="30%" width="30%" %} 

Through Battle Blocks, I also learned about Unity's newer Input System package and implemented support for Gamepads and GameCube Controllers. This knowledge proved useful in later projects such as [Crescendo](/projects/crescendo) where I worked as an engineer.