---
title: Usuario (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c6bc0031-bc1d-41bd-84e4-9074a5b77012
description: El elemento de usuario representa la identidad de un único usuario.
ms.openlocfilehash: a8dcb22f5c74a9622f978f34e48146115351fe82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840899"
---
# <a name="user-soap"></a><span data-ttu-id="8a766-103">Usuario (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8a766-103">User (SOAP)</span></span>

<span data-ttu-id="8a766-104">El elemento de **usuario** representa la identidad de un único usuario.</span><span class="sxs-lookup"><span data-stu-id="8a766-104">The **User** element represents the identity of a single user.</span></span> 
  
```XML
<User>
    <LegacyDN/>
    <Mailbox/>
    <RequestedSettings/>
</User>
```

 <span data-ttu-id="8a766-105">**User**</span><span class="sxs-lookup"><span data-stu-id="8a766-105">**User**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a766-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8a766-106">Attributes and elements</span></span>

<span data-ttu-id="8a766-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8a766-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a766-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8a766-108">Attributes</span></span>

<span data-ttu-id="8a766-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8a766-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a766-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8a766-110">Child elements</span></span>

|<span data-ttu-id="8a766-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a766-111">**Element**</span></span>|<span data-ttu-id="8a766-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a766-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a766-113">LegacyDN (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8a766-113">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="8a766-114">Representa el nombre distintivo heredado de buzón de correo alternativas.</span><span class="sxs-lookup"><span data-stu-id="8a766-114">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="8a766-115">Buzón de correo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8a766-115">Mailbox (SOAP)</span></span>](mailbox-soap.md) <br/> |<span data-ttu-id="8a766-116">Contiene la dirección de correo electrónico del usuario para ser detectado.</span><span class="sxs-lookup"><span data-stu-id="8a766-116">Contains the e-mail address of the user to be discovered.</span></span>  <br/> |
|[<span data-ttu-id="8a766-117">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8a766-117">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="8a766-118">Contiene los nombres de las opciones de configuración solicitado.</span><span class="sxs-lookup"><span data-stu-id="8a766-118">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8a766-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8a766-119">Parent elements</span></span>

|<span data-ttu-id="8a766-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a766-120">**Element**</span></span>|<span data-ttu-id="8a766-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a766-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a766-122">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8a766-122">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="8a766-123">Representa una colección de elementos de **usuario** .</span><span class="sxs-lookup"><span data-stu-id="8a766-123">Represents a collection of **User** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8a766-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8a766-124">Text value</span></span>

<span data-ttu-id="8a766-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8a766-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a766-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8a766-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a766-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8a766-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="8a766-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8a766-128">Schema Name</span></span>  <br/> |<span data-ttu-id="8a766-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="8a766-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="8a766-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8a766-130">Validation File</span></span>  <br/> |<span data-ttu-id="8a766-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8a766-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a766-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8a766-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="8a766-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="8a766-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a766-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="8a766-134">See also</span></span>



[<span data-ttu-id="8a766-135">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8a766-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="8a766-136">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8a766-136">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="8a766-137">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8a766-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

