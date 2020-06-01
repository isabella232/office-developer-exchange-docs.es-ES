---
title: SetImListMigrationCompleted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4b806441-0429-44c4-90b7-1ae5c6ab9128
description: El elemento SetImListMigrationCompleted representa una solicitud para indicar si el almacén de Exchange contiene los elementos de mensajería instantánea usados por los clientes de mensajería instantánea.
ms.openlocfilehash: e5b16044ee72a9e931a2707d3f7823931f8a642a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464829"
---
# <a name="setimlistmigrationcompleted"></a><span data-ttu-id="87088-103">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="87088-103">SetImListMigrationCompleted</span></span>

<span data-ttu-id="87088-104">El elemento **SetImListMigrationCompleted** representa una solicitud para indicar si el almacén de Exchange contiene los elementos de mensajería instantánea usados por los clientes de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="87088-104">The **SetImListMigrationCompleted** element represents a request to indicate whether the Exchange store contains the instant messaging items used by instant messaging clients.</span></span> 
  
```XML
<SetImListMigrationCompleted>
   <ImListMigrationCompleted/>
</SetImListMigrationCompleted>
```

 <span data-ttu-id="87088-105">**SetImListMigrationCompletedType**</span><span class="sxs-lookup"><span data-stu-id="87088-105">**SetImListMigrationCompletedType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="87088-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="87088-106">Attributes and elements</span></span>

<span data-ttu-id="87088-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="87088-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87088-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="87088-108">Attributes</span></span>

<span data-ttu-id="87088-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="87088-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="87088-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="87088-110">Child elements</span></span>

[<span data-ttu-id="87088-111">ImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="87088-111">ImListMigrationCompleted</span></span>](imlistmigrationcompleted.md)
  
### <a name="parent-elements"></a><span data-ttu-id="87088-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="87088-112">Parent elements</span></span>

<span data-ttu-id="87088-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="87088-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87088-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87088-114">Remarks</span></span>

<span data-ttu-id="87088-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="87088-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="87088-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="87088-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87088-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="87088-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87088-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="87088-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="87088-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="87088-119">Schema name</span></span>  <br/> |<span data-ttu-id="87088-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="87088-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="87088-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="87088-121">Validation file</span></span>  <br/> |<span data-ttu-id="87088-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="87088-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="87088-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="87088-123">Can be empty</span></span>  <br/> |<span data-ttu-id="87088-124">false</span><span class="sxs-lookup"><span data-stu-id="87088-124">false</span></span>  <br/> |
   

