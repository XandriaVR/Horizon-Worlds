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

