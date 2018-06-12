---
title: Contenido
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Content
api_type:
- schema
ms.assetid: 24f8c54a-505f-4fc0-b7e7-93ad50b97070
description: El elemento de contenido contiene el contenido con codificación Base64 de un archivo adjunto.
ms.openlocfilehash: 20afe6286d3efaa5da6cdc88e397e88fddb1d8c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763846"
---
# <a name="content"></a><span data-ttu-id="d2a90-103">Contenido</span><span class="sxs-lookup"><span data-stu-id="d2a90-103">Content</span></span>

<span data-ttu-id="d2a90-104">El elemento de **contenido** contiene el contenido con codificación Base64 de un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="d2a90-104">The **Content** element contains the Base64-encoded contents of a file attachment.</span></span> 
  
```xml
<Content/>
```

 <span data-ttu-id="d2a90-105">**Base64Binary**</span><span class="sxs-lookup"><span data-stu-id="d2a90-105">**Base64Binary**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d2a90-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d2a90-106">Attributes and elements</span></span>

<span data-ttu-id="d2a90-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d2a90-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2a90-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d2a90-108">Attributes</span></span>

<span data-ttu-id="d2a90-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d2a90-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2a90-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d2a90-110">Child elements</span></span>

<span data-ttu-id="d2a90-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d2a90-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d2a90-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d2a90-112">Parent elements</span></span>

|<span data-ttu-id="d2a90-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2a90-113">**Element**</span></span>|<span data-ttu-id="d2a90-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d2a90-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2a90-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="d2a90-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="d2a90-116">Representa un archivo t es thattached a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d2a90-116">Represents a file t is thattached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d2a90-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d2a90-117">Text value</span></span>

<span data-ttu-id="d2a90-118">El valor de cadena representa los datos binarios con codificación Base64 de los datos adjuntos de archivo.</span><span class="sxs-lookup"><span data-stu-id="d2a90-118">The string value represents the Base64-encoded binary data of the file attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2a90-119">Notas</span><span class="sxs-lookup"><span data-stu-id="d2a90-119">Remarks</span></span>

<span data-ttu-id="d2a90-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d2a90-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2a90-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d2a90-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2a90-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2a90-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d2a90-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d2a90-123">Schema name</span></span>  <br/> |<span data-ttu-id="d2a90-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d2a90-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="d2a90-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d2a90-125">Validation file</span></span>  <br/> |<span data-ttu-id="d2a90-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d2a90-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d2a90-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d2a90-127">Can be empty</span></span>  <br/> |<span data-ttu-id="d2a90-128">False</span><span class="sxs-lookup"><span data-stu-id="d2a90-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2a90-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="d2a90-129">See also</span></span>



- [<span data-ttu-id="d2a90-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d2a90-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

