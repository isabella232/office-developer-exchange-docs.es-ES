---
title: GetItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: 769df8eb-9c72-48b5-a49f-82c6b86bc5fc
description: El elemento GetItem define una solicitud para obtener un elemento de un buzón en el almacén de Exchange.
ms.openlocfilehash: 39db141bad62c34bec5ae6a937ba94c2d1288090
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764896"
---
# <a name="getitem"></a><span data-ttu-id="7904e-103">GetItem</span><span class="sxs-lookup"><span data-stu-id="7904e-103">GetItem</span></span>

<span data-ttu-id="7904e-104">El elemento **GetItem** define una solicitud para obtener un elemento de un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7904e-104">The **GetItem** element defines a request to get an item from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetItem>
   <ItemShape/>
   <ItemIds/>
</GetItem>
```

 <span data-ttu-id="7904e-105">**GetItemType**</span><span class="sxs-lookup"><span data-stu-id="7904e-105">**GetItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7904e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7904e-106">Attributes and elements</span></span>

<span data-ttu-id="7904e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7904e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7904e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7904e-108">Attributes</span></span>

<span data-ttu-id="7904e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7904e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7904e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7904e-110">Child elements</span></span>

|<span data-ttu-id="7904e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7904e-111">**Element**</span></span>|<span data-ttu-id="7904e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7904e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7904e-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="7904e-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="7904e-114">Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="7904e-114">Identifies the item properties and content to include in a **GetItem** response.</span></span>  <br/> |
|[<span data-ttu-id="7904e-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="7904e-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="7904e-116">Contiene las identidades únicas de los elementos, elementos de aparición y elementos maestros periódicos que se usan para obtener los elementos desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7904e-116">Contains the unique identities of items, occurrence items, and recurring master items that are used to get items from the Exchange store.</span></span> <span data-ttu-id="7904e-117">Estos elementos representan los contactos, tareas, los mensajes, elementos de calendario, convocatorias de reunión y otros elementos válidos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7904e-117">These items represent contacts, tasks, messages, calendar items, meeting requests, and other valid items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7904e-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7904e-118">Parent elements</span></span>

<span data-ttu-id="7904e-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7904e-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7904e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7904e-120">Remarks</span></span>

<span data-ttu-id="7904e-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7904e-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7904e-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7904e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7904e-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7904e-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7904e-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7904e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="7904e-125">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="7904e-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="7904e-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7904e-126">Validation File</span></span>  <br/> |<span data-ttu-id="7904e-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7904e-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7904e-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7904e-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="7904e-129">False</span><span class="sxs-lookup"><span data-stu-id="7904e-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7904e-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="7904e-130">See also</span></span>



[<span data-ttu-id="7904e-131">Operación GetItem</span><span class="sxs-lookup"><span data-stu-id="7904e-131">GetItem operation</span></span>](getitem-operation.md)

