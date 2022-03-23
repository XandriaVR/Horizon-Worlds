# Horizon-Worlds
## How do I use code blocks in Horizon Worlds?
Source: https://support.oculus.com/487096395667734

| Item in Library | Item in Folder  | Parameters      | Description     | Tips            |
| --------------- | --------------- | --------------- | --------------- | --------------- |
| **Events**  |   |   |   |   |
| When world is started | When world is started | | Event runs when world starts. This will happen when the first person enters the world's instance. | |
| When event is received | When event[myevent] with [obj] is received | | Event runs when a custom event is received by this object. The custom event can be sent by the same script or a script on another object. | |
| When trigger is entered by object | When event [triggerenter] with [obj] is received | Object: The object that entered trigger | Event runs when an object enters the trigger gizmo. | Note: The trigger must be configured to detect objects with a specific tag, and the object must have that tag. |
| When trigger is exited by object | When event [triggerexit] with [obj] is received | Object: The object that exited trigger | Event runs when an object exits the trigger gizmo. | Note: The trigger must be configured to detect objects with a specific tag, and the object must have that tag. |
| When trigger is entered by player | When event [triggerenter] with [player] is received | Player: The player that entered the trigger | Event runs when a player enters the trigger gizmo. | Note: The trigger must be configured to detect players. |
| When trigger is exited by player | When event [triggerexit] with [player] is received | Player: The player that exited the trigger | Event runs when a player exits the trigger gizmo. | Note: The trigger must be configured to detect players. |
| When colliding with object | When event [collisionenter] with [object] is received | Object: The object that collided with the object that this script is attached to. | Event runs when object collides with another object. | Note: The object must be configured to detect collisions. |
| When colliding with player | When event [collisionenter] with [player] is received | Player: The player that collided with the object this script it attached to. | Event runs when object collides with the players head or torso. | Note: The object must be configured to detect collisions. |
| When object is grabbed by player | When event [grabstart] with [player] is received | Player: The player that grabbed the object that this script it attached to | Event runs when this object is grabbed by a player. |
| When object is released by player | When event [grabend] with [player] is received | Player: The player that released the object that this script it attached to | Event runs when this object is released by a player. |
| When object is attached to player | When event [attachstart] with [player] is received | Player: The player that attached the object that this script it attached to | Event runs when this object is attached to a player. | Note: The object being manipulated must be marked as "Interactive" with "Grabbable" in order to be set as attachable. |
| When object is unattached from player | When event [attachend] with [player] is received | Player: The player that unattached the object that this script it attached to | Event runs when this object is detached from a player. | Note: The object being manipulated must be marked as "Interactive" with "Grabbable" in order to be set as attachable. |
| When index trigger is pressed | When event [indextriggerdown] with [player] is received while self is grabbed | Player: The player that pressed their trigger while holding the object that this script it attached to | Event runs when the index trigger on the oculus controller is pressed. This event will only work on an object that is being grabbed by a player. | |
| When index trigger is released | When event [indextriggerup] with [player] is received while self is grabbed | Player: The player that released their trigger while holding the object that this script it attached to | Event runs when the index trigger on the oculus controller is released. This event will only work on an object that is being grabbed by a player. | |
| When button1 is pressed | When event [button1down] with [player] is received while self is grabbed | Player: The player that pressed button 1 while holding the object that this script it attached to | Event runs when button 1 on the oculus controller is pressed. This event will only run on an object that is being grabbed by the hand that is holding the controller. | Note: This event will only run on an object that is being grabbed by the hand that is holding the controller. |
| When button1 is released | When event [button1up] with [player] is received while self is grabbed | Player: The player that released button 1 while holding the object that this script it attached to | Event runs when button 1 on the oculus controller is released. This event will only run on an object that is being grabbed by the hand that is holding the controller. | Note: This event will only run on an object that is being grabbed by the hand that is holding the controller. |
| When button2 is pressed | When event [button2down] with [player] is received while self is grabbed | Player: The player that released button 2 while holding the object that this script it attached to | Event runs when button 2 on the oculus controller is pressed. This event will only run on an object that is being grabbed by the hand that is holding the controller. | Note: This event will only run on an object that is being grabbed by the hand that is holding the controller. | 
| When button2 is released | When event [button2up] with [player] is received while self is grabbed | Player: The player that released button 2 while holding the object that this script it attached to | Event runs when button 2 on the oculus controller is released. This event will only run on an object that is being grabbed by the hand that is holding the controller. | Note: This event will only run on an object that is being grabbed by the hand that is holding the controller. |
| Send event to object | Send event [myevent] to [self] with [param] | Object: The object that the event is sent to param: The parameters the event will receive | Sends a custom event to an object variable. The event will be received by the object that is being referenced by the object variable. | | 
| Send event with delay | Send event [myevent] to [self] after [number] seconds | Object: The object the event is sent to number: The number of seconds to delay | Sends a custom event to an object variable, with a set delay. The event will be received by the object that is being referenced by the object variable. |
| Cancel sending event with delay | Cancel sending event [myevent] to [self] | Object: The object to stop sending a custom event to | Cancels a custom event from being sent. |
| **Connections**  |   |   |   |   |
| Connect to event | connect [self] [triggerenter] to local event [enter] | object: The object the where the non-local script event fires event: The event in the non-local script event: The event in the local script that the non-local script should connect to | Connects an event in another object to an event in the local script, so when the event in the other object is triggered, the event in the local script is triggered too. | Note: This is useful for connecting multiple triggers in a script to one or multiple events in order to make a triggerable system. |
| **Motion Tab**  |   |   |   |   |
| **Instant Motion**  |   |   |   |   |
| Move to action [moveto with [vector 1 / 0 / 0]] on [self] | vector: The position in world space that the object moves to object: The object that the motion applies to | Instantly moves the object to the coordinates provided. | Note: The object being manipulated must be marked as "Interactive" or "Animated" in the properties panel of the object. |
| Move by | action [move with [vector1 / 0 / 0]] on [self] | vector: The direction and distance the object will move by object: The object that the motion applies to | Instantly moves the object relative to its current position by adding the vector to the current position. | |
| Rotate to | action [rotateto with [rotation 90 / 0 / 0]] on [self] | rotation: The angle the object will rotate to object: The object that the motion applies to | Instantly rotates the object to the rotation provided. | |
| Rotate by | action [rotate with [rotation 90/ 0 / 0]] on [self] | rotation: The angle the object will rotate by object: The object that the motion applies to | Instantly rotates the object by adding the supplied rotation to the current rotation. | |
| Scale to | action [scale with [vector 1 / 0 / 0]] on self]] | vector: The size the object will scale to object: The object that the motion applies to | Instantly sets the scale to the value provided. | |
| **Motion Over Time**  |   |   |   |   |
| Move to over time | action [moveto with [vector 1 / 0 / 0] over [number {1} sec]] on [self] | vector: The positon in world space that the object moves to number: The number of seconds it takes to move object: The object that the motion applies to | Moves the object along a line from its current position to a new coordinate over the given time. | |
| Move by over time | action [move with [vector 1 / 0 / 0] over [number {1} sec]] on [self] | vector: The direction and distance the object will move by number: The number of seconds it takes to move object: The object that the motion applies to | Moves the object along a line from its current position to a new coordinate that is the sum of the current position and the given coordinate, over the given time. | |
| Rotate to over time | action [rotateto with [rotation 90 / 0 / 0] over [number {1} sec]] on [self] | rotation: The angle the object will rotate to number: the number of seconds it takes to rotate object: The object that the motion applies to | Rotates the object from its current rotation to the given rotation over the given time. |
| Rotate by over time | action [rotate with [rotation 90 / 0 / 0] over [number {1} sec]] on [self] | rotation: The angle the object will rotate by number: the number of seconds it takes to rotate object: The object that the motion applies to | Rotates the object from its current rotation by the given rotation over the given time. | |
| Scale to over time | action [scale with [vector 1/ 1/ 1] over [number {1} sec]] on [self] | vector: The size the object will scale to number: the number of seconds it takes to scale object: The object that the motion applies to | Scales the object from its current scale to the given scale over the given time. |
| **Player Motion**  |   |   |   |   |
| Respawn player | action [respawn with [param]] on [self] | playerid: The player that will be respawned object: The spawn point to respawn them to | Teleports a player to a spawn point. | |
| **Physical Motion**  |   |   |   |   |
| Disable object physical motion | disable [self] physical motion | object: The object that physical motion is being disabled on | Locks a physics object in place. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| Enable object physical motion | enable [self] physical motion | object: The object that physical motion is being enabled on | Unlocks a physics object, allowing it to be moved. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| Push | action [+Velocity with [vector 1/ 1/ 1]] on [self] | vector: The velocity being added object: The object that physical motion is being applied to | The object's velocity becomes equal to its current velocity, plus the given velocity. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| Push with mass | action [+impulse with [vector 1/ 0/ 0]] on [self] | vector: The velocity being added object: The object that physical motion is being applied to | The object's velocity becomes equal to its current velocity, plus the given velocity divided by the object's mass (heavier objects have their velocity adjusted less). | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| Push in local space | action [+VelLocal with [vector 1/ 0/ 0]] on [self] | vector: The velocity being added object: The object that physical motion is being applied to | The given velocity is rotated to the object's rotation, then a Push runs (x becomes left/right, y becomes above/below, z becomes forward/backward). | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| Push in local space with mass | action [+ImpLocal with [vector 1/ 0 / 0]] on [self] | vector: The velocity being added object: The object that physical motion is being applied to | The given velocity is rotated to the object's rotation, then a Push with Mass runs (x becomes left/right, y becomes above/below, z becomes forward/backward). | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| Spin | action [+AngVel with [vector 1/ 0/ 0]] on [self] | vector: The angular velocity being added object: The object that physical motion is being applied to | The object's angular velocity becomes equal to its current angular velocity, plus the given angular velocity. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| Spin in local space | action [+AngVelLocal with [vector 1/ 0/ 0]] on [self] | vector: The angular velocity being added object: The object that physical motion is being applied to | The given velocity is rotated to the object's current rotation, then a Spin runs (x becomes pitch, y becomes yaw, z becomes roll). | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| Stop physical motion | stop physical motion [self] | object: The object that the physical motion is being stopped on | The object's velocity and angular velocity both become zero. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| Launch from object | action [LaunchFrom with [self] [number {10}]] on [self] | object: The object whose position and direction will be used to launch from number: The speed to launch it at object: The object that will be launched | Makes the object become owned by the same owner of the "launch from" object (i.e. object specified by the first parameter), sets the position and rotation of the object to match that of the "launch from" object, and then sets the object's velocity to match its forward direction with a magnitude (speed) equal to the value of the second parameter. | Note: The object being manipulated must be marked as "Interactive" with "Physics" in the properties panel of the object. |
| **Actions Tab**  |   |   |   |   |
| **Object**  |   |   |   |   |
| Show object | show [self] | object: The object that will turn visible | Makes object visible in your world. | Note: This will currently also affect collisions on an object. The object will be made collidable. |
| Hide object | hide [self] | object: The object that will turn hidden | Hides the object in your world. | Note: This will currently also affect collisions on an object. The object will have collisions turned off. |
| Paint object | action color with [color 1/ 0/ 0] on [self] | color: The rgb color to paint the object with object: The object that will be painted | Sets the color of the object. |
| Enable object | enable [self] | object: The trigger that will be enabled | Enables a trigger's ability to detect people or objects. This can only be used on triggers. | |
| Disable object | disable [self] | object: The trigger that will be disabled | Disables a trigger's ability to detect people or objects. This can only be used on triggers. | |
| Set simulated | action [setsimulated with boolean {true/false}] on [self] | boolean: The true or false value that the simulated property will be set to object: The object that will have its simulation set | Enables or disables the "simulated" property. If off, the object cannot move. | |
| Set gravity | action [setgravity with boolean {true/false}] on [self] | boolean: The true or false value that the gravity property will be set to object: The object that will have its simulation set | Enables or disables gravity simulation on this object.If on, the object will fall to the floor. If off, it wil act like it's floating in space. | |
| **Text** |   |   |   |   |
| Display text | action [display with [number {1}]] on [self] | string/number: The value the text gizmo will display object: The text gizmo that displays the string/number | Sets the displayed text in the text gizmo. | |
| **Animation** |   |   |   |   |
| Play animation | play animation on [self] | object: The object that will play its animation | Plays the object's animation. | |
| Pause animation | pause animation on [self] | object: The object that will pause its animation | Pauses the object's animation. | |
| Stop animation | stop animation on [self] | object: The object to stop its animation |
| **Sound** |   |   |   |   |
| Play sound | play sound on [self] | object: The sound gizmo that will play | Plays a sound gizmo. | Note: A sound must be stopped before it can be played again. |
| Pause sound | pause sound on [self] | object: The sound gizmo that will pause | Pauses a sound gizmo. | Note: A sound must be stopped before it can be played again. |
| Stop sound | stop sound on [self] | object: The sound gizmo that will stop | Stops a sound gizmo. | Note: A sound must be stopped before it can be played again. |
| **Particles and Trails** |   |   |   |   |
| Play visual fx | play visual effects on [self] | object: The visual effect gizmo that will play | Plays a visual effects gizmo. | |
| Stop visual fx | stop visual effects on [self] | object: The visual effect gizmo that will stop | Stops a visual effects gizmo. | |
| **World**  |   |   |   |   |
| Reset world state | reset world state | | Resets the world back to its inital state. | |
| **Math**  |   |   |   |   |
| **Logic**  |   |   |   |   |
|












































