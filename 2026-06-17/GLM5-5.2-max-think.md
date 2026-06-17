**Date:**  2026-06-17<br>
**Model:**  GLM-5.2<br>
**Platform:**  chat.z.ai<br>
**Options:**  Max, Deep Think<br>
**Line of code:**  1683<br>

[Code](https://github.com/bymihaj/creeper-game/blob/main/2026-06-17/GLM5-5.2-max-think.html)<br>
[Play](https://bymihaj.github.io/creeper-game/2026-06-17/GLM5-5.2-max-think.html)<br>
[Shared chat](https://chat.z.ai/s/e24e0652-0e5b-4e11-a8b4-a7dac3b1a3c1)

**Game review:**
Implementation has nice game-style UI design. Design is not a top award winner, but details such as color palettes, fonts and spacing between components look pretty good. Icons from the build menu are identical to unit icons on the map. That staff makes to fill UI as a little bit polished. Map has terrain levels. Creeper flow is distributed according to terrain heights as well. Terrain is procedurally generated every new game, so plus one. Most annoing visual bug is blinking creeper flood. In general game is playable, it is possible to win but I can't test loose condition because creepers grow very slow although player units could be destroyed by creepers flood. Game mechanics allow you to build 4 types of units: reactor, node, blaster and storage. All units might be connected by network. And game provides good animation of energy moving across the network, similar to the original game. That is just animation without real energy packet calculation but good try. Created game is much better than GLM-5 version that is noted in previous post [GLM-5](https://github.com/bymihaj/creeper-game/blob/main/2026-03-04/zai-glm-5-deep-thinking.md)!	


**Code review:**

At starting point we see that code contains 400 lines of CSS styles and it really produce cute UI. In the same time layout is not adapted for different screen size. Main constants are placed and defined in correct place but minors are not. Javascript code is splitted by function. Half of function are expressive, compact and well-named, but another half is up to 200 lines of source code. Anyway all source code is human-readable. One good example is usage of definition like dirs = [[-1,0],[1,0],[0,-1],[0,1]] for avoiding mess of if conditions.
