---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: El elemento MarkAsJunk especifica la solicitud para mover un elemento a la carpeta correo electrónico no deseado y para agregar el remitente a la lista de remitentes bloqueados.
ms.openlocfilehash: fbb3eee7ce350954888931ca55b27f596656b161
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836350"
---
# <a name="markasjunk"></a><span data-ttu-id="5f751-103">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="5f751-103">MarkAsJunk</span></span>

<span data-ttu-id="5f751-104">El elemento **MarkAsJunk** especifica la solicitud para mover un elemento a la carpeta correo electrónico no deseado y para agregar el remitente a la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="5f751-104">The **MarkAsJunk** element specifies the request to move an item to the junk mail folder and to add the sender to the blocked sender list.</span></span> 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 <span data-ttu-id="5f751-105">**MarkAsJunkType**</span><span class="sxs-lookup"><span data-stu-id="5f751-105">**MarkAsJunkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f751-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5f751-106">Attributes and elements</span></span>

<span data-ttu-id="5f751-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5f751-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f751-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f751-108">Attributes</span></span>

|<span data-ttu-id="5f751-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5f751-109">**Attribute**</span></span>|<span data-ttu-id="5f751-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f751-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f751-111">IsJunk</span><span class="sxs-lookup"><span data-stu-id="5f751-111">IsJunk</span></span>  <br/> |<span data-ttu-id="5f751-112">Un valor de texto de **true** para el atributo **IsJunk** indica que el remitente de correo electrónico se agrega a la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="5f751-112">A text value of **true** for the **IsJunk** attribute indicates that the email sender is added to the blocked sender list.</span></span> <span data-ttu-id="5f751-113">Un valor de **false** indica que el remitente de correo electrónico se elimina de la lista de remitentes bloqueados, si el remitente de correo electrónico ya está en la lista.</span><span class="sxs-lookup"><span data-stu-id="5f751-113">A value of **false** indicates that the email sender is removed from the blocked sender list, if the email sender is already on the list.</span></span>  <br/> |
|<span data-ttu-id="5f751-114">MoveItem</span><span class="sxs-lookup"><span data-stu-id="5f751-114">MoveItem</span></span>  <br/> |<span data-ttu-id="5f751-115">Un valor de texto de **true** para el atributo **MoveItem** indica que el elemento se mueve a la carpeta de correo electrónico no deseado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5f751-115">A text value of **true** for the **MoveItem** attribute indicates that the item is moved to the default junk mail folder.</span></span> <span data-ttu-id="5f751-116">Un valor de **false** indica que el elemento no se mueve a la carpeta de correo electrónico no deseado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5f751-116">A value of **false** indicates that the item is not moved to the default junk mail folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5f751-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f751-117">Child elements</span></span>

[<span data-ttu-id="5f751-118">ItemId</span><span class="sxs-lookup"><span data-stu-id="5f751-118">ItemIds</span></span>](itemids.md)
  
### <a name="parent-elements"></a><span data-ttu-id="5f751-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5f751-119">Parent elements</span></span>

<span data-ttu-id="5f751-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5f751-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f751-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f751-121">Remarks</span></span>

<span data-ttu-id="5f751-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5f751-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5f751-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f751-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f751-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5f751-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f751-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5f751-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5f751-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5f751-126">Schema name</span></span>  <br/> |<span data-ttu-id="5f751-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5f751-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5f751-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5f751-128">Validation file</span></span>  <br/> |<span data-ttu-id="5f751-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5f751-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5f751-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5f751-130">Can be empty</span></span>  <br/> ||
   

