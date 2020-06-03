---
title: IsPermanentFailure
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18dc3a97-cc0a-4092-934e-a6e86f52e668
description: El elemento IsPermanentFailure indica si un intento anterior de indizar el elemento no se ha realizado correctamente.
ms.openlocfilehash: 48a13eebfa16c538c1b10d92f080d51f1b318d12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460396"
---
# <a name="ispermanentfailure"></a><span data-ttu-id="86cf7-103">IsPermanentFailure</span><span class="sxs-lookup"><span data-stu-id="86cf7-103">IsPermanentFailure</span></span>

<span data-ttu-id="86cf7-104">El elemento **IsPermanentFailure** indica si un intento anterior de indizar el elemento no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="86cf7-104">The **IsPermanentFailure** element indicates whether a previous attempt to index the item was unsuccessful.</span></span> 
  
```XML
<IsPermanentFailure>true | false</IsPermanentFailure>
```

 <span data-ttu-id="86cf7-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="86cf7-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86cf7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="86cf7-106">Attributes and elements</span></span>

<span data-ttu-id="86cf7-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="86cf7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86cf7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="86cf7-108">Attributes</span></span>

<span data-ttu-id="86cf7-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="86cf7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86cf7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="86cf7-110">Child elements</span></span>

<span data-ttu-id="86cf7-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="86cf7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="86cf7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="86cf7-112">Parent elements</span></span>

[<span data-ttu-id="86cf7-113">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="86cf7-113">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md)
  
## <a name="text-value"></a><span data-ttu-id="86cf7-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="86cf7-114">Text value</span></span>

<span data-ttu-id="86cf7-115">Un valor de texto de **true** para el elemento **IsPermanentFailure** indica que no se pudo realizar correctamente un intento anterior de indizar el elemento de buzón.</span><span class="sxs-lookup"><span data-stu-id="86cf7-115">A text value of **true** for the **IsPermanentFailure** element indicates that a previous attempt to index the mailbox item was unsuccessful.</span></span> <span data-ttu-id="86cf7-116">Un valor de **false** indica que un intento anterior para indizar el elemento de buzón se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="86cf7-116">A value of **false** indicates that a previous attempt to index the mailbox item was successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="86cf7-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86cf7-117">Remarks</span></span>

<span data-ttu-id="86cf7-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="86cf7-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="86cf7-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="86cf7-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86cf7-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="86cf7-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86cf7-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="86cf7-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="86cf7-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="86cf7-122">Schema name</span></span>  <br/> |<span data-ttu-id="86cf7-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="86cf7-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="86cf7-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="86cf7-124">Validation file</span></span>  <br/> |<span data-ttu-id="86cf7-125">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="86cf7-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="86cf7-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="86cf7-126">Can be empty</span></span>  <br/> |<span data-ttu-id="86cf7-127">false</span><span class="sxs-lookup"><span data-stu-id="86cf7-127">false</span></span>  <br/> |
   

