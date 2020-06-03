---
title: ContentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentId
api_type:
- schema
ms.assetid: bc59100d-6079-414b-a6e0-7c15feaa3184
description: El elemento ContentId representa un identificador para el contenido de los datos adjuntos. ContentId se puede establecer en cualquier valor de cadena. Las aplicaciones pueden usar ContentId para implementar sus propios mecanismos de identificación.
ms.openlocfilehash: ca89c8790e839326412003f26b738ad1ee956211
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529269"
---
# <a name="contentid"></a><span data-ttu-id="4a31b-105">ContentId</span><span class="sxs-lookup"><span data-stu-id="4a31b-105">ContentId</span></span>

<span data-ttu-id="4a31b-106">El elemento **contentid** representa un identificador para el contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4a31b-106">The **ContentId** element represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="4a31b-107">**Contentid** se puede establecer en cualquier valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="4a31b-107">**ContentId** can be set to any string value.</span></span> <span data-ttu-id="4a31b-108">Las aplicaciones pueden usar **contentid** para implementar sus propios mecanismos de identificación.</span><span class="sxs-lookup"><span data-stu-id="4a31b-108">Applications can use **ContentId** to implement their own identification mechanisms.</span></span> 
  
```xml
<ContentId/>
```

 <span data-ttu-id="4a31b-109">**String**</span><span class="sxs-lookup"><span data-stu-id="4a31b-109">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4a31b-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4a31b-110">Attributes and elements</span></span>

<span data-ttu-id="4a31b-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4a31b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a31b-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="4a31b-112">Attributes</span></span>

<span data-ttu-id="4a31b-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4a31b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4a31b-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4a31b-114">Child elements</span></span>

<span data-ttu-id="4a31b-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4a31b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4a31b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4a31b-116">Parent elements</span></span>

|<span data-ttu-id="4a31b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a31b-117">**Element**</span></span>|<span data-ttu-id="4a31b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a31b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a31b-119">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="4a31b-119">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="4a31b-120">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4a31b-120">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="4a31b-121">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="4a31b-121">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="4a31b-122">Representa un archivo que está adjunto a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4a31b-122">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4a31b-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4a31b-123">Text value</span></span>

<span data-ttu-id="4a31b-124">El valor de cadena representa el identificador para el contenido de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4a31b-124">The string value represents the identifier to the contents of an attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a31b-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a31b-125">Remarks</span></span>

<span data-ttu-id="4a31b-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4a31b-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a31b-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4a31b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a31b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a31b-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4a31b-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4a31b-129">Schema name</span></span>  <br/> |<span data-ttu-id="4a31b-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4a31b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="4a31b-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4a31b-131">Validation file</span></span>  <br/> |<span data-ttu-id="4a31b-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4a31b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4a31b-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4a31b-133">Can be empty</span></span>  <br/> |<span data-ttu-id="4a31b-134">Falso</span><span class="sxs-lookup"><span data-stu-id="4a31b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a31b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a31b-135">See also</span></span>



- [<span data-ttu-id="4a31b-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4a31b-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

