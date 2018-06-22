---
title: GetSearchableMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 949871f7-0d10-498e-84aa-f0652f1193be
description: El elemento GetSearchableMailboxes contiene una solicitud para obtener una lista de buzones de correo que el cliente tiene permiso para realizar una búsqueda de exhibición de documentos electrónicos.
ms.openlocfilehash: 8cce18bb62d3840cb9883d20a380cc4f2193303e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764964"
---
# <a name="getsearchablemailboxes"></a><span data-ttu-id="eba60-103">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="eba60-103">GetSearchableMailboxes</span></span>

<span data-ttu-id="eba60-104">El elemento **GetSearchableMailboxes** contiene una solicitud para obtener una lista de buzones de correo que el cliente tiene permiso para realizar una búsqueda de exhibición de documentos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="eba60-104">The **GetSearchableMailboxes** element contains a request to get a list of mailboxes that the client has permission to perform an eDiscovery search.</span></span> 
  
```XML
<GetSearchableMailboxes>
   <SearchFilter/>
   <ExpandGroupMembership/>
</GetSearchableMailboxes>
```

 <span data-ttu-id="eba60-105">**GetSearchableMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="eba60-105">**GetSearchableMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eba60-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eba60-106">Attributes and elements</span></span>

<span data-ttu-id="eba60-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eba60-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eba60-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eba60-108">Attributes</span></span>

<span data-ttu-id="eba60-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eba60-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eba60-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eba60-110">Child elements</span></span>

<span data-ttu-id="eba60-111">[SearchFilter](searchfilter.md) | [ExpandGroupMembership](expandgroupmembership.md)</span><span class="sxs-lookup"><span data-stu-id="eba60-111">[SearchFilter](searchfilter.md) | [ExpandGroupMembership](expandgroupmembership.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eba60-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eba60-112">Parent elements</span></span>

<span data-ttu-id="eba60-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eba60-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eba60-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eba60-114">Remarks</span></span>

<span data-ttu-id="eba60-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eba60-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="eba60-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="eba60-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eba60-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eba60-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eba60-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eba60-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eba60-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eba60-119">Schema name</span></span>  <br/> |<span data-ttu-id="eba60-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="eba60-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eba60-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eba60-121">Validation file</span></span>  <br/> |<span data-ttu-id="eba60-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eba60-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eba60-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eba60-123">Can be empty</span></span>  <br/> ||
   

