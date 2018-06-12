---
title: UpdatedItemIds
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9199aeb2-abdf-40c5-8743-40b61853c951
description: El elemento UpdatedItemIds especifica los identificadores de elementos de aviso actualizado.
ms.openlocfilehash: b95ebb20823706e68b1fd66dc64f756808bb7375
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840811"
---
# <a name="updateditemids"></a><span data-ttu-id="d5715-103">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="d5715-103">UpdatedItemIds</span></span>

<span data-ttu-id="d5715-104">El elemento **UpdatedItemIds** especifica los identificadores de elementos de aviso actualizado.</span><span class="sxs-lookup"><span data-stu-id="d5715-104">The **UpdatedItemIds** element specifies the identifiers of updated reminder items.</span></span> 
  
```XML
<UpdatedItemIds>
   <ItemId></ItemId>
</UpdatedItemIds>

```

 <span data-ttu-id="d5715-105">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="d5715-105">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5715-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d5715-106">Attributes and elements</span></span>

<span data-ttu-id="d5715-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d5715-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5715-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5715-108">Attributes</span></span>

<span data-ttu-id="d5715-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d5715-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5715-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d5715-110">Child elements</span></span>

[<span data-ttu-id="d5715-111">ItemId</span><span class="sxs-lookup"><span data-stu-id="d5715-111">ItemId</span></span>](itemid.md)
  
### <a name="parent-elements"></a><span data-ttu-id="d5715-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d5715-112">Parent elements</span></span>

[<span data-ttu-id="d5715-113">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="d5715-113">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="d5715-114">Notas</span><span class="sxs-lookup"><span data-stu-id="d5715-114">Remarks</span></span>

<span data-ttu-id="d5715-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d5715-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d5715-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5715-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="d5715-117">Si la operación [PerformReminderAction](performreminderaction-operation.md) no se completó correctamente o no se realizaron cambios en el servidor, se devuelve el elemento **UpdatedItemIds** como un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="d5715-117">If the [PerformReminderAction](performreminderaction-operation.md) operation did not complete successfully, or no changes were made on the server, the **UpdatedItemIds** element is returned as an empty value.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d5715-118">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d5715-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5715-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5715-119">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d5715-120">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d5715-120">Schema Name</span></span>  <br/> |<span data-ttu-id="d5715-121">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d5715-121">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d5715-122">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d5715-122">Validation File</span></span>  <br/> |<span data-ttu-id="d5715-123">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d5715-123">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d5715-124">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d5715-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5715-125">Verdadero</span><span class="sxs-lookup"><span data-stu-id="d5715-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5715-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="d5715-126">See also</span></span>



[<span data-ttu-id="d5715-127">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="d5715-127">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)


- [<span data-ttu-id="d5715-128">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d5715-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

