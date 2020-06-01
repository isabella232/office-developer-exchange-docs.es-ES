---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: El elemento GetServiceConfiguration define una solicitud de GetServiceConfiguration.
ms.openlocfilehash: e9357a9e3be22e129c4910c01231f9dbd22a2dbe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457875"
---
# <a name="getserviceconfiguration"></a><span data-ttu-id="84907-103">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="84907-103">GetServiceConfiguration</span></span>

<span data-ttu-id="84907-104">El elemento **GetServiceConfiguration** define una solicitud de GetServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="84907-104">The **GetServiceConfiguration** element defines a GetServiceConfiguration request.</span></span> 
  
```XML
<GetServiceConfiguration>
   <ActingAs/>
   <RequestedConfiguration/>
</GetServiceConfiguration>
```

 <span data-ttu-id="84907-105">**GetServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="84907-105">**GetServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84907-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="84907-106">Attributes and elements</span></span>

<span data-ttu-id="84907-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="84907-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84907-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="84907-108">Attributes</span></span>

<span data-ttu-id="84907-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="84907-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84907-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="84907-110">Child elements</span></span>

|<span data-ttu-id="84907-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="84907-111">**Element**</span></span>|<span data-ttu-id="84907-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84907-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84907-113">Acciones</span><span class="sxs-lookup"><span data-stu-id="84907-113">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="84907-114">Identifica quién envía el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="84907-114">Identifies who the caller is sending as.</span></span> <span data-ttu-id="84907-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="84907-115">This element is optional.</span></span> <span data-ttu-id="84907-116">Si este elemento no está presente, se supone que el usuario autenticado es el remitente.</span><span class="sxs-lookup"><span data-stu-id="84907-116">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="84907-117">El elemento **actual** debe incluirse para solicitar sugerencias de remitente.</span><span class="sxs-lookup"><span data-stu-id="84907-117">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="84907-118">Se puede devolver un error ErrorInvalidArgument en una respuesta si falta el elemento **actuaas** , no incluye un tipo de enrutamiento, no incluye una dirección de correo electrónico, contiene una dirección de correo electrónico no válida, no se resuelve como un usuario de los servicios de dominio de Active Directory (AD DS) o se resuelve en varios usuarios en AD DS.</span><span class="sxs-lookup"><span data-stu-id="84907-118">An ErrorInvalidArgument error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span>  <br/> |
|[<span data-ttu-id="84907-119">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="84907-119">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="84907-120">Contiene las configuraciones de servicio solicitadas.</span><span class="sxs-lookup"><span data-stu-id="84907-120">Contains the requested service configurations.</span></span> <span data-ttu-id="84907-121">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="84907-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84907-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="84907-122">Parent elements</span></span>

<span data-ttu-id="84907-123">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="84907-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="84907-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="84907-124">Text value</span></span>

<span data-ttu-id="84907-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="84907-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84907-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84907-126">Remarks</span></span>

<span data-ttu-id="84907-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="84907-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84907-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="84907-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84907-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="84907-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="84907-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="84907-130">Schema Name</span></span>  <br/> |<span data-ttu-id="84907-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="84907-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="84907-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="84907-132">Validation File</span></span>  <br/> |<span data-ttu-id="84907-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="84907-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="84907-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="84907-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="84907-135">Falso</span><span class="sxs-lookup"><span data-stu-id="84907-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84907-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="84907-136">See also</span></span>



- [<span data-ttu-id="84907-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="84907-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

