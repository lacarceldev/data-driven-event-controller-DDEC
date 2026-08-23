# DATA DRIVEN EVENT CONTROLLER (DDEC) v1.0

This plugin is designed to make actor calls by phases in an optimal and dynamic way, by defining specific variables in scene instances. Thanks to this plugin, you can place as many actors as you want in the scene and assign them a phase value. Thus, when a trigger is activated, only the functions of those actors belonging to the same phase will be called. The system is scalable and perfect for games that require constant changes in the scene as a consequence of player progression.

This plugin was developed and tested in version 5.8 (including subsequent hotfixes). Full compatibility with other engine versions cannot be guaranteed.

---

## Plugin Contents

* **C++:** Contains an interface, a subsystem, and a component, acting as managers.
* **Blueprints:** Contains a `BP_EventTrigger`, which is the one you must place and parameterize in the scene for the system to work as desired.

---

## Installation

1. Download and extract the archive.
2. Copy the `DataDrivenEventController` folder into your project's `Plugins` directory (create the `Plugins` folder at the project root if it does not exist).
3. Open your project, navigate to **Edit -> Plugins**, locate `DataDrivenEventController`, ensure it is enabled, and restart the editor.

---

## Setup & Prerequisites

Follow these steps to configure the system:

1. In the Content Browser settings, enable **Show Plugin Content**, then navigate to `/DataDrivenEventController Content` folder.
2. Place the `BP_EventTrigger` in your scene and parameterize it. Remember that each of the instances must have a different and ascending value in the `PhaseToCall` variable.
3. In the actor you want to assign to a specific phase, add the `Event` Actor Component and implement the `EventInterface`.
4. In this actor, implement the `UpdateEvent` interface function however you wish and place the instance in your scene.
5. Remember to assign a value to the `Phase` variable of the `Event` component in your instance. The `UpdateEvent` will fire when the `BP_EventTrigger` is activated, provided its `PhaseToCall` variable has a value identical to the `Phase` variable of your actor.

---

I hope this plugin helps you streamline and organize your work in Unreal!
