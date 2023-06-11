# Game_programming_exp06
EXP 06 - AI RANDOM MOVEMENT

AIM:
To implement AI concept to the actor for a random movement.

ALGORITHM:
~~~
STEP 1: Create a Character Blueprint:
In the Content Browser, right-click in the desired folder
Select Create Basic Asset > Blueprint Class.
Choose the appropriate parent class for your AI character (e.g., Character or Pawn).
Name the Blueprint (e.g., "AICharacter") and click Create.


STEP 2: Create a Blackboard:
In the Content Browser, right-click in the desired folder.
Select Create Basic Asset > AI > Blackboard.
Name the Blackboard (e.g., "AIBlackboard") and click Create.


STEP 3: Open the Behavior Tree editor:
In the Content Browser, find the Blackboard asset you just created.
Right-click the Blackboard asset and select Create > Behavior Tree.
Name the Behavior Tree (e.g., "AIBehaviorTree") and click Create.
Double-click the Behavior Tree asset to open it in the Behavior Tree editor

STEP 4: Create Behavior Tree nodes:
In the Behavior Tree editor, right-click in the graph and search for and add the following nodes:
"Selector" node: Controls the execution of child nodes.
"Service" node: Monitors and updates values in the Blackboard.
"Sequence" node: Executes child nodes in sequential order.
"Random" decorator: Randomly selects a child node to execute.
"Move To" task: Moves the AI character to a specified location.
Connect the nodes to create the desired behavior flow.
Connect the nodes to create the desired behavior flow. For example:
Connect the Random decorator to the Sequence node.
Connect the Move To task to one of the child nodes of the Random decorator.

STEP 5: Set up the Blackboard:
Open the AIBlackboard asset.
In the Blackboard editor, define the necessary keys for storing data, such as:
Vector keys: for storing target locations.
Bool keys: for storing condition flags.
Save the AIBlackboard asset.

STEP 6: Set up the AI character Blueprint:
Open the AICharacter Blueprint.
In the Blueprint editor, find the Components panel.
Add an AI Controller component to the AICharacter Blueprint.
In the Details panel, under the AI Controller section, set the AIController Class to the desired AI controller class (e.g., AIController).
Save the AICharacter Blueprint

STEP 7: Set the AI controller and behavior tree:
Open the AIController Blueprint.

In the Blueprint editor, locate the Event Begin Play event.

Drag off the execution line and search for "Possess".

In the Possess node, select the AICharacter Blueprint you created.

Drag off the AICharacter reference and search for "Use Blackboard".

Connect the output of the Use Blackboard node to the AIController's Blackboard property.

In the Blackboard property, select the AIBlackboard asset you created.

Drag off the AICharacter reference again and search for "Run Behavior Tree".

Connect the output of the Run Behavior Tree node to the AIController's Behavior Tree property.

In the Behavior Tree property, select the AIBehaviorTree asset you created.

Save the AIController Blueprint.


STEP 8: Set up the NavMesh and boundaries:
Place a NavMeshBoundsVolume in your level to define the AI character's movement boundaries.

Adjust the size and position of the NavMeshBoundsVolume to cover the desired playable area
~~~
OUTPUT:

![e1](https://github.com/Sharmilasha/Game_programming_exp06/assets/94506182/01037e92-1259-4907-9915-7d129be6a930)
![ee2](https://github.com/Sharmilasha/Game_programming_exp06/assets/94506182/7cad5cd8-f637-4820-b365-eb3e8a8bec6e)
![ee3](https://github.com/Sharmilasha/Game_programming_exp06/assets/94506182/1fde6da7-79f9-4894-be6b-85cac8205c50)
![ee4](https://github.com/Sharmilasha/Game_programming_exp06/assets/94506182/5c9fa49d-dbde-4d78-aa64-a03654abf9e1)
![ee5](https://github.com/Sharmilasha/Game_programming_exp06/assets/94506182/b50b21c9-e278-4cc7-9b5c-bd563d06f821)
![ee6](https://github.com/Sharmilasha/Game_programming_exp06/assets/94506182/e7d8cc77-92d6-4a45-b65f-ce0e10326143)

RESULT:
Thus, the AI concept to the actor for a random movement is implemented.
