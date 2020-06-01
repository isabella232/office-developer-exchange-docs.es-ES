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
description: El elemento GetItem define una solicitud para obtener un elemento de un buzón de correo en el almacén de Exchange.
ms.openlocfilehash: a02403ee84195a41387d5dbe1785ae6d12b47da5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458701"
---
# <a name="getitem"></a><span data-ttu-id="44cec-103">GetItem</span><span class="sxs-lookup"><span data-stu-id="44cec-103">GetItem</span></span>

<span data-ttu-id="44cec-104">El elemento **GetItem** define una solicitud para obtener un elemento de un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44cec-104">The **GetItem** element defines a request to get an item from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetItem>
   <ItemShape/>
   <ItemIds/>
</GetItem>
```

 <span data-ttu-id="44cec-105">**GetItemType**</span><span class="sxs-lookup"><span data-stu-id="44cec-105">**GetItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44cec-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="44cec-106">Attributes and elements</span></span>

<span data-ttu-id="44cec-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="44cec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44cec-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="44cec-108">Attributes</span></span>

<span data-ttu-id="44cec-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="44cec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44cec-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44cec-110">Child elements</span></span>

|<span data-ttu-id="44cec-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="44cec-111">**Element**</span></span>|<span data-ttu-id="44cec-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44cec-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44cec-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="44cec-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="44cec-114">Identifica las propiedades de elemento y el contenido que se incluirá en una respuesta de **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="44cec-114">Identifies the item properties and content to include in a **GetItem** response.</span></span>  <br/> |
|[<span data-ttu-id="44cec-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="44cec-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="44cec-116">Contiene las identidades únicas de los elementos, los elementos de ocurrencia y los elementos maestros periódicos que se usan para obtener elementos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44cec-116">Contains the unique identities of items, occurrence items, and recurring master items that are used to get items from the Exchange store.</span></span> <span data-ttu-id="44cec-117">Estos elementos representan contactos, tareas, mensajes, elementos de calendario, convocatorias de reunión y otros elementos válidos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="44cec-117">These items represent contacts, tasks, messages, calendar items, meeting requests, and other valid items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44cec-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="44cec-118">Parent elements</span></span>

<span data-ttu-id="44cec-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44cec-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44cec-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44cec-120">Remarks</span></span>

<span data-ttu-id="44cec-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="44cec-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44cec-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="44cec-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44cec-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="44cec-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="44cec-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="44cec-124">Schema Name</span></span>  <br/> |<span data-ttu-id="44cec-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="44cec-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="44cec-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="44cec-126">Validation File</span></span>  <br/> |<span data-ttu-id="44cec-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="44cec-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="44cec-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="44cec-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="44cec-129">Falso</span><span class="sxs-lookup"><span data-stu-id="44cec-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44cec-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="44cec-130">See also</span></span>



[<span data-ttu-id="44cec-131">Operación GetItem</span><span class="sxs-lookup"><span data-stu-id="44cec-131">GetItem operation</span></span>](getitem-operation.md)

