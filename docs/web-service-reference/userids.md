---
title: UserIds
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
description: El elemento UserIds contiene una matriz de usuarios delegados para obtener o quitar del buzón de la entidad de la identidad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: de4661226c154ef0d2d5ac55c57405e20c4d2aee
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459780"
---
# <a name="userids"></a><span data-ttu-id="76496-104">UserIds</span><span class="sxs-lookup"><span data-stu-id="76496-104">UserIds</span></span>

<span data-ttu-id="76496-105">El elemento **userids** contiene una matriz de usuarios delegados para obtener o quitar del buzón de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="76496-105">The **UserIds** element contains an array of delegate users to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="76496-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="76496-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 <span data-ttu-id="76496-107">**ArrayOfUserIdType**</span><span class="sxs-lookup"><span data-stu-id="76496-107">**ArrayOfUserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76496-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="76496-108">Attributes and elements</span></span>

<span data-ttu-id="76496-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="76496-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76496-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="76496-110">Attributes</span></span>

<span data-ttu-id="76496-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="76496-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76496-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="76496-112">Child elements</span></span>

|<span data-ttu-id="76496-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="76496-113">**Element**</span></span>|<span data-ttu-id="76496-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76496-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76496-115">UserId</span><span class="sxs-lookup"><span data-stu-id="76496-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="76496-116">Identifica un delegado para obtener o quitar del buzón de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="76496-116">Identifies a delegate to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="76496-117">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="76496-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="76496-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="76496-118">Parent elements</span></span>

|<span data-ttu-id="76496-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="76496-119">**Element**</span></span>|<span data-ttu-id="76496-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76496-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76496-121">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="76496-121">GetDelegate</span></span>](getdelegate.md) <br/> |<span data-ttu-id="76496-122">Define una solicitud para obtener información acerca de los delegados de un buzón.</span><span class="sxs-lookup"><span data-stu-id="76496-122">Defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="76496-123">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="76496-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="76496-124">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="76496-124">RemoveDelegate</span></span>](removedelegate.md) <br/> |<span data-ttu-id="76496-125">Define una solicitud para quitar delegados de un buzón.</span><span class="sxs-lookup"><span data-stu-id="76496-125">Defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="76496-126">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="76496-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76496-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76496-127">Remarks</span></span>

<span data-ttu-id="76496-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="76496-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76496-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="76496-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76496-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="76496-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="76496-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="76496-131">Schema Name</span></span>  <br/> |<span data-ttu-id="76496-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="76496-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="76496-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="76496-133">Validation File</span></span>  <br/> |<span data-ttu-id="76496-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="76496-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="76496-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="76496-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="76496-136">Falso</span><span class="sxs-lookup"><span data-stu-id="76496-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76496-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="76496-137">See also</span></span>



[<span data-ttu-id="76496-138">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="76496-138">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="76496-139">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="76496-139">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="76496-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="76496-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

