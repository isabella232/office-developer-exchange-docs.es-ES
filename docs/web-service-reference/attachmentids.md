---
title: AttachmentIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentIds
api_type:
- schema
ms.assetid: 46ce3ad7-4b20-43ae-8c63-39f1e3c2666b
description: El elemento AttachmentIds contiene una matriz de identificadores de los datos adjuntos.
ms.openlocfilehash: f205aefe6a7dc4ec208e8a96b8a6b47094aa741b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763570"
---
# <a name="attachmentids"></a><span data-ttu-id="b8f3e-103">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="b8f3e-103">AttachmentIds</span></span>

<span data-ttu-id="b8f3e-104">El elemento **AttachmentIds** contiene una matriz de identificadores de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-104">The **AttachmentIds** element contains an array of attachment identifiers.</span></span> 
  
```xml
<AttachmentIds>
   <AttachmentId Id=""/>
</AttachmentIds>
```

 <span data-ttu-id="b8f3e-105">**NonEmptyArrayOfRequestAttachmentIdsType**</span><span class="sxs-lookup"><span data-stu-id="b8f3e-105">**NonEmptyArrayOfRequestAttachmentIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8f3e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b8f3e-106">Attributes and elements</span></span>

<span data-ttu-id="b8f3e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8f3e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8f3e-108">Attributes</span></span>

<span data-ttu-id="b8f3e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8f3e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8f3e-110">Child elements</span></span>

|<span data-ttu-id="b8f3e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8f3e-111">**Element**</span></span>|<span data-ttu-id="b8f3e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8f3e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8f3e-113">AttachmentId (GetAttachment y DeleteAttachment)</span><span class="sxs-lookup"><span data-stu-id="b8f3e-113">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md) <br/> |<span data-ttu-id="b8f3e-114">El elemento que identifica un solo dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-114">The element that identifies a single attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b8f3e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b8f3e-115">Parent elements</span></span>

|<span data-ttu-id="b8f3e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8f3e-116">**Element**</span></span>|<span data-ttu-id="b8f3e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8f3e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8f3e-118">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="b8f3e-118">DeleteAttachment</span></span>](deleteattachment.md) <br/> |<span data-ttu-id="b8f3e-119">El elemento que define una solicitud para eliminar un archivo adjunto desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-119">The element that defines a request to delete an attachment from the Exchange store.</span></span>  <br/> <span data-ttu-id="b8f3e-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="b8f3e-120">The following is the XPath expression to this element:</span></span>  <br/>  `/DeleteAttachment` <br/> |
|[<span data-ttu-id="b8f3e-121">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="b8f3e-121">GetAttachment</span></span>](getattachment.md) <br/> |<span data-ttu-id="b8f3e-122">El elemento que define una solicitud para obtener datos adjuntos desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-122">The element that defines a request to get an attachment from the Exchange store.</span></span>  <br/> <span data-ttu-id="b8f3e-123">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="b8f3e-123">The following is the XPath expression to this element:</span></span>  <br/>  `/GetAttachment` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8f3e-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8f3e-124">Remarks</span></span>

<span data-ttu-id="b8f3e-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8f3e-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b8f3e-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8f3e-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8f3e-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b8f3e-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b8f3e-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b8f3e-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b8f3e-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b8f3e-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b8f3e-130">Validation File</span></span>  <br/> |<span data-ttu-id="b8f3e-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b8f3e-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b8f3e-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b8f3e-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b8f3e-133">False</span><span class="sxs-lookup"><span data-stu-id="b8f3e-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8f3e-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8f3e-134">See also</span></span>

- [<span data-ttu-id="b8f3e-135">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="b8f3e-135">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="b8f3e-136">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="b8f3e-136">GetAttachment operation</span></span>](getattachment-operation.md)

