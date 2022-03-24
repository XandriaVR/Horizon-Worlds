# Horizon-Worlds
## Code block
:small_orange_diamond: Source of this data is from Code Block Reference PDF (Note: newest data)

:small_blue_diamond: Source of this data is from: https://support.oculus.com/487096395667734 (Note: older data)

:white_medium_small_square: subcategories under main category

### Events Tab

| Icon | Item in Library | Item in Folder | Parameters | Description | Tips |
| --- | --- | --- | --- | --- | --- |
| :white_medium_small_square: | **Control** |
| :small_orange_diamond: | if | if [condition] | Boolean: condition needs to evaluate to true | When If condition evaluates to true, execute the nested command(s).
| :small_orange_diamond: | else if | else if [condition] | Boolean: condition needs to evaluate to true | When else if condition evaluates to true, execute the nested command(s). | Note: must be placed directy below an if codeblock. | 
| :small_orange_diamond: | else | else | | Will run nested commands if the the if codeblock evaluates to false. | Note: must be placed directly below an if or else if codeblock. |
| :small_orange_diamond: | while | while [condition] | Boolean: condition needs to evaluate to true | Will execute nested command(s) while the condition evaluates to true. | Note: limited to x amount of executions to avoid expensive/infinite loops. Use an event loop if you reach the limit.
| :white_medium_small_square: | **Events** |
| :small_blue_diamond: | When world is started | When world is started | | Event runs when world starts. This will happen when the first person enters the world's instance. :small_orange_diamond: Also runs after using reset world codeblock and at the start of a local script. |
| :small_blue_diamond: | When event is received | When event [myevent] is received with [param] | :small_orange_diamond: Up to 3 parameters can be received. They can be any value type, except list. | Event runs when a custom event is received by this object. The custom event can be sent by the same script or a script on another object. | :small_orange_diamond: Note: names given to input parmeters are local to the event. Use set to codebock to assign it's value to a variable and make it available to the entire script.
| :white_medium_small_square: | **Event Actions** |
| :small_blue_diamond: | Send event to object | Send event [myevent] to [self] with [param] | Object: (self, object, or player) that the event is sent to <br><br>param: Up to 3 parameters the event can send | Sends a custom event to an object variable. The event will be received by the object that is being referenced by the object variable. | :small_orange_diamond: Note: parameter names and order must match receiving event. |
| :small_blue_diamond: | Send event with delay | Send event [myevent] to [self] after [number] seconds with [param] | Object: (self, object, or player) the event is sent to <br><br>number: The number of seconds to delay <br><br>:small_orange_diamond: param: Up to 3 parameters the event can send | Sends a custom event to an object variable, with a set delay. The event will be received by the object that is being referenced by the object variable. | :small_orange_diamond: Note: parameter names and order must match receiving event. Only one of each delayed event can be sent at a time. | 
| :small_blue_diamond: | Cancel sending event with delay | Cancel sending event [myevent] to [self] | Object: (self, object, or player) to stop sending a custom event to | Cancels a custom event from being sent. |
| :white_medium_small_square: | **Collision Events** |
| :small_blue_diamond: | When trigger is entered by object | ~~When event [triggerenter] with [obj] is received~~ <br>When trigger is entered by [obj] | Object: The object that entered trigger | Event runs when an object enters the trigger gizmo. | Note: The trigger must be configured to detect objects with a specific tag, and the object must have that tag. :small_orange_diamond: Script should be attached to the trigger or use connect to or listen to codeblocks to receive events from the trigger. |
| :small_blue_diamond: | When trigger is exited by object | ~~When event [triggerexit] with [obj] is received~~ When trigger is exited by [obj] | Object: The object that exited trigger | Event runs when an object exits the trigger gizmo. | Note: The trigger must be configured to detect objects with a specific tag, and the object must have that tag. :small_orange_diamond: Script should be attached to the trigger or use connect to or listen to codeblocks to receive events from the trigger. |
| :small_blue_diamond: | When colliding with object | ~~When event [collisionenter] with [object] is received~~ <br>When colliding with [obj] | Object: The object that collided with the object that this script is attached to. | Event runs when object collides with another object. | Note: The object must be configured to detect collisions and tag must match the one specified by the trigger. |
| :small_blue_diamond: | When colliding with player | ~~When event [collisionenter] with [player] is received~~ <br>When colliding with [player] | Player: The player that collided with the object this script it attached to. | | Event runs when object collides with the players head or torso. | Note: The object must be configured to detect player collisions, or player and object collision. |
| :white_medium_small_square: | **Player Events** |
| :small_blue_diamond: | When trigger is entered by player | ~~When event [triggerenter] with [player] is received~~ <br>When trigger is entered by [player] | Player: The player that entered the trigger | Event runs when a player enters the trigger the script is attached to. | Note: The trigger must be configured to detect players. |
| :small_blue_diamond: | When trigger is exited by player | ~~When event [triggerexit] with [player] is received~~ <br>When trigger is exited by [player] | Player: The player that exited the trigger | Event runs when a player exits the trigger the script is attached to. | Note: The trigger must be configured to detect players. |
| :small_orange_diamond: | When player enters the world | When world is entered by [player] | Player: The player who eneters the world | Executes when player enters the world and when world is reset | Note: Also executes when a builder enters preview mode.
| :small_orange_diamond: | When player exits the world | When world is exited by [player] | Player: The player who exits the world | | Executes when player exists the world | Note: Also executes when a bulder enters build mode. |
| :white_medium_small_square: | **Projectile Events** |
| :small_orange_diamond: | When projectile hits player | When projectile hits player [player] [pos] [normal] [head] | Player: who was hit <br><br>Pos: vector, where projectile hit <br><br>Normal: direction vector, which side of the player was hit <br><br>Head: boolean returns true if players head was hit | Executes when projectile from the launcher gizmo hits a player. The projectile launcher gizmo receives the event with four parameters. |
| :small_orange_diamond: | When projectile hits interactive object | When projectile hits interactive object [obj] [pos] [normal] | Object: what was hit <br><br>Pos: vector, where the projectile hit <br><br>Normal: direction vector, which side of the object was hit | Executes when projectile from the launcher gizmo hits an interactive object |
| :small_orange_diamond: | When projectile hits static object | When projectile hits static object [pos] [normal] | Pos: vector, where the projectile hit <br><br>Normal: direction vector, which side of the object was hit | Executes when projectile from the launcher gizmo hits a static object |
| :white_medium_small_square: | **Grab Events** |
| :small_blue_diamond: | When object is grabbed by player | ~~When event [grabstart] with [player] is received~~ When object is grabbed by [player] | Player: The player that grabbed the object that this script it attached to. | Event runs when this object is grabbed by a player. |
| :small_blue_diamond: | When object is released by player | ~~When event [grabend] with [player] is received~~ When object is released by [player] | Player: The player that released the object that this script it attached to. :small_orange_diamond: Also executes when a player leaves the world while holding the object. | Event runs when this object is released by a player. |
| :small_orange_diamond: | When object is grabbed by 2 hands | When object is grabbed by 2 hands of [player] |
| :small_orange_diamond: | When object is no longer grabbed by 2 hands | When object is no longer grabbed by 2 hands [player] |
| :white_medium_small_square: | **Attachable Events** |
| :small_blue_diamond: | When object is attached to player | When event [attachstart] with [player] is received | Player: The player that attached the object that this script it attached to | Event runs when this object is attached to a player. | Note: The object being manipulated must be marked as "Interactive" with "Grabbable" in order to be set as attachable. |
| :small_blue_diamond: | When object is unattached from player | When event [attachend] with [player] is received | Player: The player that unattached the object that this script it attached to | Event runs when this object is detached from a player. | Note: The object being manipulated must be marked as "Interactive" with "Grabbable" in order to be set as attachable. |
| :white_medium_small_square: | **Controller Events** |
| :small_blue_diamond: | When index trigger is pressed | When event [indextriggerdown] with [player] is received while self is grabbed | Player: The player that pressed their trigger while holding the object that this script it attached to | Event runs when the index trigger on the oculus controller is pressed. This event will only work on an object that is being grabbed by a player. | |
| :small_blue_diamond: | When index trigger is released | When event [indextriggerup] with [player] is received while self is grabbed | Player: The player that released their trigger while holding the object that this script it attached to | Event runs when the index trigger on the oculus controller is released. This event will only work on an object that is being grabbed by a player. | |
| :small_blue_diamond: | When button1 is pressed | When event [button1down] with [player] is received while self is grabbed | Player: The player that pressed button 1 while holding the object that this script it attached to | Event runs when button 1 on the oculus controller is pressed. This event will only run on an object that is being grabbed by the hand that is holding the controller. | Note: This event will only run on an object that is being grabbed by the hand that is holding the controller. |
| :small_blue_diamond: | When button1 is released | When event [button1up] with [player] is received while self is grabbed | Player: The player that released button 1 while holding the object that this script it attached to | Event runs when button 1 on the oculus controller is released. This event will only run on an object that is being grabbed by the hand that is holding the controller. | Note: This event will only run on an object that is being grabbed by the hand that is holding the controller. |
| :small_blue_diamond: | When button2 is pressed | When event [button2down] with [player] is received while self is grabbed | Player: The player that released button 2 while holding the object that this script it attached to | Event runs when button 2 on the oculus controller is pressed. This event will only run on an object that is being grabbed by the hand that is holding the controller. | Note: This event will only run on an object that is being grabbed by the hand that is holding the controller. | 
| :small_blue_diamond: | When button2 is released | When event [button2up] with [player] is received while self is grabbed | Player: The player that released button 2 while holding the object that this script it attached to | Event runs when button 2 on the oculus controller is released. This event will only run on an object that is being grabbed by the hand that is holding the controller. | Note: This event will only run on an object that is being grabbed by the hand that is holding the controller. |
| :white_medium_small_square: | **Connections**  |
| :small_blue_diamond: | Connect to event | connect [self] [triggerenter] to local event [enter] | object: The object the where the non-local script event fires event: The event in the non-local script <br><br>event: The event in the local script that the non-local script should connect to | Connects an event in another object to an event in the local script, so when the event in the other object is triggered, the event in the local script is triggered too. | Note: This is useful for connecting multiple triggers in a script to one or multiple events in order to make a triggerable system. |
| :small_orange_diamond: | Listen to events |

