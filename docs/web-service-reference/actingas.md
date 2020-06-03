---
title: Acciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ActingAs
api_type:
- schema
ms.assetid: 3896afff-5c2c-4eaf-8621-c70e0371ea78
description: El elemento Actuaas identifica quién envía el autor de la llamada.
ms.openlocfilehash: 175a03018ee3529ec595dbe9afb7dc61ad6afc35
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529703"
---
# <a name="actingas"></a><span data-ttu-id="259ee-103">Acciones</span><span class="sxs-lookup"><span data-stu-id="259ee-103">ActingAs</span></span>

<span data-ttu-id="259ee-104">El elemento **actuaas** identifica quién envía el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="259ee-104">The **ActingAs** element identifies who the caller is sending as.</span></span> 
  
```xml
<ActingAs>
   <EmailAddress/>
   <RoutingType/>
</ActingAs>
```

 <span data-ttu-id="259ee-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="259ee-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="259ee-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="259ee-106">Attributes and elements</span></span>

<span data-ttu-id="259ee-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="259ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="259ee-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="259ee-108">Attributes</span></span>

<span data-ttu-id="259ee-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="259ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="259ee-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="259ee-110">Child elements</span></span>

|<span data-ttu-id="259ee-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="259ee-111">**Element**</span></span>|<span data-ttu-id="259ee-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="259ee-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="259ee-113">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="259ee-113">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="259ee-114">Define la dirección del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="259ee-114">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="259ee-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="259ee-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="259ee-116">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="259ee-116">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="259ee-117">Define la ruta que se usa para el buzón.</span><span class="sxs-lookup"><span data-stu-id="259ee-117">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="259ee-118">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="259ee-118">The default is SMTP.</span></span> <span data-ttu-id="259ee-119">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="259ee-119">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="259ee-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="259ee-120">Parent elements</span></span>

|<span data-ttu-id="259ee-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="259ee-121">**Element**</span></span>|<span data-ttu-id="259ee-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="259ee-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="259ee-123">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="259ee-123">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="259ee-124">Define una solicitud de **GetServiceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="259ee-124">Defines a **GetServiceConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="259ee-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="259ee-125">Remarks</span></span>

<span data-ttu-id="259ee-126">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="259ee-126">This element is optional.</span></span> <span data-ttu-id="259ee-127">Si este elemento no está presente, se supone que el usuario autenticado es el remitente.</span><span class="sxs-lookup"><span data-stu-id="259ee-127">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="259ee-128">El elemento **actual** debe incluirse para solicitar sugerencias de remitente.</span><span class="sxs-lookup"><span data-stu-id="259ee-128">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="259ee-129">Se puede devolver un error **ErrorInvalidArgument** en una respuesta si falta el elemento **actuaas** , no incluye un tipo de enrutamiento, no incluye una dirección de correo electrónico, contiene una dirección de correo electrónico no válida, no se resuelve como un usuario de los servicios de dominio de Active Directory (AD DS) o se resuelve en varios usuarios en AD DS.</span><span class="sxs-lookup"><span data-stu-id="259ee-129">An **ErrorInvalidArgument** error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span> 
  
<span data-ttu-id="259ee-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="259ee-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="259ee-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="259ee-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="259ee-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="259ee-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="259ee-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="259ee-133">Schema Name</span></span>  <br/> |<span data-ttu-id="259ee-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="259ee-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="259ee-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="259ee-135">Validation File</span></span>  <br/> |<span data-ttu-id="259ee-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="259ee-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="259ee-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="259ee-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="259ee-138">Falso</span><span class="sxs-lookup"><span data-stu-id="259ee-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="259ee-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="259ee-139">See also</span></span>

- [<span data-ttu-id="259ee-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="259ee-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

