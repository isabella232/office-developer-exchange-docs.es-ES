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
description: El elemento DelegateUsers contiene las identidades de los delegados para agregar o actualizar en un buzón. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 69f5aab65634f41ec0f820da05dee79a300fb32e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457378"
---
# <a name="delegateusers"></a><span data-ttu-id="e6ea8-104">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="e6ea8-104">DelegateUsers</span></span>

<span data-ttu-id="e6ea8-105">El elemento **DelegateUsers** contiene las identidades de los delegados para agregar o actualizar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e6ea8-105">The **DelegateUsers** element contains the identities of delegates to add to or update in a mailbox.</span></span> <span data-ttu-id="e6ea8-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e6ea8-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegateUsers>
   <DelegateUser>
</DelegateUsers>
```

<span data-ttu-id="e6ea8-107">**ArrayOfDelegateUserType**</span><span class="sxs-lookup"><span data-stu-id="e6ea8-107">**ArrayOfDelegateUserType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e6ea8-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e6ea8-108">Attributes and elements</span></span>

<span data-ttu-id="e6ea8-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e6ea8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6ea8-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="e6ea8-110">Attributes</span></span>

<span data-ttu-id="e6ea8-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e6ea8-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6ea8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e6ea8-112">Child elements</span></span>

|<span data-ttu-id="e6ea8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e6ea8-113">**Element**</span></span>|<span data-ttu-id="e6ea8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6ea8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6ea8-115">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="e6ea8-115">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="e6ea8-116">Identifica un único delegado para agregar o actualizar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e6ea8-116">Identifies a single delegate to add to or update in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e6ea8-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e6ea8-117">Parent elements</span></span>

|<span data-ttu-id="e6ea8-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e6ea8-118">**Element**</span></span>|<span data-ttu-id="e6ea8-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6ea8-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6ea8-120">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="e6ea8-120">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="e6ea8-121">Define una solicitud para agregar delegados a un buzón.</span><span class="sxs-lookup"><span data-stu-id="e6ea8-121">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="e6ea8-122">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e6ea8-122">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="e6ea8-123">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="e6ea8-123">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="e6ea8-124">Define una solicitud para actualizar delegados en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e6ea8-124">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="e6ea8-125">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e6ea8-125">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6ea8-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6ea8-126">Remarks</span></span>

<span data-ttu-id="e6ea8-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e6ea8-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6ea8-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e6ea8-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6ea8-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6ea8-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e6ea8-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e6ea8-130">Schema Name</span></span>  <br/> |<span data-ttu-id="e6ea8-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e6ea8-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e6ea8-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e6ea8-132">Validation File</span></span>  <br/> |<span data-ttu-id="e6ea8-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e6ea8-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e6ea8-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e6ea8-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6ea8-135">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ea8-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6ea8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6ea8-136">See also</span></span>

- [<span data-ttu-id="e6ea8-137">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="e6ea8-137">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="e6ea8-138">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="e6ea8-138">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="e6ea8-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e6ea8-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="e6ea8-140">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="e6ea8-140">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

