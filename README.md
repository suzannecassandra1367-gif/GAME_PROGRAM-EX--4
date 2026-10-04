# GAME_PROGRAM-EX--4

## AIM
To create an aiming system (attach and aim a rifle with a character) in Unreal Engine,you’re using a third-person character and a rifle skeletal mesh.

## Procedure
1.Attach the Rifle to the Character Import the Rifle Skeletal Mesh into Unreal Engine. Open your Character Blueprint (e.g., BP_ThirdPersonCharacter). In the Components tab: Add a Skeletal Mesh or Static Mesh component (name it Rifle). Set its Skeletal Mesh to your rifle asset.

2.Attach the Rifle to a socket on the character’s skeleton: In the Rifle component, set the Parent Socket to something like hand_r (right hand socket). manually attach in Event Graph:

Rifle->AttachToComponent(Mesh, FAttachmentTransformRules::SnapToTargetNotIncludingScale, "hand_rSocket");

Add Aiming Mechanism Create a Boolean variable called IsAiming. Set up Input in Project Settings: Go to Edit > Project Settings > Input. Add an Action Mapping named Aim (e.g., Right Mouse Button).

Adjust Camera When Aiming Add a Camera Boom and Follow Camera.

In Event Graph:
When IsAiming = true, zoom the camera in (FOV) and slightly shift it over the shoulder.

## OUTPUT

<img width="1002" height="813" alt="image" src="https://github.com/user-attachments/assets/5c87bb59-a9a4-48ce-b541-35776c60a0f6" />
<img width="1041" height="635" alt="image" src="https://github.com/user-attachments/assets/36e04f8e-05a8-4c98-ad19-818dcae02368" />

## Result:
Attach Rifle with character mesh and implementation bullet spawn from Rifle is successfully done.