### Motion Tab

| Icon | Item in Library | Item in Folder | Parameters | Description | Tips |
| --- | --- | --- | --- | --- | --- |
| :white_medium_small_square: | **Instant Motion**  |
| :small_blue_diamond: | Move to | action [moveto with [vector 1 / 0 / 0]] on [self] | vector: The position in world space that the object moves to object: The object that the motion applies to | Instantly moves the object to the coordinates provided. | Note: The object being manipulated must be marked as "Interactive" or "Animated" in the properties panel of the object. |
| :small_blue_diamond: | Move by | action [move with [vector 1 / 0 / 0]] on [self] | vector: The direction and distance the object will move by object: The object that the motion applies to | Instantly moves the object relative to its current position by adding the vector to the current position. | |
| :small_blue_diamond: | Rotate to | action [rotateto with [rotation 90 / 0 / 0]] on [self] | rotation: The angle the object will rotate to object: The object that the motion applies to | Instantly rotates the object to the rotation provided. |
| :small_blue_diamond: | Rotate by | action [rotate with [rotation 90/ 0 / 0]] on [self] | rotation: The angle the object will rotate by object: The object that the motion applies to | Instantly rotates the object by adding the supplied rotation to the current rotation. |
| :small_blue_diamond: | Scale to | action [scale with [vector 1 / 0 / 0]] on self]] | vector: The size the object will scale to object: The object that the motion applies to | Instantly sets the scale to the value provided. |
| :small_orange_diamond: | Scale by |
| :white_medium_small_square: | **Motion Over Time**  |
| :small_blue_diamond: | Move to over time | action [moveto with [vector 1 / 0 / 0] over [number {1} sec]] on [self] | vector: The positon in world space that the object moves to number: The number of seconds it takes to move object: The object that the motion applies to | Moves the object along a line from its current position to a new coordinate over the given time. |
| :small_blue_diamond: | Move by over time | action [move with [vector 1 / 0 / 0] over [number {1} sec]] on [self] | vector: The direction and distance the object will move by number: The number of seconds it takes to move object: The object that the motion applies to | Moves the object along a line from its current position to a new coordinate that is the sum of the current position and the given coordinate, over the given time. |
| :small_blue_diamond: | Rotate to over time | action [rotateto with [rotation 90 / 0 / 0] over [number {1} sec]] on [self] | rotation: The angle the object will rotate to number: the number of seconds it takes to rotate object: The object that the motion applies to | Rotates the object from its current rotation to the given rotation over the given time. |
| :small_blue_diamond: | Rotate by over time | action [rotate with [rotation 90 / 0 / 0] over [number {1} sec]] on [self] | rotation: The angle the object will rotate by number: the number of seconds it takes to rotate object: The object that the motion applies to | Rotates the object from its current rotation by the given rotation over the given time. |
| :small_blue_diamond: | Scale to over time | action [scale with [vector 1/ 1/ 1] over [number {1} sec]] on [self] | vector: The size the object will scale to number: the number of seconds it takes to scale object: The object that the motion applies to | Scales the object from its current scale to the given scale over the given time. |
| :small_orange_diamond: | Scale by over time |
| :white_medium_small_square: | **Player Motion**  |
| :small_blue_diamond: | Respawn player | action [respawn with [param]] on [self] | playerid: The player that will be respawned object: The spawn point to respawn them to | Teleports a player to a spawn point. |
| :small_orange_diamond: | Set player speed |
| :small_orange_diamond: | Set player gravity |
| :white_medium_small_square: | **Physical Motion**  |
| :small_blue_diamond: | Disable object physical motion | disable [self] physical motion | object: The object that physical motion is being disabled on | Locks a physics object in place. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| :small_blue_diamond: | Enable object physical motion | enable [self] physical motion | object: The object that physical motion is being enabled on | Unlocks a physics object, allowing it to be moved. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| :small_blue_diamond: | Push | action [+Velocity with [vector 1/ 1/ 1]] on [self] | vector: The velocity being added object: The object that physical motion is being applied to | The object's velocity becomes equal to its current velocity, plus the given velocity. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| :small_blue_diamond: | Push with mass | action [+impulse with [vector 1/ 0/ 0]] on [self] | vector: The velocity being added object: The object that physical motion is being applied to | The object's velocity becomes equal to its current velocity, plus the given velocity divided by the object's mass (heavier objects have their velocity adjusted less). | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| :small_blue_diamond: | Push in local space | action [+VelLocal with [vector 1/ 0/ 0]] on [self] | vector: The velocity being added object: The object that physical motion is being applied to | The given velocity is rotated to the object's rotation, then a Push runs (x becomes left/right, y becomes above/below, z becomes forward/backward). | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| :small_blue_diamond: | Push in local space with mass | action [+ImpLocal with [vector 1/ 0 / 0]] on [self] | vector: The velocity being added object: The object that physical motion is being applied to | The given velocity is rotated to the object's rotation, then a Push with Mass runs (x becomes left/right, y becomes above/below, z becomes forward/backward). | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| :small_blue_diamond: | Spin | action [+AngVel with [vector 1/ 0/ 0]] on [self] | vector: The angular velocity being added object: The object that physical motion is being applied to | The object's angular velocity becomes equal to its current angular velocity, plus the given angular velocity. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| :small_blue_diamond: | Spin in local space | action [+AngVelLocal with [vector 1/ 0/ 0]] on [self] | vector: The angular velocity being added object: The object that physical motion is being applied to | The given velocity is rotated to the object's current rotation, then a Spin runs (x becomes pitch, y becomes yaw, z becomes roll). | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| :small_blue_diamond: | Stop physical motion | stop physical motion [self] | object: The object that the physical motion is being stopped on | The object's velocity and angular velocity both become zero. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| :small_blue_diamond: | Launch from object | action [LaunchFrom with [self] [number {10}]] on [self] | object: The object whose position and direction will be used to launch from number: The speed to launch it at object: The object that will be launched | Makes the object become owned by the same owner of the "launch from" object (i.e. object specified by the first parameter), sets the position and rotation of the object to match that of the "launch from" object, and then sets the object's velocity to match its forward direction with a magnitude (speed) equal to the value of the second parameter. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |

