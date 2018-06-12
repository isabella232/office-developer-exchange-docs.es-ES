---
title: DelegateUsers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUsers
api_type:
- schema
ms.assetid: f30f80d9-20c8-41cc-afc7-a5eec1e0c5ea
description: El elemento DelegateUsers contiene las identidades de delegados para agregar o actualizar en un buzón de correo. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: a078707ae6b1676ca5a32ba718add93debd498fe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764068"
---
# <a name="delegateusers"></a><span data-ttu-id="dd830-104">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="dd830-104">DelegateUsers</span></span>

<span data-ttu-id="dd830-105">El elemento **DelegateUsers** contiene las identidades de delegados para agregar o actualizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="dd830-105">The **DelegateUsers** element contains the identities of delegates to add to or update in a mailbox.</span></span> <span data-ttu-id="dd830-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="dd830-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegateUsers>
   <DelegateUser>
</DelegateUsers>
```

<span data-ttu-id="dd830-107">**ArrayOfDelegateUserType**</span><span class="sxs-lookup"><span data-stu-id="dd830-107">**ArrayOfDelegateUserType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="dd830-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dd830-108">Attributes and elements</span></span>

<span data-ttu-id="dd830-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dd830-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd830-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="dd830-110">Attributes</span></span>

<span data-ttu-id="dd830-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd830-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd830-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dd830-112">Child elements</span></span>

|<span data-ttu-id="dd830-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd830-113">**Element**</span></span>|<span data-ttu-id="dd830-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd830-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd830-115">UsuarioDelegado</span><span class="sxs-lookup"><span data-stu-id="dd830-115">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="dd830-116">Identifica un único delegado para agregar o actualizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="dd830-116">Identifies a single delegate to add to or update in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dd830-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dd830-117">Parent elements</span></span>

|<span data-ttu-id="dd830-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd830-118">**Element**</span></span>|<span data-ttu-id="dd830-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd830-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd830-120">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="dd830-120">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="dd830-121">Define una solicitud para agregar delegados a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="dd830-121">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="dd830-122">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="dd830-122">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="dd830-123">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="dd830-123">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="dd830-124">Define una solicitud para actualizar los delegados en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="dd830-124">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="dd830-125">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="dd830-125">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd830-126">Notas</span><span class="sxs-lookup"><span data-stu-id="dd830-126">Remarks</span></span>

<span data-ttu-id="dd830-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="dd830-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd830-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dd830-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd830-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd830-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd830-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dd830-130">Schema Name</span></span>  <br/> |<span data-ttu-id="dd830-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="dd830-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dd830-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dd830-132">Validation File</span></span>  <br/> |<span data-ttu-id="dd830-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dd830-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd830-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dd830-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="dd830-135">False</span><span class="sxs-lookup"><span data-stu-id="dd830-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd830-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="dd830-136">See also</span></span>

- [<span data-ttu-id="dd830-137">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="dd830-137">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="dd830-138">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="dd830-138">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="dd830-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="dd830-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="dd830-140">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="dd830-140">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

