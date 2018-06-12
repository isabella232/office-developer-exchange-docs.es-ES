---
title: ContentType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentType
api_type:
- schema
ms.assetid: f91ff0df-0d8a-43ea-a188-d80f0e885f19
description: El elemento ContentType describe el tipo de extensiones multipropósito de correo Internet (MIME) del contenido de los datos adjuntos.
ms.openlocfilehash: 489df47343051623d5b6a98557f2bd434a5dad52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763861"
---
# <a name="contenttype"></a><span data-ttu-id="4f018-103">ContentType</span><span class="sxs-lookup"><span data-stu-id="4f018-103">ContentType</span></span>

<span data-ttu-id="4f018-104">El elemento **ContentType** describe el tipo de extensiones multipropósito de correo Internet (MIME) del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4f018-104">The **ContentType** element describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span> 
  
```xml
<ContentType/>
```

 <span data-ttu-id="4f018-105">**String**</span><span class="sxs-lookup"><span data-stu-id="4f018-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f018-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4f018-106">Attributes and elements</span></span>

<span data-ttu-id="4f018-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4f018-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f018-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4f018-108">Attributes</span></span>

<span data-ttu-id="4f018-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4f018-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f018-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4f018-110">Child elements</span></span>

<span data-ttu-id="4f018-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4f018-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4f018-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4f018-112">Parent elements</span></span>

|<span data-ttu-id="4f018-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f018-113">**Element**</span></span>|<span data-ttu-id="4f018-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f018-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f018-115">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="4f018-115">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="4f018-116">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4f018-116">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="4f018-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="4f018-117">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="4f018-118">Representa un archivo que se adjunta a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4f018-118">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4f018-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4f018-119">Text value</span></span>

<span data-ttu-id="4f018-120">El valor de texto es un valor de tipo string que representa el tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4f018-120">The text value is a string value that represents the content type of the attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f018-121">Notas</span><span class="sxs-lookup"><span data-stu-id="4f018-121">Remarks</span></span>

<span data-ttu-id="4f018-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4f018-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f018-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4f018-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f018-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f018-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f018-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4f018-125">Schema name</span></span>  <br/> |<span data-ttu-id="4f018-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4f018-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="4f018-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4f018-127">Validation file</span></span>  <br/> |<span data-ttu-id="4f018-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4f018-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f018-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4f018-129">Can be empty</span></span>  <br/> |<span data-ttu-id="4f018-130">False</span><span class="sxs-lookup"><span data-stu-id="4f018-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f018-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="4f018-131">See also</span></span>



- [<span data-ttu-id="4f018-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4f018-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