### Actions Tab

| Icon | Item in Library | Item in Folder | Parameters | Description | Tips |
| --- | --- | --- | --- | --- | --- |
| :white_medium_small_square: | **Object**  |
| :small_blue_diamond: | Show object | show [self] | object: The object that will turn visible | Makes object visible in your world. | Note: This will currently also affect collisions on an object. The object will be made collidable. |
| :small_blue_diamond: | Hide object | hide [self] | object: The object that will turn hidden | Hides the object in your world. | Note: This will currently also affect collisions on an object. The object will have collisions turned off. |
| :small_blue_diamond: | Paint object | action color with [color 1/ 0/ 0] on [self] | color: The rgb color to paint the object with object: The object that will be painted | Sets the color of the object. |
| :small_blue_diamond: | Enable object | enable [self] | object: The trigger that will be enabled | Enables a trigger's ability to detect people or objects. This can only be used on triggers. |
| :small_blue_diamond: | Disable object | disable [self] | object: The trigger that will be disabled | Disables a trigger's ability to detect people or objects. This can only be used on triggers. |
| :small_blue_diamond: | Set simulated | action [setsimulated with boolean {true/false}] on [self] | boolean: The true or false value that the simulated property will be set to object: The object that will have its simulation set | Enables or disables the "simulated" property. If off, the object cannot move. |
| :small_blue_diamond: | Set gravity | action [setgravity with boolean {true/false}] on [self] | boolean: The true or false value that the gravity property will be set to object: The object that will have its simulation set | Enables or disables gravity simulation on this object.If on, the object will fall to the floor. If off, it wil act like it's floating in space. |
| :small_orange_diamond: | Force release |
| :small_orange_diamond: | Launch projectile |
| :small_orange_diamond: | Launch projectile at speed |
| :small_orange_diamond: | Set projectile gravity |
| :white_medium_small_square: | **Text** |
| :small_blue_diamond: | Display text | action [display with [number {1}]] on [self] | string/number: The value the text gizmo will display object: The text gizmo that displays the string/number | Sets the displayed text in the text gizmo. |
| :white_medium_small_square: | **Animation** |
| :small_blue_diamond: | Play animation | play animation on [self] | object: The object that will play its animation | Plays the object's animation. |
| :small_blue_diamond: | Pause animation | pause animation on [self] | object: The object that will pause its animation | Pauses the object's animation. |
| :small_blue_diamond: | Stop animation | stop animation on [self] | object: The object to stop its animation |
| :white_medium_small_square: | **Sound** |
| :small_blue_diamond: | Play sound | play sound on [self] | object: The sound gizmo that will play | Plays a sound gizmo. | Note: A sound must be stopped before it can be played again. |
| :small_blue_diamond: | Pause sound | pause sound on [self] | object: The sound gizmo that will pause | Pauses a sound gizmo. | Note: A sound must be stopped before it can be played again. |
| :small_blue_diamond: | Stop sound | stop sound on [self] | object: The sound gizmo that will stop | Stops a sound gizmo. | Note: A sound must be stopped before it can be played again. |
| :white_medium_small_square: | **VFX** |
| :small_blue_diamond: | Play visual fx | play visual effects on [self] | object: The visual effect gizmo that will play | Plays a visual effects gizmo. |
| :small_blue_diamond: | Stop visual fx | stop visual effects on [self] | object: The visual effect gizmo that will stop | Stops a visual effects gizmo. |
| :white_medium_small_square: | **World**  |
| :small_blue_diamond: | Reset world state | reset world state | | Resets the world back to its inital state. |
| :white_medium_small_square: | **Player** |
| :small_orange_diamond: | Transfer ownership of object to player |
| :small_orange_diamond: | Owner of object |
| :small_orange_diamond: | Play Haptics on player controller |
| :small_orange_diamond: | Set player voice setting to |
| :white_medium_small_square: | **Raycast** |
| :small_orange_diamond: | Raycast |
| :small_orange_diamond: | Raycast with overrides |

