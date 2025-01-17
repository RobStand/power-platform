---
title: Microsoft Power Platform CLI | Microsoft Docs
description: "Install Microsoft Power Platform CLI to create, debug, and deploy code components by using Power Apps component framework."
keywords: Microsoft Power Platform CLI, code components, component framework, CLI
ms.author: jdaly
author: kkanakas
ms.reviewer: jdaly
ms.date: 06/20/2022
ms.topic: overview
---

# What is Microsoft Power Platform CLI?

Microsoft Power Platform CLI is a simple, one-stop developer CLI that empowers developers and ISVs to perform various operations in Microsoft Power Platform related to environment lifecycle, authentication, and work with Microsoft Dataverse environments, solution packages, portals, code components, and so on.

Microsoft Power Platform CLI is available for use in the GCC and GCC High (US Sovereign cloud) regions. Use the command `pac auth create` for help on the `--cloud` parameter to find out about supported US Sovereign cloud environments.  

## Install Microsoft Power Platform CLI

You can use either of the following ways to install Microsoft Power Platform CLI.

### Power Platform CLI for Windows

To install Power Platform CLI for Windows, follow these steps.

1. Download and install [Microsoft Power Platform CLI](https://aka.ms/PowerAppsCLI).

1. To take advantage of all the latest capabilities, update Microsoft Power Platform CLI tooling to the latest version by using this command (not applicable for Power Platform Tools for Visual Studio Code):

    ```dotnetcli
    pac install latest
    ```

   > [!NOTE]
   > - Currently, Microsoft Power Platform CLI for Windows is supported only on Windows 10 and Windows 11.
   > - Power Platform Tools for Visual Studio Code supports Windows 10, Windows 11, Linux, and MacOS.

### Using Power Platform Tools for Visual Studio Code

Follow these steps to install Microsoft Power Platform CLI using Visual Studio Code.

1. Open [Visual Studio Code](https://code.visualstudio.com/).
1. Select the **Extensions** icon from the **Activity** panel. In the search bar, enter **Power Platform Tools**.
1. Select **Install**. Once the installation is finished, restart Visual Studio Code to see the extension within the **Terminal** window.

   > [!div class="mx-imgBorder"]
   > ![VS code extension install.](media/power-platform-vs-code-extension-install.png "VS code extension install")

   > [!NOTE]
   > Power Platform Tools for Visual Studio Code updates automatically. 

1. Optionally, you can initiate the install into Visual Studio Code directly from [Marketplace]( https://aka.ms/ppcvscode) and it will launch Visual Studio Code and commence the extension installation.

   > [!div class="mx-imgBorder"]
   > ![Launch install from Marketplace.](media/marketplace-install.png "Launch install from Marketplace")

You can also do a side-load install into Visual Studio Code by downloading the extension from the [Marketplace](https://aka.ms/ppcvscode).

## Side-load install of Power Platform Tools for Visual Studio Code

In some organizations, downloading or initiating an install over the web is prohibited. Most cases, the organization download the installation media and stores it in a secure location and verify that it is working according to their standards, before it is distributed within the organization. To support this paradigm of installation, you can go to the [Marketplace](https://aka.ms/ppcvscode) and instead of pressing the install button, press the download extension.

   > [!div class="mx-imgBorder"]
   > ![Download the extension.](media/side-load-install-1.png "Download the extension")

This is will download a file with a .vsix extension on to your workstation.
   > [!div class="mx-imgBorder"]
   > ![Extension file downloaded.](media/side-load-install-2.png "Downloaded extension")

Launch Visual Studio Code and select the **Extensions** icon, select the ellipsis on the **Extensions** side bar, and then select **Install from VSIX**.

   > [!div class="mx-imgBorder"]
   > ![Initiate install with the downloaded file.](media/side-load-install-3.png "Install from VSIX")

### Standalone Power Platform CLI

To install standalone Power Platform CLI:

1. Download and install [Microsoft Power Platform CLI](https://aka.ms/PowerAppsCLI).

1. To take advantage of all the latest capabilities, update Microsoft Power Platform CLI tooling to the latest version by using this command (not applicable for Power Platform VS Code Extension):
    ```CLI
    pac install latest

    ```
> [!NOTE]
> - Currently, Microsoft Power Platform CLI is supported only on Windows 10 and Windows 11.
> - Power Platform Tools for Visual Studio Code, and works on Windows 10, Windows 11, Linux, and macOS.

## Successful installation

Once the installation is successful, you will need to restart Visual Studio Code, upon which you will see the following notification.

   > [!div class="mx-imgBorder"]
   > ![Install notification ](media/installation-success-1.png "Install notification")

On the **Activity** bar. you'll notice the icon for the Power Platform Tools.

   > [!div class="mx-imgBorder"]
   > ![Power Platform Tools icon ](media/installation-success-3.png "icon")

The final check would be to launch the terminal window and type `pac`.

   > [!div class="mx-imgBorder"]
   > ![Power Platform Command line in the Terminal window](media/installation-success-2.png "PAC CLI in the terminal window")

## Common commands

This table lists some of the common commands used in the CLI.

|Command|Description|
|-------|-----------|
|[Admin](reference/admin-command.md)|Commands for environment lifecycle features.|
|[Auth](reference/auth-command.md)|Commands to [connect to your environment](/power-apps/developer/component-framework/import-custom-controls#connecting-to-your-environment).|
|[Application](reference/application-command.md)| Commands to install AppSource applications that are pre-requisites for the solution work in the target environment (Preview). |
|[Canvas](reference/canvas-command.md)|Commands for working with canvas app source files (Preview).|
|[Org](reference/org-command.md)|Commands for working with Dataverse environments.|
|[Package](reference/package-command.md)|Commands for working with [solution packages](../../alm/package-deployer-tool.md).|
|[Paportal](reference/paportal-command.md)|Commands for working with [Portals support for Microsoft Power Platform CLI](/power-apps/maker/portals/power-apps-cli).|
|[PCF](reference/pcf-command.md)|Commands for working with [Power Apps component framework](/power-apps/developer/component-framework/overview).|
|[Plugin](reference/plugin-command.md)|Command to create a [plug-in](/power-apps/developer/data-platform/plug-ins) project.|
|[Solution](reference/solution-command.md)|Commands for working with [Dataverse solution projects](/power-apps/maker/data-platform/solutions-overview).|
|[Telemetry](reference/telemetry-command.md)|Manages the telemetry settings.|

> [!TIP]
> For the complete list of supported commands, run the `pac` command or `pac` \<subcommand> - for example: `pac solution`.

## Uninstall Microsoft Power Platform CLI

To uninstall Microsoft Power Platform CLI tooling, run the MSI from [https://aka.ms/PowerAppsCLI](https://aka.ms/PowerAppsCLI).

To uninstall the Visual Studio Code extension, follow the same steps as installing the extension, except this time select the **Uninstall** button.

If you're a private preview participant and have an older version of CLI, follow these steps:

1. To find out where Microsoft Power Platform CLI is installed, open a command prompt and enter `where pac`.
1. Delete the PowerAppsCLI folder.
1. Open the Environment Variables tool by running the command `rundll32 sysdm.cpl,EditEnvironmentVariables` in the command prompt.
1. In the `User variable for...` section, double-click to select `Path` .
1. Select the row containing the PowerAppsCLI path, and then select **Delete** on the right side.
1. Select **OK** twice.

### See also

[Power Apps component framework](/power-apps/developer/component-framework/overview)<br />

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
