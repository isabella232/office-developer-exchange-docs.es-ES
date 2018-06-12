---
title: base64FolderId (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- base64FolderId
api_type:
- schema
ms.assetid: 662f8f2f-49a7-4c7a-9065-98a02a49cfcd
description: El elemento base64FolderId contiene el identificador de la carpeta para especificar como la carpeta de correo electrónico predeterminada desde la que mensajería unificada lee los mensajes a través del teléfono en una solicitud de SetTelephoneAccessFolderEmail operación (servicio web de mensajería unificada).
ms.openlocfilehash: 7d710542418a717c6fcad243a22682e5840ebbd2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763604"
---
# <a name="base64folderid-um-web-service"></a><span data-ttu-id="e8366-103">base64FolderId (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="e8366-103">base64FolderId (UM web service)</span></span>

<span data-ttu-id="e8366-104">El elemento **base64FolderId** contiene el identificador de la carpeta para especificar como la carpeta de correo electrónico predeterminada desde la que mensajería unificada lee los mensajes a través del teléfono en una solicitud de [operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="e8366-104">The **base64FolderId** element contains the identifier of the folder to specify as the default e-mail folder from which Unified Messaging reads messages over the telephone in a [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="e8366-105">SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="e8366-105">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="e8366-106">base64FolderId (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="e8366-106">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 <span data-ttu-id="e8366-107">**string**</span><span class="sxs-lookup"><span data-stu-id="e8366-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8366-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e8366-108">Attributes and elements</span></span>

<span data-ttu-id="e8366-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e8366-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8366-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="e8366-110">Attributes</span></span>

<span data-ttu-id="e8366-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e8366-111">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8366-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e8366-112">Child elements</span></span>

<span data-ttu-id="e8366-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e8366-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e8366-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e8366-114">Parent elements</span></span>

|<span data-ttu-id="e8366-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8366-115">**Element**</span></span>|<span data-ttu-id="e8366-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8366-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8366-117">SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="e8366-117">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md) <br/> |<span data-ttu-id="e8366-118">Define la solicitud para establecer la carpeta de correo electrónico de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="e8366-118">Defines request to set the telephone access e-mail folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e8366-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e8366-119">Text value</span></span>

<span data-ttu-id="e8366-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="e8366-120">A text value is required.</span></span> <span data-ttu-id="e8366-121">El valor de texto representa el identificador de MAPI de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e8366-121">The text value represents the MAPI ID of the folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8366-122">Notas</span><span class="sxs-lookup"><span data-stu-id="e8366-122">Remarks</span></span>

<span data-ttu-id="e8366-123">Para establecer la carpeta de correo electrónico de acceso telefónico, use la [operación de SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="e8366-123">To set the telephone access e-mail folder, use the [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8366-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e8366-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8366-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e8366-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e8366-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e8366-126">Schema Name</span></span>  <br/> |<span data-ttu-id="e8366-127">Mensajes</span><span class="sxs-lookup"><span data-stu-id="e8366-127">Messages</span></span>  <br/> |
|<span data-ttu-id="e8366-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e8366-128">Validation File</span></span>  <br/> |<span data-ttu-id="e8366-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e8366-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e8366-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e8366-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8366-131">False</span><span class="sxs-lookup"><span data-stu-id="e8366-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8366-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="e8366-132">See also</span></span>



[<span data-ttu-id="e8366-133">SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="e8366-133">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="e8366-134">Operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="e8366-134">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[<span data-ttu-id="e8366-135">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="e8366-135">FindFolder operation</span></span>](findfolder-operation.md)
  
[<span data-ttu-id="e8366-136">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="e8366-136">FindItem operation</span></span>](finditem-operation.md)

