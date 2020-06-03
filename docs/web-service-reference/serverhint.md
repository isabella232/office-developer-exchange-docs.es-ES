---
title: ServerHint
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServerHint
api_type:
- schema
ms.assetid: 5ac60472-a565-43d1-a5fb-8be0c9511f82
description: El elemento ServerHint representa el punto de inicio para el seguimiento de un mensaje en un bosque o sitio remoto.
ms.openlocfilehash: 76a719901f4e4d1da67ce377ab8b73e4a4592dc4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461992"
---
# <a name="serverhint"></a><span data-ttu-id="22ad9-103">ServerHint</span><span class="sxs-lookup"><span data-stu-id="22ad9-103">ServerHint</span></span>

<span data-ttu-id="22ad9-104">El elemento **ServerHint** representa el punto de inicio para el seguimiento de un mensaje en un bosque o sitio remoto.</span><span class="sxs-lookup"><span data-stu-id="22ad9-104">The **ServerHint** element represents the starting point for tracking a message in a remote site or forest.</span></span> 
  
```xml
<ServerHint/>
```

 <span data-ttu-id="22ad9-105">**string**</span><span class="sxs-lookup"><span data-stu-id="22ad9-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22ad9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="22ad9-106">Attributes and elements</span></span>

<span data-ttu-id="22ad9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="22ad9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22ad9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="22ad9-108">Attributes</span></span>

<span data-ttu-id="22ad9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="22ad9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22ad9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="22ad9-110">Child elements</span></span>

<span data-ttu-id="22ad9-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="22ad9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="22ad9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="22ad9-112">Parent elements</span></span>

|<span data-ttu-id="22ad9-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="22ad9-113">**Element**</span></span>|<span data-ttu-id="22ad9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22ad9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22ad9-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="22ad9-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="22ad9-116">Especifica los criterios para los tipos de mensajes que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="22ad9-116">Specifies criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="22ad9-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="22ad9-117">Text value</span></span>

<span data-ttu-id="22ad9-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="22ad9-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="22ad9-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22ad9-119">Remarks</span></span>

<span data-ttu-id="22ad9-120">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="22ad9-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22ad9-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="22ad9-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22ad9-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="22ad9-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="22ad9-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="22ad9-123">Schema Name</span></span>  <br/> |<span data-ttu-id="22ad9-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="22ad9-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="22ad9-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="22ad9-125">Validation File</span></span>  <br/> |<span data-ttu-id="22ad9-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="22ad9-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="22ad9-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="22ad9-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="22ad9-128">Falso</span><span class="sxs-lookup"><span data-stu-id="22ad9-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22ad9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="22ad9-129">See also</span></span>



[<span data-ttu-id="22ad9-130">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="22ad9-130">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="22ad9-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="22ad9-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

