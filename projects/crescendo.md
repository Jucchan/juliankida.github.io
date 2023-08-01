---
title: Crescendo
permalink: /projects/crescendo
---

[<< Back to home](/)

# Crescendo

{% include image.html url="/images/crescendo.jpg" %} 

<table>
    <tbody>
    <tr>
      <td><strong>Dates</strong></td>
      <td>Summer 2020 ~ Spring 2021</td>
    </tr>
    <tr>
      <td><strong>Role</strong></td>
      <td>Gameplay Engineer</td>
    </tr>
    <tr>
      <td><strong>Team</strong></td>
      <td>USC Games (team of approx. 25 members, remote)</td>
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
            Engineer for music-themed 2D action-platformer
            </li>
            <li>
            Handled combat logic that generates and detects hits 
            </li>
            <li>
            Developed and documented custom Unity editor to allow designers to easily create, edit, and assign attacks to animations
            </li>
            <li>
            Wrote scripts for enemy attacks and projectile behavior
            </li>
            <li>
            Implemented menu navigation and save/load functionalities
            </li>
            <li>
            Game presented at USC Games Expo and published on itch.io
            </li>
            <li>
            Learned importance of robust foundational systems and documentation
            </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

<br>

{% include itchlink.html url="https://crescendogame.itch.io/crescendo" name="Crescendo" %}

<br>

{% include youtube.html id="wQGqtBvt9NY" %}

## Project and role overview

Crescendo is a 2D action-platformer developed in Unity. The player must traverse music-themed side-scrolling levels and use their conducting baton wand/sword to defeat bosses. 

Crescendo was directed by [Katie Moulton](https://katiemoulton.itch.io/) as part of the Advanced Games Project program, USC Games' capstone class where teams aim to develop a full gameplay experience from pitch to gold master. I had [previously worked with Katie](/projects/battleblocks) and was recruited as an engineer during the Summer of 2020.

As an engineer, I was primarily tasked with combat systems. I designed the process for triggering and detecting attacks, and created tools for creating attacks and attaching them to characters. I also scripted some boss behavior. Aside from combat, I managed menu navigation and save/load features. 

Crescendo was presented at the USC Games Expo and published on itch.io in May 2021. 

## Custom editor and attack manager

My largest contribution to Crescendo was undoubtedly the  attack manager. Early in the design process, there were plans for a variety of player and enemy attacks. Therefore, there was need for a robust hit detection system. 

One solution would be to create all the attack colliders beforehand and turn them on/off with animation events. But if one character had various moves, you could end up with dozens of colliders on one object, which would be hard to manage. It also forces animation events to reference specific colliders on the object, which goes against modular design. 

Instead, I stored all attack data in ScriptableObjects. When the attack manager detects that an attack animation is playing, it reads the corresponding attack data and generates the hitbox. Since the table is stored independently of animations or prefabs, designers and engineers can edit them without fear of interfering with the animations. This was especially important since the game was developed during quarantine; the lack of direct communication made it harder to avoid accidental merge conflicts. 

To allow designers to edit attacks without the help of engineers, I created a custom Unity editor:

{% include image.html url="/images/ryugif.gif" %} 

The custom editor allows you to directly drag to manipulate collider data as if it were an object in the scene. It also uses custom sliders to display when during the animation colliders are active. It supports features such as multiple colliders and animating the colliders through keyframes. 

I documented this editor and other attack features in a technical design document. The custom editor was used without issue through the whole development process. I am proud that I seemingly future-proofed the system sufficiently, considering the overall combat design for the game shifted a couple times during development and various complex boss attacks were added. 

<figure>
{% include image.html url="/images/crescendo_doc.png" %} 
<figcaption style="text-align:center">Part of documentation</figcaption>
</figure>

## Takeaways

Crescendo was my first project on a decently-sized team, during the height of the pandemic nonetheless. I am grateful for the engineering lead, Paiam Moghaddam, who mentored me during this time. At a time when it was sometimes hard to keep people accountable, Paiam was always reliable. On the technical side, he taught me about ScriptableObject architecture, which I continue to use on projects. 

This project showed to me the importance of robust foundational systems and documentation. Since development was remote, team members could not simply walk over to me for questions or fixes. The custom editor's ability to allow other teams to work independently, and the fact that no major rewrites to the attack system were needed, saved significant development time. In the later project  [Party Rogue](https://julian-kida.itch.io/party-rogue), I put the custom editor skills gained in Crescendo to allow members that had never worked on a game before to more easily contribute. 
