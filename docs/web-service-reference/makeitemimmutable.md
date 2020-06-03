---
title: MakeItemImmutable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de1d2a60-aeeb-4625-8b11-23c42e1e7bae
description: El elemento MakeItemImmutable especifica un valor booleano que indica si un elemento se debe establecer como de solo lectura.
ms.openlocfilehash: 05c6e3343b8ba892048174ad98c9d31fe8da685b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465866"
---
# <a name="makeitemimmutable"></a><span data-ttu-id="1450d-103">MakeItemImmutable</span><span class="sxs-lookup"><span data-stu-id="1450d-103">MakeItemImmutable</span></span>

<span data-ttu-id="1450d-104">El elemento **MakeItemImmutable** especifica un valor booleano que indica si un elemento se debe establecer como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1450d-104">The **MakeItemImmutable** element specifies a Boolean value that indicates whether an item should be made read-only.</span></span> 
  
```XML
<MakeItemImmutable>true | false</MakeItemImmutable>
```

 <span data-ttu-id="1450d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1450d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1450d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1450d-106">Attributes and elements</span></span>

<span data-ttu-id="1450d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1450d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1450d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1450d-108">Attributes</span></span>

<span data-ttu-id="1450d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1450d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1450d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1450d-110">Child elements</span></span>

<span data-ttu-id="1450d-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1450d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1450d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1450d-112">Parent elements</span></span>

[<span data-ttu-id="1450d-113">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="1450d-113">UpdateItemInRecoverableItems</span></span>](updateiteminrecoverableitems.md)
  
## <a name="text-value"></a><span data-ttu-id="1450d-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1450d-114">Text value</span></span>

<span data-ttu-id="1450d-115">Un valor de texto de **true** para el elemento **MakeItemImmutable** indica que el elemento se debe establecer como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1450d-115">A text value of **true** for the **MakeItemImmutable** element indicates that the item should be made read-only.</span></span> <span data-ttu-id="1450d-116">Un valor de **false** indica que el elemento permite el acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1450d-116">A value of **false** indicates that the item allows read-write access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1450d-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1450d-117">Remarks</span></span>

<span data-ttu-id="1450d-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1450d-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1450d-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1450d-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1450d-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1450d-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1450d-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="1450d-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1450d-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1450d-122">Schema name</span></span>  <br/> |<span data-ttu-id="1450d-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1450d-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1450d-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1450d-124">Validation file</span></span>  <br/> |<span data-ttu-id="1450d-125">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1450d-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1450d-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1450d-126">Can be empty</span></span>  <br/> ||
   

