---
title: ImListMigrationCompleted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6eed9502-5d9e-4345-ba23-3582ff487147
description: El elemento ImListMigrationCompleted indica si el almacén de Exchange contiene los elementos de mensajería instantáneos utilizados por los clientes de mensajería instantánea.
ms.openlocfilehash: 25f1b583b354a71958fbc8052c492726dc0eb7db
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835893"
---
# <a name="imlistmigrationcompleted"></a><span data-ttu-id="8a8f5-103">ImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="8a8f5-103">ImListMigrationCompleted</span></span>

<span data-ttu-id="8a8f5-104">El elemento **ImListMigrationCompleted** indica si el almacén de Exchange contiene los elementos utilizados por los clientes de mensajería instantánea de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-104">The **ImListMigrationCompleted** element indicates whether the Exchange store contains the instant messaging items used by instant messaging clients.</span></span> 
  
```XML
<ImListMigrationCompleted>true | false</ImListMigrationCompleted>
```

 <span data-ttu-id="8a8f5-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a8f5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a8f5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8a8f5-106">Attributes and elements</span></span>

<span data-ttu-id="8a8f5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a8f5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8a8f5-108">Attributes</span></span>

<span data-ttu-id="8a8f5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a8f5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8a8f5-110">Child elements</span></span>

<span data-ttu-id="8a8f5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8a8f5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8a8f5-112">Parent elements</span></span>

[<span data-ttu-id="8a8f5-113">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="8a8f5-113">SetImListMigrationCompleted</span></span>](setimlistmigrationcompleted.md)
  
## <a name="text-value"></a><span data-ttu-id="8a8f5-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8a8f5-114">Text value</span></span>

<span data-ttu-id="8a8f5-115">Un valor de texto de **true** para el elemento **ImListMigrationCompleted** indica que almacenan los contactos de mensajería instantánea almacén se ha migrado a Exchange.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-115">A text value of **true** for the **ImListMigrationCompleted** element indicates that the instant messaging contacts store has been migrated to the Exchange store.</span></span> <span data-ttu-id="8a8f5-116">Un valor de **false** indica que no se ha migrado el almacén de contactos de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-116">A value of **false** indicates that the instant message contacts store has not been migrated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8a8f5-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a8f5-117">Remarks</span></span>

<span data-ttu-id="8a8f5-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8a8f5-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a8f5-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8a8f5-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a8f5-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8a8f5-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8a8f5-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8a8f5-122">Schema name</span></span>  <br/> |<span data-ttu-id="8a8f5-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8a8f5-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8a8f5-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8a8f5-124">Validation file</span></span>  <br/> |<span data-ttu-id="8a8f5-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8a8f5-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a8f5-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8a8f5-126">Can be empty</span></span>  <br/> ||
   

