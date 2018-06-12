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
ms.openlocfilehash: dc46ae4b33d435f5d47eb7deb39e92fd0170194b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763853"
---
# <a name="contentid"></a><span data-ttu-id="a4d89-105">ContentId</span><span class="sxs-lookup"><span data-stu-id="a4d89-105">ContentId</span></span>

<span data-ttu-id="a4d89-106">El elemento **ContentId** representa un identificador para el contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a4d89-106">The **ContentId** element represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="a4d89-107">**ContentId** se puede establecer en cualquier valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="a4d89-107">**ContentId** can be set to any string value.</span></span> <span data-ttu-id="a4d89-108">Las aplicaciones pueden usar **ContentId** para implementar sus propios mecanismos de identificación.</span><span class="sxs-lookup"><span data-stu-id="a4d89-108">Applications can use **ContentId** to implement their own identification mechanisms.</span></span> 
  
```xml
<ContentId/>
```

 <span data-ttu-id="a4d89-109">**String**</span><span class="sxs-lookup"><span data-stu-id="a4d89-109">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a4d89-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a4d89-110">Attributes and elements</span></span>

<span data-ttu-id="a4d89-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a4d89-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4d89-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a4d89-112">Attributes</span></span>

<span data-ttu-id="a4d89-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a4d89-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a4d89-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a4d89-114">Child elements</span></span>

<span data-ttu-id="a4d89-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a4d89-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a4d89-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a4d89-116">Parent elements</span></span>

|<span data-ttu-id="a4d89-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4d89-117">**Element**</span></span>|<span data-ttu-id="a4d89-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4d89-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4d89-119">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="a4d89-119">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="a4d89-120">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a4d89-120">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="a4d89-121">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="a4d89-121">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="a4d89-122">Representa un archivo que se adjunta a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a4d89-122">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a4d89-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a4d89-123">Text value</span></span>

<span data-ttu-id="a4d89-124">El valor de cadena representa el identificador para el contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a4d89-124">The string value represents the identifier to the contents of an attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4d89-125">Notas</span><span class="sxs-lookup"><span data-stu-id="a4d89-125">Remarks</span></span>

<span data-ttu-id="a4d89-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a4d89-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4d89-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a4d89-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4d89-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a4d89-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a4d89-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a4d89-129">Schema name</span></span>  <br/> |<span data-ttu-id="a4d89-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a4d89-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="a4d89-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a4d89-131">Validation file</span></span>  <br/> |<span data-ttu-id="a4d89-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a4d89-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a4d89-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a4d89-133">Can be empty</span></span>  <br/> |<span data-ttu-id="a4d89-134">False</span><span class="sxs-lookup"><span data-stu-id="a4d89-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4d89-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="a4d89-135">See also</span></span>



- [<span data-ttu-id="a4d89-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a4d89-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

