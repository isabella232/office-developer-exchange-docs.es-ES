---
title: GetImItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 455e5709-6c06-49fd-bfb2-403fc912287c
description: El elemento de solicitud GetImItems define una solicitud para obtener información acerca de los grupos especificados de mensajería instantáneos y roles contactos de mensajería instantánea.
ms.openlocfilehash: ff7d520dde44fac6e9278633c1ad46b07b38d6c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764871"
---
# <a name="getimitems"></a><span data-ttu-id="e0f58-103">GetImItems</span><span class="sxs-lookup"><span data-stu-id="e0f58-103">GetImItems</span></span>

<span data-ttu-id="e0f58-104">El elemento de solicitud **GetImItems** define una solicitud para obtener información acerca de los grupos especificados de mensajería instantáneos y roles contactos de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="e0f58-104">The **GetImItems** request element defines a request to get information about the specified instant messaging groups and instant messaging contact personas.</span></span> 
  
```XML
<GetImItems>
   <ContactIds/>
   <GroupIds/>
   <ExtendedProperties/>
</GetImItems>
```

 <span data-ttu-id="e0f58-105">**GetImItemsType**</span><span class="sxs-lookup"><span data-stu-id="e0f58-105">**GetImItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0f58-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e0f58-106">Attributes and elements</span></span>

<span data-ttu-id="e0f58-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e0f58-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0f58-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0f58-108">Attributes</span></span>

<span data-ttu-id="e0f58-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0f58-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0f58-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0f58-110">Child elements</span></span>

<span data-ttu-id="e0f58-111">[ContactIds](contactids.md) | [GroupIds](groupids.md) | [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span><span class="sxs-lookup"><span data-stu-id="e0f58-111">[ContactIds](contactids.md) | [GroupIds](groupids.md) | [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e0f58-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e0f58-112">Parent elements</span></span>

<span data-ttu-id="e0f58-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0f58-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0f58-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0f58-114">Remarks</span></span>

<span data-ttu-id="e0f58-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0f58-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e0f58-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0f58-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0f58-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e0f58-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0f58-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e0f58-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0f58-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e0f58-119">Schema name</span></span>  <br/> |<span data-ttu-id="e0f58-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e0f58-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e0f58-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e0f58-121">Validation file</span></span>  <br/> |<span data-ttu-id="e0f58-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e0f58-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0f58-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e0f58-123">Can be empty</span></span>  <br/> ||
   

