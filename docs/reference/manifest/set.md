---
title: Set element in the manifest file
description: The Set element specifies an Office JavaScript API requirement set your Office Add-in requires in order to activate.
ms.date: 03/19/2019
ms.localizationpriority: medium
---

# Set element

Specifies a requirement set from the Office JavaScript API that your Office Add-in requires to activate.

**Add-in type:** Content, Task pane, Mail

## Syntax

```XML
<Set Name="string" MinVersion="n .n">
```

## Contained in

[Sets](sets.md)

## Attributes

|Attribute|Type|Required|Description|
|:-----|:-----|:-----|:-----|
|Name|string|required|The name of a [requirement set](../../develop/office-versions-and-requirement-sets.md).|
|MinVersion|string|optional|Specifies the minimum version of the API set required by your add-in. Overrides the value of **DefaultMinVersion**, if it is specified in the parent [Sets](sets.md) element.|

## Remarks

For more information about requirement sets, see [Office versions and requirement sets](../../develop/office-versions-and-requirement-sets.md).

For more information about the **MinVersion** attribute of the **Set** element and the **DefaultMinVersion** attribute of the **Sets** element, see [Set the Requirements element in the manifest](../../develop/specify-office-hosts-and-api-requirements.md#set-the-requirements-element-in-the-manifest).

> [!IMPORTANT]
> For mail add-ins, there is only one  `"Mailbox"` requirement set available. This requirement set contains the entire subset of API supported in mail add-ins for Outlook, and you must specify the `"Mailbox"` requirement set in your mail add-in's manifest (it's not optional as is the case for content and task pane add-ins). Also, you can't declare support for specific methods in mail add-ins.
