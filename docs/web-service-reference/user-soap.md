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
description: El elemento User representa la identidad de un único usuario.
ms.openlocfilehash: f151ffa8050a10cdbb4562471d815f8692596cc3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456349"
---
# <a name="user-soap"></a><span data-ttu-id="c1ca5-103">Usuario (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1ca5-103">User (SOAP)</span></span>

<span data-ttu-id="c1ca5-104">El elemento **User** representa la identidad de un único usuario.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-104">The **User** element represents the identity of a single user.</span></span> 
  
```XML
<User>
    <LegacyDN/>
    <Mailbox/>
    <RequestedSettings/>
</User>
```

 <span data-ttu-id="c1ca5-105">**User**</span><span class="sxs-lookup"><span data-stu-id="c1ca5-105">**User**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1ca5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1ca5-106">Attributes and elements</span></span>

<span data-ttu-id="c1ca5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1ca5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1ca5-108">Attributes</span></span>

<span data-ttu-id="c1ca5-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1ca5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1ca5-110">Child elements</span></span>

|<span data-ttu-id="c1ca5-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1ca5-111">**Element**</span></span>|<span data-ttu-id="c1ca5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1ca5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1ca5-113">LegacyDN (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1ca5-113">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="c1ca5-114">Representa el nombre distintivo heredado de buzón alternativo.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-114">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="c1ca5-115">Buzón de correo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1ca5-115">Mailbox (SOAP)</span></span>](mailbox-soap.md) <br/> |<span data-ttu-id="c1ca5-116">Contiene la dirección de correo electrónico del usuario que se va a detectar.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-116">Contains the e-mail address of the user to be discovered.</span></span>  <br/> |
|[<span data-ttu-id="c1ca5-117">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1ca5-117">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="c1ca5-118">Contiene los nombres de las opciones de configuración solicitadas.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-118">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1ca5-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1ca5-119">Parent elements</span></span>

|<span data-ttu-id="c1ca5-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1ca5-120">**Element**</span></span>|<span data-ttu-id="c1ca5-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1ca5-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1ca5-122">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1ca5-122">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="c1ca5-123">Representa una colección de elementos **User** .</span><span class="sxs-lookup"><span data-stu-id="c1ca5-123">Represents a collection of **User** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1ca5-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c1ca5-124">Text value</span></span>

<span data-ttu-id="c1ca5-125">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1ca5-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1ca5-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1ca5-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1ca5-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="c1ca5-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c1ca5-128">Schema Name</span></span>  <br/> |<span data-ttu-id="c1ca5-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="c1ca5-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="c1ca5-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c1ca5-130">Validation File</span></span>  <br/> |<span data-ttu-id="c1ca5-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c1ca5-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1ca5-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c1ca5-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1ca5-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c1ca5-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1ca5-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1ca5-134">See also</span></span>



[<span data-ttu-id="c1ca5-135">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1ca5-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="c1ca5-136">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1ca5-136">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="c1ca5-137">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1ca5-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

