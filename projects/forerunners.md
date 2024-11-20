---
title: The Forerunners Gospel
permalink: /projects/forerunners
---

[<< Back to home](/)

# The Forerunners Gospel

{% include image.html url="/images/butterfly_logo_edit.png" %} 

<table>
    <tbody>
    <tr>
      <td><strong>Dates</strong></td>
      <td>Summer 2021 ~ Summer 2023</td>
    </tr>
    <tr>
      <td><strong>Role</strong></td>
      <td>Mobile Systems Engineer (Monetization, Social Features, Publishing)</td>
    </tr>
    <tr>
      <td><strong>Team</strong></td>
      <td>Individual contract with director</td>
    </tr>
    <tr>
      <td><strong>Development Software/Tools</strong></td>
      <td>Unity, XCode</td>
    </tr>
    <tr>
      <td><strong>Summary</strong></td>
      <td>
        <ul>
            <li>
            Contracted to publish Unity-based game to mobile app stores
            </li>
            <li>
            Monetized game by implementing in-app purchases and interstitial advertisements
            </li>
            <li>
            Resolved plugin compatibility issues to publish to iOS and Android app stores
            </li>
            <li>
            Created social sharing features for Twitter and Facebook
            </li>
            <li>
            Challenged by difficulties in pre-existing codebase and plugins
            </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

<br>
<div class="itch-link">
    <span>
        <a href="https://bookofegu.com/games">Official website and download links</a>
    </span>
</div>
<br>
{% include youtube.html id="Z--UHuMXWr4" %}
<br>

## Project and role overview
I was contracted by director Ken Egu to aid with monetization, social features, and publishing of The Forerunners Gospel, which he previously developed with a team at USC. In terms of monetization, I was tasked with adding in-app purchases and interstitial advertisements. For social features, I added the ability to share highscores and screenshots through Facebook and Twitter. I also fixed bugs and edited the game to comply with publishing guidelines in order to release the game to iOS and Google Play app stores. 

My first important task was to familiarize myself with the structure of the project. I was on my own for this, since the game was a past project and there were no other active developers on the game. The game uses Unity and was adapted to mobile using a plugin called "Easy Mobile". Adding features thus required me to read documentation to gain specific knowledge of Easy Mobile and iOS/Android APIs. This was complicated by the project's age: the version of both Easy Mobile and Unity that the original game was built on had compatibility issues and were also non-compliant with the most recent iOS/Android advertising APIs. I needed to update the plugin versions and scour the internet for fixes that would allow proper compiling of builds. Ultimately, I was able to add the required features and publish the game to mobile storefronts.

Through this work, I learned the difficulties of working on mobile projects, as well as the pros/cons of using 3rd party plugins. Even putting Unity compatibility issues aside, publishing to app stores proved cumbersome. I often had to install the game to my personal devices to see whether ads and social features would load, and if not, I had to use activity loggers to examine what went wrong. I also needed to add features to comply with app store policies, such as refunds. The project used the Easy Mobile third-party plugin, which made it much easier to add certain features like IAP and ads. But the plugin was also the source of various problems, like the previously mentioned compatibility issues. The plugin also seems to have ceased development after I left the project, so it would be extremely difficult to update the game to newer Unity versions without significant restructuring. This would pose a problem if, for example, Google Play began requiring support for Android versions that are only compatible with recent Unity builds. This demonstrates the vulnerability of third-party plugins for long-term projects: they can break suddenly and unexpectedly. If monetization relies on continuous availability on app stores or Steam, it may be wiser to stick with each storefront's official API. 