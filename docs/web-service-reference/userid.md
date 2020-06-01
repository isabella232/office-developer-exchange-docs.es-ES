---
title: UserId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserId
api_type:
- schema
ms.assetid: 244af9e0-bf3c-46b4-8bfa-9719a1ed3107
description: El elemento UserId identifica un usuario delegado o un usuario que tiene permisos de acceso a la carpeta.
ms.openlocfilehash: 68075e335383835ddce9575d85ba5fa945ed305c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455544"
---
# <a name="userid"></a><span data-ttu-id="50552-103">UserId</span><span class="sxs-lookup"><span data-stu-id="50552-103">UserId</span></span>

<span data-ttu-id="50552-104">El elemento **userid** identifica un usuario delegado o un usuario que tiene permisos de acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="50552-104">The **UserId** element identifies a delegate user or a user who has folder access permissions.</span></span> 
  
```xml
<UserId>
   <SID/>
   <PrimarySmtpAddress/>
   <DisplayName/>
   <DistinguishedUser/>
   <ExternalUserIdentity/>
</UserId>
```

 <span data-ttu-id="50552-105">**UserIdType**</span><span class="sxs-lookup"><span data-stu-id="50552-105">**UserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50552-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="50552-106">Attributes and elements</span></span>

<span data-ttu-id="50552-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="50552-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50552-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="50552-108">Attributes</span></span>

<span data-ttu-id="50552-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="50552-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50552-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="50552-110">Child elements</span></span>

|<span data-ttu-id="50552-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="50552-111">**Element**</span></span>|<span data-ttu-id="50552-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50552-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50552-113">SID</span><span class="sxs-lookup"><span data-stu-id="50552-113">SID</span></span>](sid.md) <br/> |<span data-ttu-id="50552-114">Representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="50552-114">Represents the security descriptor definition language (SDDL) form of the security identifier (SID).</span></span>  <br/> |
|[<span data-ttu-id="50552-115">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="50552-115">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="50552-116">Representa la dirección de Protocolo simple de transferencia de correo (SMTP) principal de una cuenta que se va a usar para el acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="50552-116">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for delegate access.</span></span>  <br/> |
|[<span data-ttu-id="50552-117">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="50552-117">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="50552-118">Define el nombre para mostrar de una carpeta, un contacto, una lista de distribución o un usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="50552-118">Defines the display name of a folder, contact, distribution list, or delegate user.</span></span>  <br/> |
|[<span data-ttu-id="50552-119">DistinguishedUser</span><span class="sxs-lookup"><span data-stu-id="50552-119">DistinguishedUser</span></span>](distinguisheduser.md) <br/> |<span data-ttu-id="50552-120">Identifica cuentas de usuario anónimas y predeterminadas para el acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="50552-120">Identifies Anonymous and Default user accounts for delegate access.</span></span>  <br/> |
|[<span data-ttu-id="50552-121">ExternalUserIdentity</span><span class="sxs-lookup"><span data-stu-id="50552-121">ExternalUserIdentity</span></span>](externaluseridentity.md) <br/> |<span data-ttu-id="50552-122">Identifica un usuario delegado externo o un usuario externo que tiene permisos de acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="50552-122">Identifies an external delegate user or an external user who has folder access permissions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="50552-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="50552-123">Parent elements</span></span>

|<span data-ttu-id="50552-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="50552-124">**Element**</span></span>|<span data-ttu-id="50552-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50552-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50552-126">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="50552-126">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="50552-127">Identifica un único delegado para agregar o actualizar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="50552-127">Identifies a single delegate to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="50552-128">Permiso</span><span class="sxs-lookup"><span data-stu-id="50552-128">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="50552-129">Define el acceso que un usuario tiene a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="50552-129">Defines the access that a user has to a folder.</span></span>  <br/> |
|[<span data-ttu-id="50552-130">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="50552-130">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="50552-131">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="50552-131">Defines the access that a user has to a Calendar folder.</span></span>  <br/> |
|[<span data-ttu-id="50552-132">UserIds</span><span class="sxs-lookup"><span data-stu-id="50552-132">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="50552-133">Contiene una matriz de usuarios delegados para obtener o quitar del buzón de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="50552-133">Contains an array of delegate users to get or remove from a principal's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="50552-134">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="50552-134">Text value</span></span>

<span data-ttu-id="50552-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="50552-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50552-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50552-136">Remarks</span></span>

<span data-ttu-id="50552-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="50552-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50552-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="50552-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50552-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="50552-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="50552-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="50552-140">Schema Name</span></span>  <br/> |<span data-ttu-id="50552-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="50552-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="50552-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="50552-142">Validation File</span></span>  <br/> |<span data-ttu-id="50552-143">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="50552-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="50552-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="50552-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="50552-145">Falso</span><span class="sxs-lookup"><span data-stu-id="50552-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50552-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="50552-146">See also</span></span>



[<span data-ttu-id="50552-147">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="50552-147">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="50552-148">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="50552-148">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="50552-149">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="50552-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="50552-150">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="50552-150">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

