---
title: FolderChanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChanges
api_type:
- schema
ms.assetid: d3f611ed-56a4-43f8-aa65-cbd7844b827f
description: El elemento FolderChanges representa una colección de cambios para una carpeta.
ms.openlocfilehash: 7ab89e79f6babb5e93863974835685c6975d96dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764669"
---
# <a name="folderchanges"></a><span data-ttu-id="55e1e-103">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="55e1e-103">FolderChanges</span></span>

<span data-ttu-id="55e1e-104">El elemento **FolderChanges** representa una colección de cambios para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="55e1e-104">The **FolderChanges** element represents a collection of changes for a folder.</span></span> 
  
[<span data-ttu-id="55e1e-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="55e1e-105">UpdateFolder</span></span>](updatefolder.md)
  
[<span data-ttu-id="55e1e-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="55e1e-106">FolderChanges</span></span>](folderchanges.md)
  
```xml
<FolderChanges>
   <FolderChange/>
</FolderChanges>
```

 <span data-ttu-id="55e1e-107">**NonEmptyArrayOfFolderChangesType**</span><span class="sxs-lookup"><span data-stu-id="55e1e-107">**NonEmptyArrayOfFolderChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="55e1e-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="55e1e-108">Attributes and elements</span></span>

<span data-ttu-id="55e1e-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="55e1e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55e1e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="55e1e-110">Attributes</span></span>

<span data-ttu-id="55e1e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="55e1e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="55e1e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="55e1e-112">Child elements</span></span>

|<span data-ttu-id="55e1e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="55e1e-113">**Element**</span></span>|<span data-ttu-id="55e1e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55e1e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55e1e-115">FolderChange</span><span class="sxs-lookup"><span data-stu-id="55e1e-115">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="55e1e-116">Representa un único cambio que se debe realizar en una sola carpeta.</span><span class="sxs-lookup"><span data-stu-id="55e1e-116">Represents a single change to be performed on a single folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="55e1e-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="55e1e-117">Parent elements</span></span>

|<span data-ttu-id="55e1e-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="55e1e-118">**Element**</span></span>|<span data-ttu-id="55e1e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55e1e-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55e1e-120">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="55e1e-120">UpdateFolder</span></span>](updatefolder.md) <br/> |<span data-ttu-id="55e1e-121">Representa la operación que se utiliza para actualizar las propiedades de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="55e1e-121">Represents the operation that is used to update properties for a folder.</span></span>  <br/> <span data-ttu-id="55e1e-122">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="55e1e-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55e1e-123">Notas</span><span class="sxs-lookup"><span data-stu-id="55e1e-123">Remarks</span></span>

<span data-ttu-id="55e1e-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="55e1e-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55e1e-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="55e1e-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55e1e-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="55e1e-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="55e1e-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="55e1e-127">Schema Name</span></span>  <br/> |<span data-ttu-id="55e1e-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="55e1e-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="55e1e-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="55e1e-129">Validation File</span></span>  <br/> |<span data-ttu-id="55e1e-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="55e1e-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="55e1e-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="55e1e-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="55e1e-132">False</span><span class="sxs-lookup"><span data-stu-id="55e1e-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55e1e-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="55e1e-133">See also</span></span>



[<span data-ttu-id="55e1e-134">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="55e1e-134">UpdateFolder operation</span></span>](updatefolder-operation.md)

