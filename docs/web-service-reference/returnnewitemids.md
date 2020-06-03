---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: El elemento ReturnNewItemIds indica si los identificadores de elemento de los elementos nuevos se devuelven en la respuesta.
ms.openlocfilehash: 003676c4c034454aa551e42bf3af976183117b8c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465117"
---
# <a name="returnnewitemids"></a><span data-ttu-id="ac8ea-103">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="ac8ea-103">ReturnNewItemIds</span></span>

<span data-ttu-id="ac8ea-104">El elemento **ReturnNewItemIds** indica si los identificadores de elemento de los elementos nuevos se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac8ea-104">The **ReturnNewItemIds** element indicates whether the item identifiers of new items are returned in the response.</span></span> 
  
```XML
<ReturnNewItemIds/>
```

 <span data-ttu-id="ac8ea-105">**XS: Boolean**</span><span class="sxs-lookup"><span data-stu-id="ac8ea-105">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac8ea-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ac8ea-106">Attributes and elements</span></span>

<span data-ttu-id="ac8ea-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ac8ea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac8ea-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac8ea-108">Attributes</span></span>

<span data-ttu-id="ac8ea-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ac8ea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac8ea-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ac8ea-110">Child elements</span></span>

<span data-ttu-id="ac8ea-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ac8ea-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ac8ea-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ac8ea-112">Parent elements</span></span>

|<span data-ttu-id="ac8ea-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ac8ea-113">**Element**</span></span>|<span data-ttu-id="ac8ea-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac8ea-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac8ea-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="ac8ea-115">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="ac8ea-116">Define una solicitud para copiar un elemento en un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ac8ea-116">Defines a request to copy an item in a mailbox in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ac8ea-117">MoveItem</span><span class="sxs-lookup"><span data-stu-id="ac8ea-117">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="ac8ea-118">Define una solicitud para mover un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ac8ea-118">Defines a request to move an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ac8ea-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ac8ea-119">Text value</span></span>

<span data-ttu-id="ac8ea-120">Un valor de texto de **true** para el elemento **ReturnNewItemIds** indica que los nuevos identificadores de elemento se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac8ea-120">A text value of **true** for the **ReturnNewItemIds** element indicates that the new item identifiers are returned in the response.</span></span> <span data-ttu-id="ac8ea-121">Un valor de **false** indica que los nuevos identificadores de elemento no se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac8ea-121">A value of **false** indicates that the new item identifiers are not returned in the response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ac8ea-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac8ea-122">Remarks</span></span>

<span data-ttu-id="ac8ea-123">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ac8ea-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac8ea-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ac8ea-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac8ea-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac8ea-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ac8ea-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ac8ea-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ac8ea-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ac8ea-127">Message schema</span></span>  <br/> |
|<span data-ttu-id="ac8ea-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ac8ea-128">Validation File</span></span>  <br/> |<span data-ttu-id="ac8ea-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ac8ea-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ac8ea-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ac8ea-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac8ea-131">Falso</span><span class="sxs-lookup"><span data-stu-id="ac8ea-131">False</span></span>  <br/> |
   

