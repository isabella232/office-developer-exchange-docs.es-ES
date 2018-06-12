---
title: QueryString (cadena)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: El elemento de QueryString especifica un conjunto de valores que se devolverá que coinciden con la cadena de consulta en una solicitud de operación FindPeople. Una búsqueda con ninguna cadena de consulta especificada devuelve todos los elementos de la carpeta especificada.
ms.openlocfilehash: 9c5c733adcec1496e36986fd720b56b0a0274593
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836935"
---
# <a name="querystring-string"></a><span data-ttu-id="9a130-104">QueryString (cadena)</span><span class="sxs-lookup"><span data-stu-id="9a130-104">QueryString (String)</span></span>

<span data-ttu-id="9a130-105">El elemento de **QueryString** especifica un conjunto de valores que se devolverá que coinciden con la cadena de consulta en una solicitud de [operación FindPeople](findpeople-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9a130-105">The **QueryString** element specifies a set of values to be returned that match the query string in a [FindPeople operation](findpeople-operation.md) request.</span></span> <span data-ttu-id="9a130-106">Una búsqueda con ninguna **cadena de consulta** especificada devuelve todos los elementos de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="9a130-106">A search with no **QueryString** specified returns all items from the specified folder.</span></span> 
  
```XML
<QueryString/> 
```

 <span data-ttu-id="9a130-107">**string**</span><span class="sxs-lookup"><span data-stu-id="9a130-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9a130-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9a130-108">Attributes and elements</span></span>

<span data-ttu-id="9a130-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9a130-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a130-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="9a130-110">Attributes</span></span>

<span data-ttu-id="9a130-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9a130-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a130-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9a130-112">Child elements</span></span>

<span data-ttu-id="9a130-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9a130-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9a130-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9a130-114">Parent elements</span></span>

|<span data-ttu-id="9a130-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="9a130-115">**Element**</span></span>|<span data-ttu-id="9a130-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a130-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9a130-117">FindPeople</span><span class="sxs-lookup"><span data-stu-id="9a130-117">FindPeople</span></span>](findpeople.md) <br/> |<span data-ttu-id="9a130-118">Contiene los argumentos para una búsqueda de la [operación de FindPeople](findpeople-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9a130-118">Contains the arguments for a [FindPeople operation](findpeople-operation.md) search.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9a130-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9a130-119">Text value</span></span>

<span data-ttu-id="9a130-120">El valor de texto de la **cadena de consulta** representa una consulta de buzón de correo realizada mediante un subconjunto de la [Sintaxis de consulta avanzada (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9a130-120">The **QueryString** text value represents a mailbox query made by using a subset of [Advanced Query Syntax (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="9a130-121">Para obtener información sobre la sintaxis de este elemento, vea [QueryString (QueryStringType)](querystring-querystringtype.md).</span><span class="sxs-lookup"><span data-stu-id="9a130-121">For information about the syntax for this element, see [QueryString (QueryStringType)](querystring-querystringtype.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a130-122">Notas</span><span class="sxs-lookup"><span data-stu-id="9a130-122">Remarks</span></span>

<span data-ttu-id="9a130-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9a130-123">This element was introduced in Exchange Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a130-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9a130-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a130-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9a130-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9a130-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9a130-126">Schema name</span></span>  <br/> |<span data-ttu-id="9a130-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9a130-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9a130-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9a130-128">Validation file</span></span>  <br/> |<span data-ttu-id="9a130-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9a130-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9a130-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9a130-130">Can be empty</span></span>  <br/> |<span data-ttu-id="9a130-131">False</span><span class="sxs-lookup"><span data-stu-id="9a130-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a130-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="9a130-132">See also</span></span>



[<span data-ttu-id="9a130-133">Operación FindPeople</span><span class="sxs-lookup"><span data-stu-id="9a130-133">FindPeople operation</span></span>](findpeople-operation.md)


- [<span data-ttu-id="9a130-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9a130-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

