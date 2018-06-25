---
title: UsuarioDelegado
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUser
api_type:
- schema
ms.assetid: aac4e74e-f69b-4c41-a0c9-489610330fbf
description: El elemento UsuarioDelegado identifica un único delegado para agregar o actualizar en un buzón o un delegado devueltas en una respuesta de administración de delegado. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 72ddc313a5a76cd0345918cad63b7775ff85026b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764070"
---
# <a name="delegateuser"></a><span data-ttu-id="464a2-104">UsuarioDelegado</span><span class="sxs-lookup"><span data-stu-id="464a2-104">DelegateUser</span></span>

<span data-ttu-id="464a2-105">El elemento **UsuarioDelegado** identifica un único delegado para agregar o actualizar en un buzón o un delegado devueltas en una respuesta de administración de delegado.</span><span class="sxs-lookup"><span data-stu-id="464a2-105">The **DelegateUser** element identifies a single delegate to add or update in a mailbox or a delegate returned in a delegate management response.</span></span> <span data-ttu-id="464a2-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="464a2-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegateUser>
   <UserId/>
   <DelegatePermissions/>
   <ReceiveCopiesOfMeetingMessages/>
   <ViewPrivateItems/>
</DelegateUser>
```

<span data-ttu-id="464a2-107">**DelegateUserType**</span><span class="sxs-lookup"><span data-stu-id="464a2-107">**DelegateUserType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="464a2-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="464a2-108">Attributes and elements</span></span>

<span data-ttu-id="464a2-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="464a2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="464a2-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="464a2-110">Attributes</span></span>

<span data-ttu-id="464a2-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="464a2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="464a2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="464a2-112">Child elements</span></span>

|<span data-ttu-id="464a2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="464a2-113">**Element**</span></span>|<span data-ttu-id="464a2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="464a2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="464a2-115">UserId</span><span class="sxs-lookup"><span data-stu-id="464a2-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="464a2-116">Identifica al delegado.</span><span class="sxs-lookup"><span data-stu-id="464a2-116">Identifies the delegate.</span></span> <span data-ttu-id="464a2-117">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="464a2-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="464a2-118">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="464a2-118">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="464a2-119">Contiene la configuración de nivel de permisos de delegado.</span><span class="sxs-lookup"><span data-stu-id="464a2-119">Contains the delegate permission level settings.</span></span> <span data-ttu-id="464a2-120">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="464a2-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="464a2-121">ReceiveCopiesOfMeetingMessages</span><span class="sxs-lookup"><span data-stu-id="464a2-121">ReceiveCopiesOfMeetingMessages</span></span>](receivecopiesofmeetingmessages.md) <br/> |<span data-ttu-id="464a2-122">Indica si un delegado reciba copias de los mensajes de reunión que se dirigen a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="464a2-122">Indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal.</span></span> <span data-ttu-id="464a2-123">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="464a2-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="464a2-124">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="464a2-124">ViewPrivateItems</span></span>](viewprivateitems.md) <br/> |<span data-ttu-id="464a2-125">Indica si un delegado tiene permiso para ver los elementos de calendario privados en el buzón de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="464a2-125">Indicates whether a delegate has permission to view private calendar items in the principal's mailbox.</span></span> <span data-ttu-id="464a2-126">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="464a2-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="464a2-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="464a2-127">Parent elements</span></span>

|<span data-ttu-id="464a2-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="464a2-128">**Element**</span></span>|<span data-ttu-id="464a2-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="464a2-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="464a2-130">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="464a2-130">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="464a2-131">Contiene las identidades de los delegados para agregar o actualizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="464a2-131">Contains the identities of delegates to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="464a2-132">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="464a2-132">DelegateUserResponseMessageType</span></span>](delegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="464a2-133">Contiene los mensajes de respuesta para las operaciones de administración de delegado.</span><span class="sxs-lookup"><span data-stu-id="464a2-133">Contains response messages for delegate management operations.</span></span> <span data-ttu-id="464a2-134">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="464a2-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="464a2-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="464a2-135">Remarks</span></span>

<span data-ttu-id="464a2-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="464a2-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="464a2-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="464a2-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="464a2-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="464a2-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="464a2-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="464a2-139">Schema Name</span></span>  <br/> |<span data-ttu-id="464a2-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="464a2-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="464a2-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="464a2-141">Validation File</span></span>  <br/> |<span data-ttu-id="464a2-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="464a2-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="464a2-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="464a2-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="464a2-144">False</span><span class="sxs-lookup"><span data-stu-id="464a2-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="464a2-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="464a2-145">See also</span></span>

- [<span data-ttu-id="464a2-146">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="464a2-146">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="464a2-147">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="464a2-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="464a2-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="464a2-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="464a2-149">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="464a2-149">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

