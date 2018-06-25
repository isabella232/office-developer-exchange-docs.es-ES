---
title: Ruta de acceso
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Path
api_type:
- schema
ms.assetid: 5829149e-7bfe-4820-bcc6-910e9264acc9
description: El elemento de ruta de acceso es el tipo de esquema de base para todos los identificadores de propiedad. Este tipo es abstracto y no se producirá nunca directamente dentro de los documentos de instancia.
ms.openlocfilehash: a5a1ca5179ccf339e5a1f15621c92e2870f4f2d9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836700"
---
# <a name="path"></a><span data-ttu-id="ebff4-104">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="ebff4-104">Path</span></span>

<span data-ttu-id="ebff4-105">El elemento de **ruta de acceso** es el tipo de esquema de base para todos los identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ebff4-105">The **Path** element is the base schema type for all property identifiers.</span></span> <span data-ttu-id="ebff4-106">Este tipo es abstracto y no se producirá nunca directamente dentro de los documentos de instancia.</span><span class="sxs-lookup"><span data-stu-id="ebff4-106">This type is abstract and will never occur directly within instance documents.</span></span> 
  
```xml
<Path/>
```

 <span data-ttu-id="ebff4-107">**BasePathToElementType**</span><span class="sxs-lookup"><span data-stu-id="ebff4-107">**BasePathToElementType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ebff4-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ebff4-108">Attributes and elements</span></span>

<span data-ttu-id="ebff4-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ebff4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ebff4-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ebff4-110">Attributes</span></span>

<span data-ttu-id="ebff4-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ebff4-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ebff4-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ebff4-112">Child elements</span></span>

<span data-ttu-id="ebff4-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ebff4-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ebff4-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ebff4-114">Parent elements</span></span>

<span data-ttu-id="ebff4-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ebff4-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ebff4-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ebff4-116">Remarks</span></span>

<span data-ttu-id="ebff4-117">Los siguientes elementos se usan para sustituir para el elemento de **ruta de acceso** :</span><span class="sxs-lookup"><span data-stu-id="ebff4-117">The following elements are used to substitute for the **Path** element:</span></span> 
  
- [<span data-ttu-id="ebff4-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="ebff4-118">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="ebff4-119">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ebff4-119">IndexedFieldURI</span></span>](indexedfielduri.md)
    
- [<span data-ttu-id="ebff4-120">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="ebff4-120">ExceptionFieldURI</span></span>](exceptionfielduri.md)
    
- [<span data-ttu-id="ebff4-121">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ebff4-121">ExtendedFieldURI</span></span>](extendedfielduri.md)
    
<span data-ttu-id="ebff4-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ebff4-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ebff4-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ebff4-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ebff4-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ebff4-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ebff4-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ebff4-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ebff4-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ebff4-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="ebff4-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ebff4-127">Validation File</span></span>  <br/> |<span data-ttu-id="ebff4-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ebff4-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ebff4-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ebff4-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="ebff4-130">False</span><span class="sxs-lookup"><span data-stu-id="ebff4-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebff4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebff4-131">See also</span></span>



- [<span data-ttu-id="ebff4-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ebff4-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

