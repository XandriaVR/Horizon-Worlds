# Horizon-Worlds
## How do I use code blocks in Horizon Worlds?
Source: https://support.oculus.com/487096395667734

| Item in Library | Item in Folder  | Parameters      | Description     | Tips            |
| --------------- | --------------- | --------------- | --------------- | --------------- |
| Events  |   |   |   |   |
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
| Connections  |   |   |   |   |
| Connect to event | connect [self] [triggerenter] to local event [enter] | object: The object the where the non-local script event fires event: The event in the non-local script event: The event in the local script that the non-local script should connect to | Connects an event in another object to an event in the local script, so when the event in the other object is triggered, the event in the local script is triggered too. | Note: This is useful for connecting multiple triggers in a script to one or multiple events in order to make a triggerable system. |
| Motion Tab  |   |   |   |   |
| Instant Motion  |   |   |   |   |
| Move to action [moveto with [vector 1 / 0 / 0]] on [self] | vector: The position in world space that the object moves to object: The object that the motion applies to | Instantly moves the object to the coordinates provided. | Note: The object being manipulated must be marked as "Interactive" or "Animated" in the properties panel of the object. |
| Move by | action [move with [vector1 / 0 / 0]] on [self] | vector: The direction and distance the object will move by object: The object that the motion applies to | Instantly moves the object relative to its current position by adding the vector to the current position. | |
| Rotate to | action [rotateto with [rotation 90 / 0 / 0]] on [self] | rotation: The angle the object will rotate to object: The object that the motion applies to | Instantly rotates the object to the rotation provided. | |
| Rotate by | action [rotate with [rotation 90/ 0 / 0]] on [self] | rotation: The angle the object will rotate by object: The object that the motion applies to | Instantly rotates the object by adding the supplied rotation to the current rotation. | |
| Scale to | action [scale with [vector 1 / 0 / 0]] on self]] | vector: The size the object will scale to object: The object that the motion applies to | Instantly sets the scale to the value provided. | |

















