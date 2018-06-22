---
title: ActingAs
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
description: El elemento ActingAs identifica quién envía como el autor de la llamada.
ms.openlocfilehash: 9c007ed45f85dba265261dd79a6fd846dbd9d2f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764568"
---
# <a name="actingas"></a><span data-ttu-id="de88c-103">ActingAs</span><span class="sxs-lookup"><span data-stu-id="de88c-103">ActingAs</span></span>

<span data-ttu-id="de88c-104">El elemento **ActingAs** identifica quién envía como el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="de88c-104">The **ActingAs** element identifies who the caller is sending as.</span></span> 
  
```xml
<ActingAs>
   <EmailAddress/>
   <RoutingType/>
</ActingAs>
```

 <span data-ttu-id="de88c-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="de88c-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de88c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="de88c-106">Attributes and elements</span></span>

<span data-ttu-id="de88c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="de88c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de88c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="de88c-108">Attributes</span></span>

<span data-ttu-id="de88c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="de88c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de88c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="de88c-110">Child elements</span></span>

|<span data-ttu-id="de88c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="de88c-111">**Element**</span></span>|<span data-ttu-id="de88c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de88c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de88c-113">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="de88c-113">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="de88c-114">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="de88c-114">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="de88c-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="de88c-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="de88c-116">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="de88c-116">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="de88c-117">Define la ruta que se usa para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="de88c-117">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="de88c-118">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="de88c-118">The default is SMTP.</span></span> <span data-ttu-id="de88c-119">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="de88c-119">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de88c-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="de88c-120">Parent elements</span></span>

|<span data-ttu-id="de88c-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="de88c-121">**Element**</span></span>|<span data-ttu-id="de88c-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de88c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de88c-123">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="de88c-123">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="de88c-124">Define una solicitud **GetServiceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="de88c-124">Defines a **GetServiceConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de88c-125">Notas</span><span class="sxs-lookup"><span data-stu-id="de88c-125">Remarks</span></span>

<span data-ttu-id="de88c-126">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="de88c-126">This element is optional.</span></span> <span data-ttu-id="de88c-127">Si este elemento no está presente, el usuario autenticado se supone que el remitente.</span><span class="sxs-lookup"><span data-stu-id="de88c-127">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="de88c-128">El elemento **ActingAs** debe incluirse para solicitar sugerencias de remitente.</span><span class="sxs-lookup"><span data-stu-id="de88c-128">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="de88c-129">Puede devolver un error de **ErrorInvalidArgument** en una respuesta si el elemento **ActingAs** falta, no incluye un tipo de distribución, no incluye una dirección de correo electrónico, contiene una dirección de correo electrónico no válida, no se resuelve a un usuario en Active Directory Servicios de dominio (AD DS), o se resuelve a varios usuarios en AD DS.</span><span class="sxs-lookup"><span data-stu-id="de88c-129">An **ErrorInvalidArgument** error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span> 
  
<span data-ttu-id="de88c-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="de88c-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de88c-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="de88c-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de88c-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="de88c-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="de88c-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="de88c-133">Schema Name</span></span>  <br/> |<span data-ttu-id="de88c-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="de88c-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="de88c-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="de88c-135">Validation File</span></span>  <br/> |<span data-ttu-id="de88c-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="de88c-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="de88c-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="de88c-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="de88c-138">False</span><span class="sxs-lookup"><span data-stu-id="de88c-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de88c-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="de88c-139">See also</span></span>

- [<span data-ttu-id="de88c-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="de88c-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

