---
title: GetUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserConfiguration
api_type:
- schema
ms.assetid: 4044c0a1-cd88-41ae-9cc4-a7cf2b279094
description: El elemento GetUserConfiguration representa una solicitud para obtener un objeto de configuración de usuario.
ms.openlocfilehash: 46a2a5ebbabfc038692a5de83e0a960e05295061
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457714"
---
# <a name="getuserconfiguration"></a><span data-ttu-id="3b08a-103">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b08a-103">GetUserConfiguration</span></span>

<span data-ttu-id="3b08a-104">El elemento **GetUserConfiguration** representa una solicitud para obtener un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3b08a-104">The **GetUserConfiguration** element represent a request to get a user configuration object.</span></span> 
  
```XML
<GetUserConfiguration>
   <UserConfigurationName/>
   <UserConfigurationProperties/>
</GetUserConfiguration>
```

 <span data-ttu-id="3b08a-105">**GetUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="3b08a-105">**GetUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b08a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3b08a-106">Attributes and elements</span></span>

<span data-ttu-id="3b08a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3b08a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b08a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3b08a-108">Attributes</span></span>

<span data-ttu-id="3b08a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3b08a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b08a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3b08a-110">Child elements</span></span>

|<span data-ttu-id="3b08a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3b08a-111">**Element**</span></span>|<span data-ttu-id="3b08a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b08a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b08a-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3b08a-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="3b08a-114">Representa el nombre de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3b08a-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="3b08a-115">Este elemento debe estar presente en una solicitud GetUserConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3b08a-115">This element must be present in a GetUserConfiguration request.</span></span>  <br/> |
|[<span data-ttu-id="3b08a-116">UserConfigurationProperties</span><span class="sxs-lookup"><span data-stu-id="3b08a-116">UserConfigurationProperties</span></span>](userconfigurationproperties.md) <br/> |<span data-ttu-id="3b08a-117">Especifica los tipos de propiedades de configuración de usuario que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="3b08a-117">Specifies the user configuration property types to return.</span></span> <span data-ttu-id="3b08a-118">Este elemento debe estar presente en una solicitud GetUserConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3b08a-118">This element must be present in a GetUserConfiguration request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3b08a-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3b08a-119">Parent elements</span></span>

<span data-ttu-id="3b08a-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3b08a-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="3b08a-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3b08a-121">Text value</span></span>

<span data-ttu-id="3b08a-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b08a-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b08a-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b08a-123">Remarks</span></span>

<span data-ttu-id="3b08a-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3b08a-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b08a-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3b08a-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b08a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b08a-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3b08a-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3b08a-127">Schema Name</span></span>  <br/> |<span data-ttu-id="3b08a-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3b08a-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3b08a-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3b08a-129">Validation File</span></span>  <br/> |<span data-ttu-id="3b08a-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3b08a-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3b08a-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3b08a-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b08a-132">Falso</span><span class="sxs-lookup"><span data-stu-id="3b08a-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b08a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b08a-133">See also</span></span>



- [<span data-ttu-id="3b08a-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3b08a-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

