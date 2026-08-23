# Data Driven Event Controller (DDEC)

Welcome to **Data Driven Event Controller (DDEC)** for Unreal Engine 5.8! 

This repository establishes the core framework for managing phase-driven actor interactions cleanly and efficiently through a decoupled C++ architecture.

## 🚀 Key Architectural Highlights
* **Core C++ Subsystem**: Utilizes a centralized `UEventManagerSubsystem` running on the GameInstance to handle component registration and phase dispatching globally.
* **Event Components**: Features the `UEventComponent` to easily attach event-listening capabilities to any actor in your scene.
* **Interface-Driven Logic**: Implements `IEventInterface` to safely invoke custom `UpdateEvent` functions on targeted owners.
* **Ready-to-Use Blueprint Trigger**: Includes `BP_EventTrigger` to easily handle overlap-based or call-based scene events directly from the editor.

## ⚙️ Technical Details & Requirements
* **Engine Version**: Built and tested specifically on Unreal Engine 5.8.
* **Architecture**: Fully modular C++ plugin design with Blueprint exposure.

---
*For complete installation steps and a quick-start guide, please refer to the README instructions.*
