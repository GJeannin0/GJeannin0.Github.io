# Inspector Aer Editor Tool Technical Document

## Role

It's a window where the user can see and modify components and attributes of the scene's entities.
My task was to implement the UI for adding and removing components and to display, change and add layers & tags to entities.

## Client

The tool will be used by the third year students to view and modify entities and their components in the neko engine.
My referent for the tool is Lucas Floreau, he's the lead programmer of the project.

## State of the tool

The tool is finished.

![inspector](/images/Inspector.png)

It displays the tag and layer lists in dropdowns, the user can set the tag and layer of an entity by selecting one in the dropdown.
The components part contains buttons to add any component to the entity, and shows a delete button for each component the entity has.


## How does it work

It uses the hierarchy to select an entity, from there it displays the entity's components.

![transform](/images/Transform.png)

Then it accesses the existing tags and layers vectors from the sceneManager, and convert them to a char* array for ImGUI to use in a dropdown.
To create a new tag or layer the user can type a name and then press the add button below the text input, the inspector then create the new tag or layer via the sceneManager.

![tag](/images/Tag.png)

There is an add and a delete button for every component type, the delete buttons are only visible on entities that have the corresponding component.

![buttons](/images/Buttons.png)


Code : https://github.com/SAE-Institute-Geneva/AerRacers.git 
Branch : tool/engine/inspector_hierarchy_hot_fix