### Operators Tab

| Icon | Item in Library | Item in Folder | Parameters | Description | Tips |
| --- | --- | --- | --- | --- | --- |
| :white_medium_small_square: | **Logic**  |
| :small_blue_diamond: | == | [a] == [b] | | "true" if both values are the same. |
| :small_blue_diamond: | != | [a] != [b] | | "true" if both values are not same. |
| :small_blue_diamond: | < | [a] < [b] | | "true" if the first value is less than the second value |
| :small_blue_diamond: | > | [a] > [b] | | "true" if the first value is greater than the second value |
| :small_orange_diamond: | <= | [a] <= [b] | | "true" if the first value is less than or equal to the second value |
| :small_orange_diamond: | >= | [a] >= [b] | | "true" if the first value is greater than or equal to the second value |
| :small_blue_diamond: | and | [a] and [b] | | "true" if both values are true. | |
| :small_blue_diamond: | not | not [a] | | toggles a boolean value from true to false, or false to true. (I think this correct?) |
| :small_blue_diamond: | or | [a] or [b] | | "true" if one of the values is true. |
| :white_medium_small_square: | **Basic Operations**  |
| :small_blue_diamond: | + | [a] + [b] | | Returns the sum of two numbers. |
| :small_blue_diamond: | - | [a] - [b] | | Returns the difference of two numbers. |
| :small_blue_diamond: | * | [a] * [b] | | Returns the result of two multiplied numbers |
| :small_blue_diamond: | / | [a] / [b] | | Returns the result of the first number divided by the second number. |
| :small_blue_diamond: | % | [a] % [b] | | Returns the "remainder" of the first number divided by the second number. Useful for making counters that count up to a certain number and then go back to 0. |
| :white_medium_small_square: | **Basic Math**  |
| :small_blue_diamond: | abs | abs [n] | | Returns the positive value of a number. So, abs -10 = 10 and abs 3 = 3. |
| :small_blue_diamond: | ceil | ceil [n] | | Rounds a decimal number up to the next largest whole number. |
| :small_blue_diamond: | clamp | clamp [value] [min] [max] | | If the value is less than the smallest number, return the smallest number. If the value is larger than the biggest number, return the biggest number. Otherwise return the value. |
| :small_blue_diamond: | floor | floor [n] | | Rounds a decimal number down to the next smallest whole number. |
| :small_blue_diamond: | frac | frac [n] |
| :small_blue_diamond: | lerp | lerp [from] [to] [alpha] | | Given a minimum number, maximum number, and an interpolated value between those numbers, lerp will return a value that represents the point of the interpolated value. |
| :small_blue_diamond: | max | max [a] [b] | | Returns the biggest number |
| :small_blue_diamond: | min | min [a] [b] | | Returns the smalles number |
| :small_blue_diamond: | sqrt | sqrt [n] | | Returns the square root of a number |
| :white_medium_small_square: | **Advanced Math**  |
| :small_blue_diamond: | pow | pow [number] [power] |
| :small_blue_diamond: | cos | cos [radians] | | Returns the cosine value of a number, from -1.0 to 1.0. |
| :small_blue_diamond: | sin | sin [radians] | | Returns the sine value of a number, from -1.0 to 1.0. |
| :small_blue_diamond: | tan | tan [radians] |
| :small_blue_diamond: | acos | acos [radians] |
| :small_blue_diamond: | asin | asin [radians] |
| :small_blue_diamond: | atan2 | atan2 [y] [x] |
| :small_blue_diamond: | exp | exp [power] |
| :small_blue_diamond: | log10 | log10 [number] |
| :small_orange_diamond: | radians to degrees |
| :small_orange_diamond: | degrees to radians |
| :white_medium_small_square: | **Random Numbers** |
| :small_blue_diamond: | random number with decimals | random between [min] and [max] | | Returns a value that can contain fractional decimals, between the first number and the second number. | Note: This is inclusive of the [min] value and inclusive of the [max] value. |
| :small_blue_diamond: | random number | random integer between [min] and [max] | | Returns a whole number value, between the first number and the second number. | Note: This is inclusive of the [min] value and exclusive of the [max] value. |
| :small_blue_diamond: | 2d perlin noise | 2d perlin noise [x] [y] | | Returns a number value based on the perlin noise algorithm. |
| :white_medium_small_square: | **Object Transformation** |
| :small_blue_diamond: | position of object | position of [o] |
| :small_blue_diamond: | rotation of object | rotation of [o] |
| :small_blue_diamond: | scale of object | scale of [o] |
| :small_blue_diamond: | velocity of object | velocity of [o] |
| :small_blue_diamond: | forward direction of object | forward direction of [object] |
| :small_blue_diamond: | upward direction of object | upward direction of [object] |
| :white_medium_small_square: | **Vector Math** |
| :small_blue_diamond: | new vector from xyz | new vector [x] [y] [z] |
| :small_blue_diamond: | x of vector | x of [vector] |
| :small_blue_diamond: | y of vector | y of [vector] |
| :small_blue_diamond: | z of vector | z of [vector] |
| :small_blue_diamond: | normalize | normalize [vector] |
| :small_blue_diamond: | dot | dot [a] [b] |
| :small_blue_diamond: | cross | cross [a] [b] |
| :small_blue_diamond: | distance to | distance from [a] to [b] | 
| :small_blue_diamond: | magnitude of | magnitutde of [vector] |
| :small_blue_diamond: | reflect | reflect [vector] |
| :small_blue_diamond: | new rotation from xyz | new rotation [pitch] [yaw] [roll] |
| :small_blue_diamond: | look at | look towards [forward] with up [up] |
| :white_medium_small_square: | **Color** |
| :small_blue_diamond: | new color from rgb | new color [r] [g] [b] |
| :small_blue_diamond: | rgb to hsv | convert rgb to hsv [color] |
| :small_blue_diamond: | hsv to rgb | convert hsv to rgb [color] |
| :small_blue_diamond: | color of object | color of [o] |
| :white_medium_small_square: | **Player** |
| :small_blue_diamond: | Position of player | [head] position of [player] | | Can specify head, torso, left hand, right hand, and foot position of a player. |
| :small_blue_diamond: | Forward direction of player | [head] forward of [player] | | Can specify head, torso, left hand, right hand, and foot forward of a player. |
| :small_orange_diamond: | Upward direction of player |
| :small_blue_diamond: | Name of player | name of [player] | | Returns the username of a player. |
| :small_orange_diamond: | Get player index |
| :small_orange_diamond: | Get player from index |
| :white_medium_small_square: | **Text** |
| :small_blue_diamond: | Length of string | length of [string] | | Returns the length of a string. |
| :small_orange_diamond: | Substring of string |
| :white_medium_small_square: | **List** |
| :small_orange_diamond: | Length of list |
| :small_orange_diamond: | Add to list |
| :small_orange_diamond: | Set Value at index in list |
| :small_orange_diamond: | Remove item at index from list |
| :small_orange_diamond: | Clear list |
| :small_orange_diamond: | Get item from list |
| :small_orange_diamond: | Index of item in list |
| :white_medium_small_square: | **Raycast** |
| :small_orange_diamond: | Get raycast data |

