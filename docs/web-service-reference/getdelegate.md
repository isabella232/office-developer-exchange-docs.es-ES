---
title: GetDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 6d5efe59-596f-46f8-bdc6-ca9cded9bb8e
description: El elemento GetDelegate define una solicitud para obtener información sobre los delegados de un buzón. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: bd7fb55800b51eb2d69184bc4e04cdef3e6b9a89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461033"
---
# <a name="getdelegate"></a><span data-ttu-id="90c5c-104">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="90c5c-104">GetDelegate</span></span>

<span data-ttu-id="90c5c-105">El elemento **GetDelegate** define una solicitud para obtener información sobre los delegados de un buzón.</span><span class="sxs-lookup"><span data-stu-id="90c5c-105">The **GetDelegate** element defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="90c5c-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="90c5c-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 <span data-ttu-id="90c5c-107">**GetDelegateType**</span><span class="sxs-lookup"><span data-stu-id="90c5c-107">**GetDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90c5c-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="90c5c-108">Attributes and elements</span></span>

<span data-ttu-id="90c5c-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="90c5c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90c5c-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="90c5c-110">Attributes</span></span>

|<span data-ttu-id="90c5c-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="90c5c-111">**Attribute**</span></span>|<span data-ttu-id="90c5c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90c5c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90c5c-113">**IncludePermissions**</span><span class="sxs-lookup"><span data-stu-id="90c5c-113">**IncludePermissions**</span></span> <br/> |<span data-ttu-id="90c5c-114">Indica si la respuesta contiene la configuración de permisos para cada usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="90c5c-114">Indicates whether the response contains permission settings for each delegate user.</span></span>  <br/> |
   
#### <a name="includepermissions-attribute-values"></a><span data-ttu-id="90c5c-115">Valores del atributo IncludePermissions</span><span class="sxs-lookup"><span data-stu-id="90c5c-115">IncludePermissions attribute values</span></span>

|<span data-ttu-id="90c5c-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="90c5c-116">**Value**</span></span>|<span data-ttu-id="90c5c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90c5c-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90c5c-118">**True**</span><span class="sxs-lookup"><span data-stu-id="90c5c-118">**True**</span></span> <br/> |<span data-ttu-id="90c5c-119">Se devuelven los permisos de usuario delegado además de la información de usuario delegada que se devuelve en el elemento [userid](userid.md) .</span><span class="sxs-lookup"><span data-stu-id="90c5c-119">Delegate user permissions are returned in addition to the delegate user information that is returned in the [UserId](userid.md) element.</span></span>  <br/> |
|<span data-ttu-id="90c5c-120">**False**</span><span class="sxs-lookup"><span data-stu-id="90c5c-120">**False**</span></span> <br/> |<span data-ttu-id="90c5c-121">Se devuelve la información de [userid](userid.md) .</span><span class="sxs-lookup"><span data-stu-id="90c5c-121">[UserId](userid.md) information is returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="90c5c-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90c5c-122">Child elements</span></span>

|<span data-ttu-id="90c5c-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="90c5c-123">**Element**</span></span>|<span data-ttu-id="90c5c-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90c5c-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90c5c-125">Buzón</span><span class="sxs-lookup"><span data-stu-id="90c5c-125">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="90c5c-126">Identifica el buzón de la entidad de identidad.</span><span class="sxs-lookup"><span data-stu-id="90c5c-126">Identifies the principal's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="90c5c-127">UserIds</span><span class="sxs-lookup"><span data-stu-id="90c5c-127">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="90c5c-128">Contiene una matriz de usuarios delegados para obtener desde el buzón de una entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="90c5c-128">Contains an array of delegate users to get from a principal's mailbox.</span></span> <span data-ttu-id="90c5c-129">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="90c5c-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="90c5c-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="90c5c-130">Parent elements</span></span>

<span data-ttu-id="90c5c-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="90c5c-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90c5c-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90c5c-132">Remarks</span></span>

<span data-ttu-id="90c5c-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="90c5c-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90c5c-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="90c5c-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90c5c-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="90c5c-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="90c5c-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="90c5c-136">Schema Name</span></span>  <br/> |<span data-ttu-id="90c5c-137">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="90c5c-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="90c5c-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="90c5c-138">Validation File</span></span>  <br/> |<span data-ttu-id="90c5c-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="90c5c-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="90c5c-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="90c5c-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="90c5c-141">Falso</span><span class="sxs-lookup"><span data-stu-id="90c5c-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90c5c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="90c5c-142">See also</span></span>



[<span data-ttu-id="90c5c-143">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="90c5c-143">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="90c5c-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="90c5c-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

