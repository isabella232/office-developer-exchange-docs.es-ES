---
title: UpdateFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolder
api_type:
- schema
ms.assetid: 412d0683-2819-40c5-a0ae-f613499a7b66
description: El elemento UpdateFolder representa la operación que se utiliza para actualizar las propiedades de una carpeta especificada.
ms.openlocfilehash: 9a86bf6b3b5917600b3b09f23b3ee4e9cdc0364f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840813"
---
# <a name="updatefolder"></a><span data-ttu-id="4c128-103">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="4c128-103">UpdateFolder</span></span>

<span data-ttu-id="4c128-104">El elemento **UpdateFolder** representa la operación que se utiliza para actualizar las propiedades de una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="4c128-104">The **UpdateFolder** element represents the operation that is used to update properties for a specified folder.</span></span> 
  
```xml
<UpdateFolder>
   <FolderChanges/>
</UpdateFolder>
```

 <span data-ttu-id="4c128-105">**UpdateFolderType**</span><span class="sxs-lookup"><span data-stu-id="4c128-105">**UpdateFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c128-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4c128-106">Attributes and elements</span></span>

<span data-ttu-id="4c128-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4c128-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c128-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c128-108">Attributes</span></span>

<span data-ttu-id="4c128-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4c128-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c128-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4c128-110">Child elements</span></span>

|<span data-ttu-id="4c128-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4c128-111">**Element**</span></span>|<span data-ttu-id="4c128-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c128-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c128-113">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="4c128-113">FolderChanges</span></span>](folderchanges.md) <br/> |<span data-ttu-id="4c128-114">Contiene una colección de cambios para una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="4c128-114">Contains a collection of changes for a specified folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4c128-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4c128-115">Parent elements</span></span>

<span data-ttu-id="4c128-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4c128-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c128-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c128-117">Remarks</span></span>

<span data-ttu-id="4c128-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4c128-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c128-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4c128-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c128-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4c128-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4c128-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4c128-121">Schema Name</span></span>  <br/> |<span data-ttu-id="4c128-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4c128-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4c128-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4c128-123">Validation File</span></span>  <br/> |<span data-ttu-id="4c128-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4c128-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4c128-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4c128-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="4c128-126">False</span><span class="sxs-lookup"><span data-stu-id="4c128-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c128-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="4c128-127">See also</span></span>



[<span data-ttu-id="4c128-128">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="4c128-128">UpdateFolder operation</span></span>](updatefolder-operation.md)

