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
description: El elemento GetDelegate define una solicitud para obtener información acerca de los delegados a un buzón de correo. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: e31d6bd4f4387094beb467fcc4dff31ca7ec5d62
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764803"
---
# <a name="getdelegate"></a><span data-ttu-id="b6ec8-104">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="b6ec8-104">GetDelegate</span></span>

<span data-ttu-id="b6ec8-105">El elemento **GetDelegate** define una solicitud para obtener información acerca de los delegados a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-105">The **GetDelegate** element defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="b6ec8-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b6ec8-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 <span data-ttu-id="b6ec8-107">**GetDelegateType**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-107">**GetDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6ec8-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b6ec8-108">Attributes and elements</span></span>

<span data-ttu-id="b6ec8-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6ec8-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6ec8-110">Attributes</span></span>

|<span data-ttu-id="b6ec8-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-111">**Attribute**</span></span>|<span data-ttu-id="b6ec8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6ec8-113">**IncludePermissions**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-113">**IncludePermissions**</span></span> <br/> |<span data-ttu-id="b6ec8-114">Indica si la respuesta contiene la configuración de permisos para cada usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-114">Indicates whether the response contains permission settings for each delegate user.</span></span>  <br/> |
   
#### <a name="includepermissions-attribute-values"></a><span data-ttu-id="b6ec8-115">Valores de atributo de IncludePermissions</span><span class="sxs-lookup"><span data-stu-id="b6ec8-115">IncludePermissions attribute values</span></span>

|<span data-ttu-id="b6ec8-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-116">**Value**</span></span>|<span data-ttu-id="b6ec8-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6ec8-118">**True**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-118">**True**</span></span> <br/> |<span data-ttu-id="b6ec8-119">Delegar permisos se devuelven además de la información del usuario delegado que se devuelve en el elemento [UserId](userid.md) del usuario.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-119">Delegate user permissions are returned in addition to the delegate user information that is returned in the [UserId](userid.md) element.</span></span>  <br/> |
|<span data-ttu-id="b6ec8-120">**False**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-120">**False**</span></span> <br/> |<span data-ttu-id="b6ec8-121">Se devuelve información de [UserId](userid.md) .</span><span class="sxs-lookup"><span data-stu-id="b6ec8-121">[UserId](userid.md) information is returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b6ec8-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b6ec8-122">Child elements</span></span>

|<span data-ttu-id="b6ec8-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-123">**Element**</span></span>|<span data-ttu-id="b6ec8-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6ec8-125">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="b6ec8-125">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="b6ec8-126">Identifica el buzón de correo de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-126">Identifies the principal's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="b6ec8-127">Identificadores de usuario</span><span class="sxs-lookup"><span data-stu-id="b6ec8-127">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="b6ec8-128">Contiene una matriz de delegado a los usuarios obtener desde el buzón de correo de una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-128">Contains an array of delegate users to get from a principal's mailbox.</span></span> <span data-ttu-id="b6ec8-129">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b6ec8-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b6ec8-130">Parent elements</span></span>

<span data-ttu-id="b6ec8-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6ec8-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6ec8-132">Remarks</span></span>

<span data-ttu-id="b6ec8-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6ec8-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b6ec8-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6ec8-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b6ec8-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b6ec8-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b6ec8-136">Schema Name</span></span>  <br/> |<span data-ttu-id="b6ec8-137">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b6ec8-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b6ec8-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b6ec8-138">Validation File</span></span>  <br/> |<span data-ttu-id="b6ec8-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b6ec8-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b6ec8-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b6ec8-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="b6ec8-141">False</span><span class="sxs-lookup"><span data-stu-id="b6ec8-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6ec8-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="b6ec8-142">See also</span></span>



[<span data-ttu-id="b6ec8-143">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="b6ec8-143">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="b6ec8-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b6ec8-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

