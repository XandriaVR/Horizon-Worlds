# Horizon-Worlds
## How do I use code blocks in Horizon Worlds?
Source: https://support.oculus.com/487096395667734

| Item in Library | Item in Folder  | Parameters      | Description     | Tips            |
| --------------- | --------------- | --------------- | --------------- | --------------- |
| Events  |   |   |   |   |
| When world is started | When world is started | | Event runs when world starts. This will happen when the first person enters the world's instance. | |
| When event is received | When event[myevent] with [obj] is received | | Event runs when a custom event is received by this object. The custom event can be sent by the same script or a script on another object. | |
| When trigger is entered by object | When event [triggerenter] with [obj] is received | Object: The object that entered trigger | Event runs when an object enters the trigger gizmo. | Note: The trigger must be configured to detect objects with a specific tag, and the object must have that tag. |

