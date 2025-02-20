---
# Mandatory fields.
title: Azure Digital Twins CLI command set
titleSuffix: Azure Digital Twins
description: Learn about the Azure Digital Twins CLI command set.
author: baanders
ms.author: baanders # Microsoft employees only
ms.date: 02/28/2022
ms.topic: conceptual
ms.service: digital-twins

# Optional fields. Don't forget to remove # if you need a field.
# ms.custom: can-be-multiple-comma-separated
# ms.reviewer: MSFT-alias-of-reviewer
# manager: MSFT-alias-of-manager-or-PM-counterpart
---

# Azure Digital Twins CLI command set

Apart from managing your Azure Digital Twins instance in the Azure portal, Azure Digital Twins also has a command set for the [Azure CLI](/cli/azure/what-is-azure-cli) that you can use to do most major actions with the service. This article covers the [Azure CLI](/cli/azure/what-is-azure-cli) in terms of its uses, how to get it, and the requirements for using it.

Some of the actions you can do using the command set include:
* Managing an Azure Digital Twins instance
* Managing models
* Managing digital twins
* Managing twin relationships
* Configuring endpoints
* Managing [routes](concepts-route-events.md)
* Configuring [security](concepts-security.md) via Azure role-based access control (Azure RBAC)

The command set is called `az dt`, and is part of the [Azure IoT extension for Azure CLI](https://github.com/Azure/azure-iot-cli-extension). You can view the full list of commands and their usage as part of the reference documentation for the `az iot` command set: [az dt command reference](/cli/azure/dt).

## Uses (deploy and validate)

Apart from generally managing your instance, the CLI is also a useful tool for deployment and validation.
* The control plane commands can be used to make the deployment of a new instance repeatable or automated.
* The data plane commands can be used to quickly check values in your instance, and verify that operations completed as expected.

## Get the command set

The Azure Digital Twins commands are part of the [Azure IoT extension for Azure CLI (azure-iot)](https://github.com/Azure/azure-iot-cli-extension), so follow these steps to make sure you have the latest `azure-iot` extension with the `az dt` commands.

### CLI version requirements

If you're using the Azure CLI with PowerShell, your Azure CLI version should be 2.3.1 or above as a requirement of the extension package.

You can check the version of your Azure CLI with this CLI command:
```azurecli
az --version
```

For instructions on how to install or update the Azure CLI to a newer version, see [Install the Azure CLI](/cli/azure/install-azure-cli).

### Get the extension

The Azure CLI will automatically prompt you to install the extension on the first use of a command that requires it.

Otherwise, you can use the following command to install the extension yourself at any time (or update it if it turns out that you already have an older version). The command can be run in either the [Azure Cloud Shell](../cloud-shell/overview.md) or a [local Azure CLI](/cli/azure/install-azure-cli).

```azurecli-interactive
az extension add --upgrade --name azure-iot
```

## Next steps

Explore the CLI and its full set of commands through the reference docs:
* [az dt command reference](/cli/azure/dt)