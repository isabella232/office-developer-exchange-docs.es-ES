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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763846"
---
# <a name="content"></a><span data-ttu-id="69f47-103">Contenido</span><span class="sxs-lookup"><span data-stu-id="69f47-103">Content</span></span>

<span data-ttu-id="69f47-104">El elemento de **contenido** contiene el contenido con codificación Base64 de un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="69f47-104">The **Content** element contains the Base64-encoded contents of a file attachment.</span></span> 
  
```xml
<Content/>
```

 <span data-ttu-id="69f47-105">**Base64Binary**</span><span class="sxs-lookup"><span data-stu-id="69f47-105">**Base64Binary**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69f47-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="69f47-106">Attributes and elements</span></span>

<span data-ttu-id="69f47-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="69f47-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69f47-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="69f47-108">Attributes</span></span>

<span data-ttu-id="69f47-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="69f47-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69f47-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="69f47-110">Child elements</span></span>

<span data-ttu-id="69f47-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="69f47-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="69f47-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="69f47-112">Parent elements</span></span>

|<span data-ttu-id="69f47-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="69f47-113">**Element**</span></span>|<span data-ttu-id="69f47-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69f47-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69f47-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="69f47-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="69f47-116">Representa un archivo t es thattached a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="69f47-116">Represents a file t is thattached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="69f47-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="69f47-117">Text value</span></span>

<span data-ttu-id="69f47-118">El valor de cadena representa los datos binarios con codificación Base64 de los datos adjuntos de archivo.</span><span class="sxs-lookup"><span data-stu-id="69f47-118">The string value represents the Base64-encoded binary data of the file attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69f47-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69f47-119">Remarks</span></span>

<span data-ttu-id="69f47-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="69f47-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69f47-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="69f47-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69f47-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="69f47-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="69f47-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="69f47-123">Schema name</span></span>  <br/> |<span data-ttu-id="69f47-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="69f47-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="69f47-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="69f47-125">Validation file</span></span>  <br/> |<span data-ttu-id="69f47-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="69f47-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="69f47-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="69f47-127">Can be empty</span></span>  <br/> |<span data-ttu-id="69f47-128">False</span><span class="sxs-lookup"><span data-stu-id="69f47-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69f47-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="69f47-129">See also</span></span>



- [<span data-ttu-id="69f47-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="69f47-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

