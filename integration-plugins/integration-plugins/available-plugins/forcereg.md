---
description: Requires players to register on the CAD via a nag screen or freezing them.
---

# ForceReg

{% hint style="warning" %}
This plugin utilizes API endpoints that require the **standard** version of Sonoran CAD or higher. For more information, view our [pricing ](../../../pricing/faq/)page.
{% endhint %}

## Installation

### 1. Download and Install the Framework

If you haven't already, be sure to install and configure the [plugin framework](../framework-installation.md) first.

### 2. Download the Plugin

1. Click [HERE ](https://github.com/Sonoran-Software/sonoran_forcereg/releases)to download the locations plugin .zip file.
2. You will also need the [apicheck](https://github.com/Sonoran-Software/sonoran_apicheck/releases) plugin.

### 3. Install the Plugin

1. Follow the [standard plugin installation guide](../plugin-installation.md) for the locations plugin.

### 4. Set Your API ID

Don't forget to set your account [API ID](../../../sonoran-cad/api-integration/getting-started/setting-your-api-id.md) to properly link your in-game user to the CAD.

## Further Configuration

| Option | Description | Default Value |
| :--- | :--- | :--- |
| captiveOption | The mode to use for telling players to sign up. | Nag |
| captiveMessage | Message to show to the player. | See Config |
| verifyMessage | Message to show how to confirm the player registered. | See Config |

## Usage

### Automated Functionality

This plugin requires no configuration by default and will show a message at the top of the screen telling players to register for the CAD. Depending on the selected option, this behavior can change.

### Event

This event is sent to the **client** after the check is completed.

```lua
Event: "SonoranCAD::forcereg:PlayerReg"

Parameters:
    identifier: The identifier checked
    exists: true/false, if the identifier is linked to a CAD account
```
