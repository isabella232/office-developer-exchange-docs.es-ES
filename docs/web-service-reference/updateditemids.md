---
title: UpdatedItemIds
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9199aeb2-abdf-40c5-8743-40b61853c951
description: El elemento UpdatedItemIds especifica los identificadores de los elementos de aviso actualizados.
ms.openlocfilehash: 4a87bf50f90e80c0c887ee3a66b9f201ea1c8440
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465039"
---
# <a name="updateditemids"></a><span data-ttu-id="f1db3-103">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="f1db3-103">UpdatedItemIds</span></span>

<span data-ttu-id="f1db3-104">El elemento **UpdatedItemIds** especifica los identificadores de los elementos de aviso actualizados.</span><span class="sxs-lookup"><span data-stu-id="f1db3-104">The **UpdatedItemIds** element specifies the identifiers of updated reminder items.</span></span> 
  
```XML
<UpdatedItemIds>
   <ItemId></ItemId>
</UpdatedItemIds>

```

 <span data-ttu-id="f1db3-105">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="f1db3-105">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1db3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f1db3-106">Attributes and elements</span></span>

<span data-ttu-id="f1db3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f1db3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1db3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1db3-108">Attributes</span></span>

<span data-ttu-id="f1db3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f1db3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1db3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f1db3-110">Child elements</span></span>

[<span data-ttu-id="f1db3-111">ItemId</span><span class="sxs-lookup"><span data-stu-id="f1db3-111">ItemId</span></span>](itemid.md)
  
### <a name="parent-elements"></a><span data-ttu-id="f1db3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f1db3-112">Parent elements</span></span>

[<span data-ttu-id="f1db3-113">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="f1db3-113">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="f1db3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1db3-114">Remarks</span></span>

<span data-ttu-id="f1db3-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f1db3-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f1db3-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f1db3-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="f1db3-117">Si la operación [PerformReminderAction](performreminderaction-operation.md) no se completó correctamente o no se realizaron cambios en el servidor, el elemento **UpdatedItemIds** se devuelve como un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="f1db3-117">If the [PerformReminderAction](performreminderaction-operation.md) operation did not complete successfully, or no changes were made on the server, the **UpdatedItemIds** element is returned as an empty value.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f1db3-118">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f1db3-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1db3-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1db3-119">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f1db3-120">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f1db3-120">Schema Name</span></span>  <br/> |<span data-ttu-id="f1db3-121">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f1db3-121">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f1db3-122">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f1db3-122">Validation File</span></span>  <br/> |<span data-ttu-id="f1db3-123">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f1db3-123">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f1db3-124">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f1db3-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="f1db3-125">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f1db3-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1db3-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1db3-126">See also</span></span>



[<span data-ttu-id="f1db3-127">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="f1db3-127">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)


- [<span data-ttu-id="f1db3-128">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f1db3-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

