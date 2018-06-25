---
title: Identificadores de usuario
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserIds
api_type:
- schema
ms.assetid: 78a09c3a-1646-4c55-95a2-1109fb11e1c6
description: Elemento contiene una matriz de los identificadores de usuario delegan a los usuarios obtener o quitar de buzón de una entidad de seguridad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 277ae96fdbc30f1b39ef20553e10ff1de3ff7a8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840912"
---
# <a name="userids"></a><span data-ttu-id="7cabf-104">Identificadores de usuario</span><span class="sxs-lookup"><span data-stu-id="7cabf-104">UserIds</span></span>

<span data-ttu-id="7cabf-105">El elemento de **identificadores de usuario** contiene una matriz de delegado a los usuarios obtener o quitar de buzón de una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7cabf-105">The **UserIds** element contains an array of delegate users to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="7cabf-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7cabf-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 <span data-ttu-id="7cabf-107">**ArrayOfUserIdType**</span><span class="sxs-lookup"><span data-stu-id="7cabf-107">**ArrayOfUserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7cabf-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7cabf-108">Attributes and elements</span></span>

<span data-ttu-id="7cabf-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7cabf-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cabf-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="7cabf-110">Attributes</span></span>

<span data-ttu-id="7cabf-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7cabf-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7cabf-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7cabf-112">Child elements</span></span>

|<span data-ttu-id="7cabf-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7cabf-113">**Element**</span></span>|<span data-ttu-id="7cabf-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cabf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cabf-115">UserId</span><span class="sxs-lookup"><span data-stu-id="7cabf-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="7cabf-116">Identifica a obtener o quitar buzón de una entidad de seguridad de un delegado.</span><span class="sxs-lookup"><span data-stu-id="7cabf-116">Identifies a delegate to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="7cabf-117">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="7cabf-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7cabf-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7cabf-118">Parent elements</span></span>

|<span data-ttu-id="7cabf-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="7cabf-119">**Element**</span></span>|<span data-ttu-id="7cabf-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cabf-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cabf-121">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="7cabf-121">GetDelegate</span></span>](getdelegate.md) <br/> |<span data-ttu-id="7cabf-122">Define una solicitud para obtener información acerca de los delegados a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7cabf-122">Defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="7cabf-123">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="7cabf-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="7cabf-124">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="7cabf-124">RemoveDelegate</span></span>](removedelegate.md) <br/> |<span data-ttu-id="7cabf-125">Define una solicitud para quitar delegados de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7cabf-125">Defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="7cabf-126">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="7cabf-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cabf-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7cabf-127">Remarks</span></span>

<span data-ttu-id="7cabf-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7cabf-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7cabf-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7cabf-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cabf-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7cabf-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7cabf-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7cabf-131">Schema Name</span></span>  <br/> |<span data-ttu-id="7cabf-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7cabf-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7cabf-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7cabf-133">Validation File</span></span>  <br/> |<span data-ttu-id="7cabf-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7cabf-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7cabf-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7cabf-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="7cabf-136">False</span><span class="sxs-lookup"><span data-stu-id="7cabf-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7cabf-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cabf-137">See also</span></span>



[<span data-ttu-id="7cabf-138">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="7cabf-138">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="7cabf-139">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="7cabf-139">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="7cabf-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7cabf-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

