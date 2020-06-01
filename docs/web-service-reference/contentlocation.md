---
title: ContentLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentLocation
api_type:
- schema
ms.assetid: d91cf587-24e3-4c13-8784-5ca29787cca7
description: El elemento ContentLocation contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.
ms.openlocfilehash: 01bb95da5f620fddc8777f88b1d3eb1a7e6069b1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461488"
---
# <a name="contentlocation"></a><span data-ttu-id="e604c-103">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="e604c-103">ContentLocation</span></span>

<span data-ttu-id="e604c-104">El elemento **ContentLocation** contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e604c-104">The **ContentLocation** element contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of an attachment.</span></span> 
  
```xml
<ContentLocation/>
```

 <span data-ttu-id="e604c-105">**String**</span><span class="sxs-lookup"><span data-stu-id="e604c-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e604c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e604c-106">Attributes and elements</span></span>

<span data-ttu-id="e604c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e604c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e604c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e604c-108">Attributes</span></span>

<span data-ttu-id="e604c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e604c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e604c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e604c-110">Child elements</span></span>

<span data-ttu-id="e604c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e604c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e604c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e604c-112">Parent elements</span></span>

|<span data-ttu-id="e604c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e604c-113">**Element**</span></span>|<span data-ttu-id="e604c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e604c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e604c-115">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="e604c-115">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="e604c-116">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e604c-116">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="e604c-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="e604c-117">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="e604c-118">Representa un archivo que está adjunto a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e604c-118">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e604c-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e604c-119">Text value</span></span>

<span data-ttu-id="e604c-120">El valor de texto es un valor de cadena que representa un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="e604c-120">The text value is a string value that represents a URI.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e604c-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e604c-121">Remarks</span></span>

<span data-ttu-id="e604c-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e604c-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e604c-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e604c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e604c-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="e604c-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e604c-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e604c-125">Schema name</span></span>  <br/> |<span data-ttu-id="e604c-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e604c-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="e604c-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e604c-127">Validation file</span></span>  <br/> |<span data-ttu-id="e604c-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e604c-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e604c-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e604c-129">Can be empty</span></span>  <br/> |<span data-ttu-id="e604c-130">Falso</span><span class="sxs-lookup"><span data-stu-id="e604c-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e604c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e604c-131">See also</span></span>



- [<span data-ttu-id="e604c-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e604c-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

