---
title: ExpandGroupMembership
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8989e96b-8fa1-4858-93b2-2cbdb30b9ca9
description: El elemento ExpandGroupMembership indica si se debe expandir la pertenencia del grupo devuelto desde una solicitud GetSearchableMailboxes.
ms.openlocfilehash: 8a94aa3da165ecc13282127e75c8d166f3972ead
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456909"
---
# <a name="expandgroupmembership"></a><span data-ttu-id="e3de5-103">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="e3de5-103">ExpandGroupMembership</span></span>

<span data-ttu-id="e3de5-104">El elemento **ExpandGroupMembership** indica si se debe expandir la pertenencia del grupo devuelto desde una solicitud **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="e3de5-104">The **ExpandGroupMembership** element indicates whether to expand the membership of the group returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<ExpandGroupMembership>true | false</ExpandGroupMembership>
```

 <span data-ttu-id="e3de5-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e3de5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3de5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e3de5-106">Attributes and elements</span></span>

<span data-ttu-id="e3de5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e3de5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3de5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e3de5-108">Attributes</span></span>

<span data-ttu-id="e3de5-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e3de5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3de5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e3de5-110">Child elements</span></span>

<span data-ttu-id="e3de5-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e3de5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3de5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e3de5-112">Parent elements</span></span>

<span data-ttu-id="e3de5-113">[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md)  |  [GetSearchableMailboxes](getsearchablemailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="e3de5-113">[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md) | [GetSearchableMailboxes](getsearchablemailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e3de5-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e3de5-114">Text value</span></span>

<span data-ttu-id="e3de5-115">Un valor de texto de **true** para el elemento **ExpandGroupElement** indica que la pertenencia a grupos está expandida.</span><span class="sxs-lookup"><span data-stu-id="e3de5-115">A text value of **true** for the **ExpandGroupElement** element indicates that group membership is expanded.</span></span> <span data-ttu-id="e3de5-116">Un valor de **false** indica que la pertenencia al grupo no se expande para mostrar los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="e3de5-116">A value of **false** indicates that the group membership is not expanded to show the members of the group.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e3de5-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3de5-117">Remarks</span></span>

<span data-ttu-id="e3de5-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e3de5-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e3de5-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3de5-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3de5-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e3de5-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3de5-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3de5-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e3de5-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e3de5-122">Schema name</span></span>  <br/> |<span data-ttu-id="e3de5-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e3de5-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e3de5-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e3de5-124">Validation file</span></span>  <br/> |<span data-ttu-id="e3de5-125">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e3de5-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e3de5-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e3de5-126">Can be empty</span></span>  <br/> |<span data-ttu-id="e3de5-127">false</span><span class="sxs-lookup"><span data-stu-id="e3de5-127">false</span></span>  <br/> |
   

