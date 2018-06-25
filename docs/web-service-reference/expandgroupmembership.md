---
title: ExpandGroupMembership
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8989e96b-8fa1-4858-93b2-2cbdb30b9ca9
description: El elemento ExpandGroupMembership indica si se debe expandir la pertenencia del grupo devuelto desde una solicitud de GetSearchableMailboxes.
ms.openlocfilehash: 11bfcf6893a147c726c94df77f7d9a9dfbaa773e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764491"
---
# <a name="expandgroupmembership"></a><span data-ttu-id="a20b8-103">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="a20b8-103">ExpandGroupMembership</span></span>

<span data-ttu-id="a20b8-104">El elemento **ExpandGroupMembership** indica si se debe expandir la pertenencia del grupo devuelto desde una solicitud de **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="a20b8-104">The **ExpandGroupMembership** element indicates whether to expand the membership of the group returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<ExpandGroupMembership>true | false</ExpandGroupMembership>
```

 <span data-ttu-id="a20b8-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a20b8-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a20b8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a20b8-106">Attributes and elements</span></span>

<span data-ttu-id="a20b8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a20b8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a20b8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a20b8-108">Attributes</span></span>

<span data-ttu-id="a20b8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a20b8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a20b8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a20b8-110">Child elements</span></span>

<span data-ttu-id="a20b8-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a20b8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a20b8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a20b8-112">Parent elements</span></span>

<span data-ttu-id="a20b8-113">[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md) | [GetSearchableMailboxes](getsearchablemailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="a20b8-113">[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md) | [GetSearchableMailboxes](getsearchablemailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a20b8-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a20b8-114">Text value</span></span>

<span data-ttu-id="a20b8-115">Un valor de texto de **true** para el elemento **ExpandGroupElement** indica que se expande la pertenencia a grupos.</span><span class="sxs-lookup"><span data-stu-id="a20b8-115">A text value of **true** for the **ExpandGroupElement** element indicates that group membership is expanded.</span></span> <span data-ttu-id="a20b8-116">Un valor de **false** indica que la pertenencia al grupo no se expande para mostrar a los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="a20b8-116">A value of **false** indicates that the group membership is not expanded to show the members of the group.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a20b8-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a20b8-117">Remarks</span></span>

<span data-ttu-id="a20b8-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a20b8-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a20b8-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a20b8-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a20b8-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a20b8-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a20b8-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a20b8-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a20b8-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a20b8-122">Schema name</span></span>  <br/> |<span data-ttu-id="a20b8-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a20b8-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a20b8-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a20b8-124">Validation file</span></span>  <br/> |<span data-ttu-id="a20b8-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a20b8-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a20b8-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a20b8-126">Can be empty</span></span>  <br/> |<span data-ttu-id="a20b8-127">falso</span><span class="sxs-lookup"><span data-stu-id="a20b8-127">false</span></span>  <br/> |
   

