---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: El elemento RetentionAction especifica la acción realizada en los elementos con la etiqueta de retención.
ms.openlocfilehash: 54a1038f2e56aad66f89522423ccfbd69dc44a80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837215"
---
# <a name="retentionaction"></a><span data-ttu-id="ee579-103">RetentionAction</span><span class="sxs-lookup"><span data-stu-id="ee579-103">RetentionAction</span></span>

<span data-ttu-id="ee579-104">El elemento **RetentionAction** especifica la acción realizada en los elementos con la etiqueta de retención.</span><span class="sxs-lookup"><span data-stu-id="ee579-104">The **RetentionAction** element specifies the action performed on items with the retention tag.</span></span> 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 <span data-ttu-id="ee579-105">**RetentionActionType**</span><span class="sxs-lookup"><span data-stu-id="ee579-105">**RetentionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ee579-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ee579-106">Attributes and elements</span></span>

<span data-ttu-id="ee579-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ee579-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee579-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee579-108">Attributes</span></span>

<span data-ttu-id="ee579-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ee579-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ee579-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ee579-110">Child elements</span></span>

<span data-ttu-id="ee579-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ee579-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ee579-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ee579-112">Parent elements</span></span>

[<span data-ttu-id="ee579-113">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="ee579-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="ee579-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ee579-114">Text value</span></span>

<span data-ttu-id="ee579-115">El valor de texto del elemento **RetentionAction** es la acción realizada en los elementos.</span><span class="sxs-lookup"><span data-stu-id="ee579-115">The text value of the **RetentionAction** element is the action performed on items.</span></span> <span data-ttu-id="ee579-116">En la lista siguiente contiene los valores de texto para el elemento **RetentionAction** .</span><span class="sxs-lookup"><span data-stu-id="ee579-116">The following list contains the text values for the **RetentionAction** element.</span></span> 
  
> <span data-ttu-id="ee579-117">**Ninguno** : ninguna acción se realiza en el elemento.</span><span class="sxs-lookup"><span data-stu-id="ee579-117">**None** - No action is performed on the item.</span></span> 
    
> <span data-ttu-id="ee579-118">**MoveToDeletedItems** - el elemento se mueve a la carpeta Elementos eliminados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ee579-118">**MoveToDeletedItems** - The item is moved to the default Deleted Items folder.</span></span> 
    
> <span data-ttu-id="ee579-119">**MoveToFolder** - el elemento se mueve a una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="ee579-119">**MoveToFolder** - The item is moved to a specified folder.</span></span> 
    
> <span data-ttu-id="ee579-120">**DeleteAndAllowRecovery** - el elemento se elimina y se coloca el volcado de archivos.</span><span class="sxs-lookup"><span data-stu-id="ee579-120">**DeleteAndAllowRecovery** - The item is deleted and put into the Dumpster.</span></span> 
    
> <span data-ttu-id="ee579-121">**PermanentlyDelete** - el elemento se elimina de manera permanente del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ee579-121">**PermanentlyDelete** - The item is permanently deleted from the mailbox.</span></span> 
    
> <span data-ttu-id="ee579-122">**MarkAsPastRetentionLimit** - el elemento está marcado como que se ha excedido el límite de tiempo de retención.</span><span class="sxs-lookup"><span data-stu-id="ee579-122">**MarkAsPastRetentionLimit** - The item is marked as having exceeded the retention time limit.</span></span> 
    
> <span data-ttu-id="ee579-123">**MoveToArchive** - el elemento se mueve al buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="ee579-123">**MoveToArchive** - The item is moved to the archive mailbox.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ee579-124">Notas</span><span class="sxs-lookup"><span data-stu-id="ee579-124">Remarks</span></span>

<span data-ttu-id="ee579-125">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ee579-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ee579-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ee579-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ee579-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ee579-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee579-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ee579-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ee579-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ee579-129">Schema name</span></span>  <br/> |<span data-ttu-id="ee579-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ee579-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="ee579-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ee579-131">Validation file</span></span>  <br/> |<span data-ttu-id="ee579-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ee579-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ee579-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ee579-133">Can be empty</span></span>  <br/> ||
   

