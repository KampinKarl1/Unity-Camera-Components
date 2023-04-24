# Unity-Camera-Components
**Raycaster**
TLDR: Don't use the raycaster because it's a clump of shit right now.
Idea: I was raycasting a lot and reusing a lot of the same information in various scripts so I made a raycasting script with hopes to improve performance and not generate duplicate code. I ended up with a real crappy script that tries to do the job of everything... it should probably just hold a RaycastHit for the current frame and possibly the last few frames as well so you could do, for example, a comparison of the objects that were hit (if any were hit) to say, "Okay, if I hit an interactable object on the last frame but am not hitting the same object on this frame, I want to close or change the prompt for interaction."

**Scene Like Camera**
Whenever I press play when I'm prototyping or something, I sort of expect to be able to look at the scene as I would in Scene mode and am, still after 7 years in Unity, surprised when I have no camera control. This is a simple camera controller for giving you pretty much the same controls for the camera in Play mode as you would have in Scene mode. Use it for RTS style games, strategy/city-builders, et cetera.

**SniperMouseLook**
This just builds on one of Unity's old Standard Assets. It came from the RigidbodyFirstPersonController's MouseLook. As the name implies, it allows you to look around (rotate) with movement of the mouse. *It reduces* sensitivity of movement when you're trying to be more precise like when sniping. So, if over the course of a few frames you haven't moved the mouse very much, the x and y sensitivities are effectively reduced. You could just consider this as giving mouse looking some acceleration/deceleration.
