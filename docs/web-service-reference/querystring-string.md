---
title: QueryString (cadena)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: El elemento QueryString especifica un conjunto de valores que se devolverán que coinciden con la cadena de consulta en una solicitud de operación FindPeople. Una búsqueda sin cadena de consulta especificada devuelve todos los elementos de la carpeta especificada.
ms.openlocfilehash: ec025f86d3e6fb74810e9c539eba102d05adbb93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465327"
---
# <a name="querystring-string"></a><span data-ttu-id="ab97b-104">QueryString (cadena)</span><span class="sxs-lookup"><span data-stu-id="ab97b-104">QueryString (String)</span></span>

<span data-ttu-id="ab97b-105">El elemento **QueryString** especifica un conjunto de valores que se devolverán que coinciden con la cadena de consulta en una solicitud de [operación FindPeople](findpeople-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ab97b-105">The **QueryString** element specifies a set of values to be returned that match the query string in a [FindPeople operation](findpeople-operation.md) request.</span></span> <span data-ttu-id="ab97b-106">Una búsqueda sin **cadena** de consulta especificada devuelve todos los elementos de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="ab97b-106">A search with no **QueryString** specified returns all items from the specified folder.</span></span> 
  
```XML
<QueryString/> 
```

 <span data-ttu-id="ab97b-107">**string**</span><span class="sxs-lookup"><span data-stu-id="ab97b-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab97b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ab97b-108">Attributes and elements</span></span>

<span data-ttu-id="ab97b-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ab97b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab97b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ab97b-110">Attributes</span></span>

<span data-ttu-id="ab97b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ab97b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab97b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ab97b-112">Child elements</span></span>

<span data-ttu-id="ab97b-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ab97b-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ab97b-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ab97b-114">Parent elements</span></span>

|<span data-ttu-id="ab97b-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ab97b-115">**Element**</span></span>|<span data-ttu-id="ab97b-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab97b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab97b-117">FindPeople</span><span class="sxs-lookup"><span data-stu-id="ab97b-117">FindPeople</span></span>](findpeople.md) <br/> |<span data-ttu-id="ab97b-118">Contiene los argumentos para una búsqueda de [operación FindPeople](findpeople-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ab97b-118">Contains the arguments for a [FindPeople operation](findpeople-operation.md) search.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ab97b-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ab97b-119">Text value</span></span>

<span data-ttu-id="ab97b-120">El valor de texto **QueryString** representa una consulta de buzón realizada mediante un subconjunto de [Sintaxis de consulta avanzada (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ab97b-120">The **QueryString** text value represents a mailbox query made by using a subset of [Advanced Query Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="ab97b-121">Para obtener información acerca de la sintaxis de este elemento, consulte [QueryString (QueryStringType)](querystring-querystringtype.md).</span><span class="sxs-lookup"><span data-stu-id="ab97b-121">For information about the syntax for this element, see [QueryString (QueryStringType)](querystring-querystringtype.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab97b-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab97b-122">Remarks</span></span>

<span data-ttu-id="ab97b-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ab97b-123">This element was introduced in Exchange Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab97b-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ab97b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab97b-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab97b-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ab97b-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ab97b-126">Schema name</span></span>  <br/> |<span data-ttu-id="ab97b-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ab97b-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ab97b-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ab97b-128">Validation file</span></span>  <br/> |<span data-ttu-id="ab97b-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ab97b-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ab97b-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ab97b-130">Can be empty</span></span>  <br/> |<span data-ttu-id="ab97b-131">Falso</span><span class="sxs-lookup"><span data-stu-id="ab97b-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab97b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab97b-132">See also</span></span>



[<span data-ttu-id="ab97b-133">Operación FindPeople</span><span class="sxs-lookup"><span data-stu-id="ab97b-133">FindPeople operation</span></span>](findpeople-operation.md)


- [<span data-ttu-id="ab97b-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ab97b-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

