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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459780"
---
# <a name="userids"></a><span data-ttu-id="c405c-104">UserIds</span><span class="sxs-lookup"><span data-stu-id="c405c-104">UserIds</span></span>

<span data-ttu-id="c405c-105">El elemento **userids** contiene una matriz de usuarios delegados para obtener o quitar del buzón de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="c405c-105">The **UserIds** element contains an array of delegate users to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="c405c-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c405c-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 <span data-ttu-id="c405c-107">**ArrayOfUserIdType**</span><span class="sxs-lookup"><span data-stu-id="c405c-107">**ArrayOfUserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c405c-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c405c-108">Attributes and elements</span></span>

<span data-ttu-id="c405c-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c405c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c405c-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c405c-110">Attributes</span></span>

<span data-ttu-id="c405c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c405c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c405c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c405c-112">Child elements</span></span>

|<span data-ttu-id="c405c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c405c-113">**Element**</span></span>|<span data-ttu-id="c405c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c405c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c405c-115">UserId</span><span class="sxs-lookup"><span data-stu-id="c405c-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="c405c-116">Identifica un delegado para obtener o quitar del buzón de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="c405c-116">Identifies a delegate to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="c405c-117">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="c405c-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c405c-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c405c-118">Parent elements</span></span>

|<span data-ttu-id="c405c-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c405c-119">**Element**</span></span>|<span data-ttu-id="c405c-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c405c-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c405c-121">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="c405c-121">GetDelegate</span></span>](getdelegate.md) <br/> |<span data-ttu-id="c405c-122">Define una solicitud para obtener información acerca de los delegados de un buzón.</span><span class="sxs-lookup"><span data-stu-id="c405c-122">Defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="c405c-123">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="c405c-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="c405c-124">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="c405c-124">RemoveDelegate</span></span>](removedelegate.md) <br/> |<span data-ttu-id="c405c-125">Define una solicitud para quitar delegados de un buzón.</span><span class="sxs-lookup"><span data-stu-id="c405c-125">Defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="c405c-126">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="c405c-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c405c-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c405c-127">Remarks</span></span>

<span data-ttu-id="c405c-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c405c-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c405c-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c405c-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c405c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="c405c-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c405c-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c405c-131">Schema Name</span></span>  <br/> |<span data-ttu-id="c405c-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c405c-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c405c-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c405c-133">Validation File</span></span>  <br/> |<span data-ttu-id="c405c-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c405c-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c405c-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c405c-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="c405c-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c405c-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c405c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c405c-137">See also</span></span>



[<span data-ttu-id="c405c-138">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="c405c-138">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="c405c-139">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="c405c-139">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="c405c-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c405c-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

