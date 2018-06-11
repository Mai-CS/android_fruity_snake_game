# Description
3D Snake game in Unity3D. The key game components are:<br>
<ul>
<li>snake</li>
<li>game playground border</li>
<li>fruits</li>
<li>obstacles</li>
</ul>
Snake is 3 pieces long at start of a game and starts moving into random direction upon game
start. Snake grows 1 piece for every fruit eaten. After the snake eats a fruit a new fruit appears
on random location. User can control the direction of a snake by pressing/swiping
left/right/up/down. The game is over when the snake hits the border, an obstacle or itself. Think
of this game running on a smartphone device

# Screenshots
 <table>
  <tr>
    <td><img src = "https://image.ibb.co/gGemDT/screener_1499435276551.png"/></td>
    <td><img src = "https://image.ibb.co/gkhHL8/screener_1499435304662.png"/></td>
    <td><img src = "https://image.ibb.co/d3J4YT/screener_1499436242656.png"/></td>
  </tr>
  <tr>
    <td><img src = "https://image.ibb.co/hHEBDT/screener_1499436213969.png"/></td>
    <td><img src = "https://image.ibb.co/j7Bu08/screener_1499436069715.png"/></td>
  </tr>
</table> 

# Assets Links
<a href="http://www.iconarchive.com/show/delightful-zodiac-icons-by-troyboydesign/Snake-icon.html">Launcher icon</a><br>
<a href="http://wallpaperswide.com/fruit_slice-wallpapers.html">Loading screen background</a><br>
<a href="http://kenney.nl/assets/nature-pack-extended">Nature Pack Extended</a><br>
<a href="https://www.assetstore.unity3d.com/en/#!/content/18353">Fantasy Skybox</a><br>
<a href="https://www.assetstore.unity3d.com/en/#!/content/80254">Fruit Pack</a><br>

# Tutorials
<a href="https://www.youtube.com/watch?v=xz8Ga9er3_8">Snake Movement Algorithm in Unity</a>

# Tools & Technologies
Unity 5.6.1, Android SDK

# Download
<a href="https://drive.google.com/open?id=0ByN8UVrN9463S3RlUG5aTkdqbHM"><img src="https://image.ibb.co/h45q7o/android_download.png" width="150" height="80" /></a>

# Brief Technical Design Document
The game is based on 3 TAGS:
<ul>
<li>Fruit - such as apples or bananas</li>
<li>Obstacle - such as walls, trees, etc.</li>
<li>Snake - for every newly created part of snake</li>
</ul>

At first, the snake is composed of only 3 untagged spheres. The snake moves according to touch/swiping position.</br>

If the snake hits "Fruit", The score is increased by 1 and a new sphere is appended to the snake and is tagged by "Snake" using method <code>AddSnakePart()</code>. Also, a new "Fruit" is instantiated at random position on playground using method <code>RandomPointInBox()</code>.</br>

And if the snake hits "Obstacle" or any of its new parts tagged "Snake", <code>Gameover()</code> coroutine is called.</br>

The player goes to next level when the score becomes 10 using method <code>NextLevel()</code>.</br>

There is a loading scene before each level. This scene loads the level number according to <code>public static int level</code></br>

# License
<pre><code>
   Copyright 2017 Mai Ahmed

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
   </code></pre>
