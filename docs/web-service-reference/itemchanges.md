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
description: El elemento ItemChanges contiene una matriz de elementos ItemChange que identifican los elementos y las actualizaciones que se aplican a los elementos.
ms.openlocfilehash: ea6fb2023b88360f9558057e80c7fe0d855173b5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459913"
---
# <a name="itemchanges"></a><span data-ttu-id="c902f-103">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="c902f-103">ItemChanges</span></span>

<span data-ttu-id="c902f-104">El elemento **ItemChanges** contiene una matriz de elementos [ItemChange](itemchange.md) que identifican los elementos y las actualizaciones que se aplican a los elementos.</span><span class="sxs-lookup"><span data-stu-id="c902f-104">The **ItemChanges** element contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span> 
  
[<span data-ttu-id="c902f-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="c902f-105">UpdateItem</span></span>](updateitem.md)
  
[<span data-ttu-id="c902f-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="c902f-106">ItemChanges</span></span>](itemchanges.md)
  
```xml
<ItemChanges>
   <ItemChange/>
</ItemChanges>
```

 <span data-ttu-id="c902f-107">**NonEmptyArrayOfItemChangesType**</span><span class="sxs-lookup"><span data-stu-id="c902f-107">**NonEmptyArrayOfItemChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c902f-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c902f-108">Attributes and elements</span></span>

<span data-ttu-id="c902f-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c902f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c902f-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c902f-110">Attributes</span></span>

<span data-ttu-id="c902f-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c902f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c902f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c902f-112">Child elements</span></span>

|<span data-ttu-id="c902f-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c902f-113">**Element**</span></span>|<span data-ttu-id="c902f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c902f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c902f-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="c902f-115">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="c902f-116">Contiene un identificador de elemento y las actualizaciones que se aplican al elemento.</span><span class="sxs-lookup"><span data-stu-id="c902f-116">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c902f-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c902f-117">Parent elements</span></span>

|<span data-ttu-id="c902f-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c902f-118">**Element**</span></span>|<span data-ttu-id="c902f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c902f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c902f-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="c902f-120">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="c902f-121">Define una solicitud para actualizar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c902f-121">Defines a request to update items in a mailbox.</span></span>  <br/> <span data-ttu-id="c902f-122">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="c902f-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c902f-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c902f-123">Remarks</span></span>

<span data-ttu-id="c902f-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c902f-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c902f-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c902f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c902f-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c902f-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c902f-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c902f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="c902f-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c902f-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c902f-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c902f-129">Validation File</span></span>  <br/> |<span data-ttu-id="c902f-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c902f-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c902f-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c902f-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="c902f-132">Falso</span><span class="sxs-lookup"><span data-stu-id="c902f-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c902f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c902f-133">See also</span></span>



[<span data-ttu-id="c902f-134">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="c902f-134">UpdateItem operation</span></span>](updateitem-operation.md)

