---
title: base64FolderId (servicio Web de mensajería unificada)
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
description: El elemento base64FolderId contiene el identificador de la carpeta que se va a especificar como carpeta de correo electrónico predeterminada desde la que la mensajería unificada Lee los mensajes a través del teléfono en una solicitud SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada).
ms.openlocfilehash: ea31c7a0f93188e563bf95c4a3e6e91f0866746c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458050"
---
# <a name="base64folderid-um-web-service"></a><span data-ttu-id="ed895-103">base64FolderId (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="ed895-103">base64FolderId (UM web service)</span></span>

<span data-ttu-id="ed895-104">El elemento **base64FolderId** contiene el identificador de la carpeta que se va a especificar como carpeta de correo electrónico predeterminada desde la que la mensajería unificada Lee los mensajes a través del teléfono en una solicitud [SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="ed895-104">The **base64FolderId** element contains the identifier of the folder to specify as the default e-mail folder from which Unified Messaging reads messages over the telephone in a [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="ed895-105">SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="ed895-105">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="ed895-106">base64FolderId (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="ed895-106">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 <span data-ttu-id="ed895-107">**string**</span><span class="sxs-lookup"><span data-stu-id="ed895-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed895-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ed895-108">Attributes and elements</span></span>

<span data-ttu-id="ed895-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ed895-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed895-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ed895-110">Attributes</span></span>

<span data-ttu-id="ed895-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ed895-111">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed895-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ed895-112">Child elements</span></span>

<span data-ttu-id="ed895-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ed895-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ed895-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ed895-114">Parent elements</span></span>

|<span data-ttu-id="ed895-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ed895-115">**Element**</span></span>|<span data-ttu-id="ed895-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ed895-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed895-117">SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="ed895-117">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md) <br/> |<span data-ttu-id="ed895-118">Define la solicitud para establecer la carpeta de correo electrónico de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="ed895-118">Defines request to set the telephone access e-mail folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ed895-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ed895-119">Text value</span></span>

<span data-ttu-id="ed895-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="ed895-120">A text value is required.</span></span> <span data-ttu-id="ed895-121">El valor de texto representa el identificador MAPI de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ed895-121">The text value represents the MAPI ID of the folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed895-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed895-122">Remarks</span></span>

<span data-ttu-id="ed895-123">Para establecer la carpeta de correo electrónico de acceso telefónico, use la [operación SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="ed895-123">To set the telephone access e-mail folder, use the [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed895-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ed895-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed895-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed895-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ed895-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ed895-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ed895-127">Mensajes</span><span class="sxs-lookup"><span data-stu-id="ed895-127">Messages</span></span>  <br/> |
|<span data-ttu-id="ed895-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ed895-128">Validation File</span></span>  <br/> |<span data-ttu-id="ed895-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ed895-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed895-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ed895-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed895-131">Falso</span><span class="sxs-lookup"><span data-stu-id="ed895-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed895-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed895-132">See also</span></span>



[<span data-ttu-id="ed895-133">SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="ed895-133">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="ed895-134">Operación SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="ed895-134">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[<span data-ttu-id="ed895-135">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="ed895-135">FindFolder operation</span></span>](findfolder-operation.md)
  
[<span data-ttu-id="ed895-136">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="ed895-136">FindItem operation</span></span>](finditem-operation.md)

