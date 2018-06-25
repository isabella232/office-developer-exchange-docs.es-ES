---
title: Archivar como
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAs
api_type:
- schema
ms.assetid: df50524e-471c-49d2-89fe-b2d0f61a1365
description: El elemento FileAs representa cómo se presenta una lista de contactos o de distribución en la carpeta Contactos.
ms.openlocfilehash: dab9142eebf7691862e7970a7d1e8f5874393b94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764597"
---
# <a name="fileas"></a><span data-ttu-id="b8859-103">Archivar como</span><span class="sxs-lookup"><span data-stu-id="b8859-103">FileAs</span></span>

<span data-ttu-id="b8859-104">El elemento **FileAs** representa cómo se presenta una lista de contactos o de distribución en la carpeta Contactos.</span><span class="sxs-lookup"><span data-stu-id="b8859-104">The **FileAs** element represents how a contact or distribution list is filed in the Contacts folder.</span></span> 
  
```xml
<FileAs/>
```

 <span data-ttu-id="b8859-105">**string**</span><span class="sxs-lookup"><span data-stu-id="b8859-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8859-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b8859-106">Attributes and elements</span></span>

<span data-ttu-id="b8859-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b8859-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8859-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8859-108">Attributes</span></span>

<span data-ttu-id="b8859-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8859-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8859-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8859-110">Child elements</span></span>

<span data-ttu-id="b8859-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8859-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b8859-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b8859-112">Parent elements</span></span>

|<span data-ttu-id="b8859-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8859-113">**Element**</span></span>|<span data-ttu-id="b8859-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8859-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8859-115">DistributionList</span><span class="sxs-lookup"><span data-stu-id="b8859-115">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="b8859-116">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="b8859-116">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="b8859-117">Contact</span><span class="sxs-lookup"><span data-stu-id="b8859-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="b8859-118">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8859-118">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b8859-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b8859-119">Text value</span></span>

<span data-ttu-id="b8859-120">Si se usa este elemento, es necesario un valor de texto que representa una cadena.</span><span class="sxs-lookup"><span data-stu-id="b8859-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8859-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8859-121">Remarks</span></span>

<span data-ttu-id="b8859-122">El elemento **FileAs** se usa para ordenar los contactos y las listas de distribución por un nombre que no sea un nombre completo o el nombre de la compañía.</span><span class="sxs-lookup"><span data-stu-id="b8859-122">The **FileAs** element is used to sort contacts and distribution lists by a name other than a full name or company name.</span></span> 
  
<span data-ttu-id="b8859-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b8859-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8859-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b8859-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8859-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8859-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b8859-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b8859-126">Schema name</span></span>  <br/> |<span data-ttu-id="b8859-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b8859-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="b8859-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b8859-128">Validation file</span></span>  <br/> |<span data-ttu-id="b8859-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b8859-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b8859-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b8859-130">Can be empty</span></span>  <br/> |<span data-ttu-id="b8859-131">False</span><span class="sxs-lookup"><span data-stu-id="b8859-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8859-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8859-132">See also</span></span>



- [<span data-ttu-id="b8859-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b8859-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

