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
description: El elemento DeleteAttachment es el elemento raíz de una solicitud para eliminar datos adjuntos del almacén de Exchange.
ms.openlocfilehash: ae8dd5abc1dced2645e579a62f1f57a66cbc9877
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457350"
---
# <a name="deleteattachment"></a><span data-ttu-id="2de75-103">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="2de75-103">DeleteAttachment</span></span>

<span data-ttu-id="2de75-104">El elemento **DeleteAttachment** es el elemento raíz de una solicitud para eliminar datos adjuntos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2de75-104">The **DeleteAttachment** element is the root element in a request to delete an attachment from the Exchange store.</span></span> 
  
```xml
<DeleteAttachment>
   <AttachmentIds/>
</DeleteAttachment>
```

<span data-ttu-id="2de75-105">**DeleteAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="2de75-105">**DeleteAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2de75-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2de75-106">Attributes and elements</span></span>

<span data-ttu-id="2de75-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2de75-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2de75-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2de75-108">Attributes</span></span>

<span data-ttu-id="2de75-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2de75-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2de75-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2de75-110">Child elements</span></span>

|<span data-ttu-id="2de75-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2de75-111">**Element**</span></span>|<span data-ttu-id="2de75-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2de75-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2de75-113">Identificadores</span><span class="sxs-lookup"><span data-stu-id="2de75-113">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="2de75-114">Contiene una matriz de identificadores de datos adjuntos que se usan para eliminar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2de75-114">Contains an array of attachment identifiers that are used to delete the attachments.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2de75-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2de75-115">Parent elements</span></span>

<span data-ttu-id="2de75-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2de75-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2de75-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2de75-117">Remarks</span></span>

<span data-ttu-id="2de75-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2de75-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2de75-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2de75-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2de75-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="2de75-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2de75-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2de75-121">Schema Name</span></span>  <br/> |<span data-ttu-id="2de75-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2de75-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2de75-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2de75-123">Validation File</span></span>  <br/> |<span data-ttu-id="2de75-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2de75-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2de75-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2de75-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="2de75-126">Falso</span><span class="sxs-lookup"><span data-stu-id="2de75-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2de75-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2de75-127">See also</span></span>

- [<span data-ttu-id="2de75-128">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="2de75-128">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

