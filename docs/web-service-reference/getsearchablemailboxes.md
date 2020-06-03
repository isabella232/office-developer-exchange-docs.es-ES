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
ms.openlocfilehash: a327f8766e53e9f1fae6928179d5a4b8e3d044a8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530193"
---
# <a name="getsearchablemailboxes"></a><span data-ttu-id="14952-103">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="14952-103">GetSearchableMailboxes</span></span>

<span data-ttu-id="14952-104">El elemento **GetSearchableMailboxes** contiene una solicitud para obtener una lista de buzones de correo que el cliente tiene permiso para realizar una búsqueda de exhibición de documentos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="14952-104">The **GetSearchableMailboxes** element contains a request to get a list of mailboxes that the client has permission to perform an eDiscovery search.</span></span> 
  
```XML
<GetSearchableMailboxes>
   <SearchFilter/>
   <ExpandGroupMembership/>
</GetSearchableMailboxes>
```

 <span data-ttu-id="14952-105">**GetSearchableMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="14952-105">**GetSearchableMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="14952-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="14952-106">Attributes and elements</span></span>

<span data-ttu-id="14952-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="14952-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14952-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="14952-108">Attributes</span></span>

<span data-ttu-id="14952-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="14952-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="14952-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="14952-110">Child elements</span></span>

<span data-ttu-id="14952-111">[SearchFilter](searchfilter.md)  |  [ExpandGroupMembership](expandgroupmembership.md)</span><span class="sxs-lookup"><span data-stu-id="14952-111">[SearchFilter](searchfilter.md) | [ExpandGroupMembership](expandgroupmembership.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="14952-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="14952-112">Parent elements</span></span>

<span data-ttu-id="14952-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="14952-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="14952-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14952-114">Remarks</span></span>

<span data-ttu-id="14952-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="14952-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="14952-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="14952-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14952-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="14952-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14952-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="14952-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="14952-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="14952-119">Schema name</span></span>  <br/> |<span data-ttu-id="14952-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="14952-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="14952-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="14952-121">Validation file</span></span>  <br/> |<span data-ttu-id="14952-122">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="14952-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="14952-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="14952-123">Can be empty</span></span>  <br/> ||
   

