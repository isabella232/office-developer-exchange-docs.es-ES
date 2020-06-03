---
title: Ruta
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
description: El elemento path es el tipo de esquema base para todos los identificadores de propiedad. Este tipo es abstracto y nunca se producirá directamente en documentos de instancia.
ms.openlocfilehash: 5ba18084243e9720a76b9ac28023778c6d546bc4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529017"
---
# <a name="path"></a><span data-ttu-id="f3e8b-104">Ruta</span><span class="sxs-lookup"><span data-stu-id="f3e8b-104">Path</span></span>

<span data-ttu-id="f3e8b-105">El elemento **path** es el tipo de esquema base para todos los identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f3e8b-105">The **Path** element is the base schema type for all property identifiers.</span></span> <span data-ttu-id="f3e8b-106">Este tipo es abstracto y nunca se producirá directamente en documentos de instancia.</span><span class="sxs-lookup"><span data-stu-id="f3e8b-106">This type is abstract and will never occur directly within instance documents.</span></span> 
  
```xml
<Path/>
```

 <span data-ttu-id="f3e8b-107">**BasePathToElementType**</span><span class="sxs-lookup"><span data-stu-id="f3e8b-107">**BasePathToElementType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f3e8b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f3e8b-108">Attributes and elements</span></span>

<span data-ttu-id="f3e8b-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f3e8b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3e8b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3e8b-110">Attributes</span></span>

<span data-ttu-id="f3e8b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f3e8b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3e8b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f3e8b-112">Child elements</span></span>

<span data-ttu-id="f3e8b-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f3e8b-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f3e8b-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f3e8b-114">Parent elements</span></span>

<span data-ttu-id="f3e8b-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f3e8b-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f3e8b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3e8b-116">Remarks</span></span>

<span data-ttu-id="f3e8b-117">Los siguientes elementos se usan para sustituir al elemento **path** :</span><span class="sxs-lookup"><span data-stu-id="f3e8b-117">The following elements are used to substitute for the **Path** element:</span></span> 
  
- [<span data-ttu-id="f3e8b-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="f3e8b-118">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="f3e8b-119">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f3e8b-119">IndexedFieldURI</span></span>](indexedfielduri.md)
    
- [<span data-ttu-id="f3e8b-120">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="f3e8b-120">ExceptionFieldURI</span></span>](exceptionfielduri.md)
    
- [<span data-ttu-id="f3e8b-121">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f3e8b-121">ExtendedFieldURI</span></span>](extendedfielduri.md)
    
<span data-ttu-id="f3e8b-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f3e8b-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3e8b-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f3e8b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3e8b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3e8b-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f3e8b-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f3e8b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f3e8b-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f3e8b-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="f3e8b-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f3e8b-127">Validation File</span></span>  <br/> |<span data-ttu-id="f3e8b-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f3e8b-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f3e8b-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f3e8b-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="f3e8b-130">Falso</span><span class="sxs-lookup"><span data-stu-id="f3e8b-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3e8b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3e8b-131">See also</span></span>



- [<span data-ttu-id="f3e8b-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f3e8b-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