### Values Tab

| Icon | Item in Library | Item in Folder | Parameters | Description | Tips |
| --- | --- | --- | --- | --- | --- |
| :white_medium_small_square: | **Values** |
| :small_blue_diamond: | set to | set [variable] to [value] |
| :small_orange_diamond: | Set player persistent variable to |
| :small_orange_diamond: | Get player persistent var |
| :white_medium_small_square: | **Debugging** |
| :small_blue_diamond: | debug print | debug print [value] |
| :white_medium_small_square: | **Type Casting** |
| :small_blue_diamond: | Variable as string | [string] as string | | Converts other variables that aren't strings into strings. This is useful when concatenating values that aren’t strings together. |
| :white_medium_small_square: | **Value Input** |
| :small_blue_diamond: | self | (self) | | Represents the object that the script is attached to. |
| :small_orange_diamond: | server player |
| :small_blue_diamond: | number input | (number [0]) | | A number value. |
| :small_blue_diamond: | boolean input | [boolean [false]] | | A boolean value. |
| :small_blue_diamond: | vector input | (vector [0] [0] [0]) | | A vector3 value. |
| :small_blue_diamond: | rotation input | (rotation [0] [0] [0]) | | A rotation value. |
| :small_blue_diamond: | color input | (color [1] [1] [1]) | | A color value. |
| :small_blue_diamond: | string input | (string [.]) | | A string value. |
| :white_medium_small_square: | **Constants** |
| :small_orange_diamond: | Pi |

### Variables Tab
| Icon | Item in Library | Item in Folder | Parameters | Description | Tips |
| --- | --- | --- | --- | --- | --- |
| :white_medium_small_square: | **Variables** |
| :small_orange_diamond: | Number |
| :small_orange_diamond: | Boolean |
| :small_orange_diamond: | Object |
| :small_orange_diamond: | Player |
| :small_orange_diamond: | Vector |
| :small_orange_diamond: | Rotation |
| :small_orange_diamond: | Color |
| :small_orange_diamond: | String |
| :small_orange_diamond: | List |

