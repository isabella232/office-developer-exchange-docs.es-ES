---
title: Identificadores
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
description: El elemento identificadores contiene una matriz de identificadores de datos adjuntos.
ms.openlocfilehash: cff1cb5658690fd6dd2c6a7812e1f600a4c80e29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464255"
---
# <a name="attachmentids"></a><span data-ttu-id="3f194-103">Identificadores</span><span class="sxs-lookup"><span data-stu-id="3f194-103">AttachmentIds</span></span>

<span data-ttu-id="3f194-104">El elemento **identificadores** contiene una matriz de identificadores de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="3f194-104">The **AttachmentIds** element contains an array of attachment identifiers.</span></span> 
  
```xml
<AttachmentIds>
   <AttachmentId Id=""/>
</AttachmentIds>
```

 <span data-ttu-id="3f194-105">**NonEmptyArrayOfRequestAttachmentIdsType**</span><span class="sxs-lookup"><span data-stu-id="3f194-105">**NonEmptyArrayOfRequestAttachmentIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3f194-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3f194-106">Attributes and elements</span></span>

<span data-ttu-id="3f194-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3f194-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f194-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3f194-108">Attributes</span></span>

<span data-ttu-id="3f194-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3f194-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3f194-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3f194-110">Child elements</span></span>

|<span data-ttu-id="3f194-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3f194-111">**Element**</span></span>|<span data-ttu-id="3f194-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f194-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f194-113">AttachmentId (GetAttachment y DeleteAttachment)</span><span class="sxs-lookup"><span data-stu-id="3f194-113">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md) <br/> |<span data-ttu-id="3f194-114">Elemento que identifica un solo dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="3f194-114">The element that identifies a single attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3f194-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3f194-115">Parent elements</span></span>

|<span data-ttu-id="3f194-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3f194-116">**Element**</span></span>|<span data-ttu-id="3f194-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f194-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f194-118">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="3f194-118">DeleteAttachment</span></span>](deleteattachment.md) <br/> |<span data-ttu-id="3f194-119">Elemento que define una solicitud para eliminar datos adjuntos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f194-119">The element that defines a request to delete an attachment from the Exchange store.</span></span>  <br/> <span data-ttu-id="3f194-120">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="3f194-120">The following is the XPath expression to this element:</span></span>  <br/>  `/DeleteAttachment` <br/> |
|[<span data-ttu-id="3f194-121">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="3f194-121">GetAttachment</span></span>](getattachment.md) <br/> |<span data-ttu-id="3f194-122">Elemento que define una solicitud para obtener datos adjuntos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f194-122">The element that defines a request to get an attachment from the Exchange store.</span></span>  <br/> <span data-ttu-id="3f194-123">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="3f194-123">The following is the XPath expression to this element:</span></span>  <br/>  `/GetAttachment` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f194-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f194-124">Remarks</span></span>

<span data-ttu-id="3f194-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="3f194-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f194-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3f194-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f194-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f194-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3f194-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3f194-128">Schema Name</span></span>  <br/> |<span data-ttu-id="3f194-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3f194-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3f194-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3f194-130">Validation File</span></span>  <br/> |<span data-ttu-id="3f194-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3f194-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3f194-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3f194-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="3f194-133">Falso</span><span class="sxs-lookup"><span data-stu-id="3f194-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f194-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f194-134">See also</span></span>

- [<span data-ttu-id="3f194-135">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="3f194-135">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="3f194-136">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="3f194-136">GetAttachment operation</span></span>](getattachment-operation.md)

