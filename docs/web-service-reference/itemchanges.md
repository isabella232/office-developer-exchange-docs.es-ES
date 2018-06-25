---
title: ItemChanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemChanges
api_type:
- schema
ms.assetid: cd307892-2f69-4494-8325-219bdb5c3ad5
description: El elemento ItemChanges contiene una matriz de elementos de ItemChange que identifican los elementos y las actualizaciones que se debe aplicar a los elementos.
ms.openlocfilehash: 38fe112441a8773a2d6b494ed57c63341cab2b58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836141"
---
# <a name="itemchanges"></a><span data-ttu-id="652f1-103">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="652f1-103">ItemChanges</span></span>

<span data-ttu-id="652f1-104">El elemento **ItemChanges** contiene una matriz de elementos de [ItemChange](itemchange.md) que identifican los elementos y las actualizaciones que se debe aplicar a los elementos.</span><span class="sxs-lookup"><span data-stu-id="652f1-104">The **ItemChanges** element contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span> 
  
[<span data-ttu-id="652f1-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="652f1-105">UpdateItem</span></span>](updateitem.md)
  
[<span data-ttu-id="652f1-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="652f1-106">ItemChanges</span></span>](itemchanges.md)
  
```xml
<ItemChanges>
   <ItemChange/>
</ItemChanges>
```

 <span data-ttu-id="652f1-107">**NonEmptyArrayOfItemChangesType**</span><span class="sxs-lookup"><span data-stu-id="652f1-107">**NonEmptyArrayOfItemChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="652f1-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="652f1-108">Attributes and elements</span></span>

<span data-ttu-id="652f1-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="652f1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="652f1-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="652f1-110">Attributes</span></span>

<span data-ttu-id="652f1-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="652f1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="652f1-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="652f1-112">Child elements</span></span>

|<span data-ttu-id="652f1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="652f1-113">**Element**</span></span>|<span data-ttu-id="652f1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="652f1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="652f1-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="652f1-115">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="652f1-116">Contiene un identificador de elemento y las actualizaciones que se debe aplicar al elemento.</span><span class="sxs-lookup"><span data-stu-id="652f1-116">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="652f1-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="652f1-117">Parent elements</span></span>

|<span data-ttu-id="652f1-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="652f1-118">**Element**</span></span>|<span data-ttu-id="652f1-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="652f1-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="652f1-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="652f1-120">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="652f1-121">Define una solicitud para actualizar elementos de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="652f1-121">Defines a request to update items in a mailbox.</span></span>  <br/> <span data-ttu-id="652f1-122">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="652f1-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="652f1-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="652f1-123">Remarks</span></span>

<span data-ttu-id="652f1-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="652f1-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="652f1-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="652f1-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="652f1-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="652f1-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="652f1-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="652f1-127">Schema Name</span></span>  <br/> |<span data-ttu-id="652f1-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="652f1-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="652f1-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="652f1-129">Validation File</span></span>  <br/> |<span data-ttu-id="652f1-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="652f1-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="652f1-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="652f1-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="652f1-132">False</span><span class="sxs-lookup"><span data-stu-id="652f1-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="652f1-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="652f1-133">See also</span></span>



[<span data-ttu-id="652f1-134">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="652f1-134">UpdateItem operation</span></span>](updateitem-operation.md)

