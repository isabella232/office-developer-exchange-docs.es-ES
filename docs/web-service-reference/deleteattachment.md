---
title: DeleteAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 43d0c1cb-92ca-4399-9b3a-acb2b5c22624
description: El elemento DeleteAttachment es el elemento raíz en una solicitud para eliminar un archivo adjunto desde el almacén de Exchange.
ms.openlocfilehash: 2beedd647febf025f6e3140ec37b196c9aeb7611
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764076"
---
# <a name="deleteattachment"></a><span data-ttu-id="b02eb-103">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="b02eb-103">DeleteAttachment</span></span>

<span data-ttu-id="b02eb-104">El elemento **DeleteAttachment** es el elemento raíz en una solicitud para eliminar un archivo adjunto desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b02eb-104">The **DeleteAttachment** element is the root element in a request to delete an attachment from the Exchange store.</span></span> 
  
```xml
<DeleteAttachment>
   <AttachmentIds/>
</DeleteAttachment>
```

<span data-ttu-id="b02eb-105">**DeleteAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="b02eb-105">**DeleteAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b02eb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b02eb-106">Attributes and elements</span></span>

<span data-ttu-id="b02eb-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b02eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b02eb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b02eb-108">Attributes</span></span>

<span data-ttu-id="b02eb-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b02eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b02eb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b02eb-110">Child elements</span></span>

|<span data-ttu-id="b02eb-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b02eb-111">**Element**</span></span>|<span data-ttu-id="b02eb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b02eb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b02eb-113">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="b02eb-113">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="b02eb-114">Contiene una matriz de identificadores de los datos adjuntos que se usan para eliminar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b02eb-114">Contains an array of attachment identifiers that are used to delete the attachments.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b02eb-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b02eb-115">Parent elements</span></span>

<span data-ttu-id="b02eb-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b02eb-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b02eb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b02eb-117">Remarks</span></span>

<span data-ttu-id="b02eb-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b02eb-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b02eb-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b02eb-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b02eb-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b02eb-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b02eb-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b02eb-121">Schema Name</span></span>  <br/> |<span data-ttu-id="b02eb-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b02eb-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b02eb-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b02eb-123">Validation File</span></span>  <br/> |<span data-ttu-id="b02eb-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b02eb-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b02eb-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b02eb-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="b02eb-126">False</span><span class="sxs-lookup"><span data-stu-id="b02eb-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b02eb-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="b02eb-127">See also</span></span>

- [<span data-ttu-id="b02eb-128">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="b02eb-128">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

