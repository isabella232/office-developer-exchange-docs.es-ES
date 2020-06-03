---
title: UserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfiguration
api_type:
- schema
ms.assetid: 1811df99-ca5b-48a3-b160-b3fd70320c34
description: El elemento UserConfiguration define un único objeto de configuración de usuario.
ms.openlocfilehash: 1217f5d591570c2d8df49a116b6bf35c243d1e0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468911"
---
# <a name="userconfiguration"></a><span data-ttu-id="e7609-103">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7609-103">UserConfiguration</span></span>

<span data-ttu-id="e7609-104">El elemento **UserConfiguration** define un único objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7609-104">The **UserConfiguration** element defines a single user configuration object.</span></span> 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 <span data-ttu-id="e7609-105">**UserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="e7609-105">**UserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e7609-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e7609-106">Attributes and elements</span></span>

<span data-ttu-id="e7609-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e7609-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7609-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e7609-108">Attributes</span></span>

<span data-ttu-id="e7609-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e7609-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7609-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e7609-110">Child elements</span></span>

|<span data-ttu-id="e7609-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e7609-111">**Element**</span></span>|<span data-ttu-id="e7609-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7609-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7609-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e7609-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="e7609-114">Representa el nombre de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7609-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="e7609-115">Este elemento debe usarse cuando se crea un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7609-115">This element must be used when you create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="e7609-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="e7609-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="e7609-117">Define el identificador de elemento de objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7609-117">Defines the user configuration object item identifier.</span></span>  <br/> |
|[<span data-ttu-id="e7609-118">Diccionario</span><span class="sxs-lookup"><span data-stu-id="e7609-118">Dictionary</span></span>](dictionary.md) <br/> |<span data-ttu-id="e7609-119">Define un conjunto de entradas de propiedades de diccionario para un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7609-119">Defines a set of dictionary property entries for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="e7609-120">XmlData</span><span class="sxs-lookup"><span data-stu-id="e7609-120">XmlData</span></span>](xmldata.md) <br/> |<span data-ttu-id="e7609-121">Contiene el contenido de la propiedad de datos XML para un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7609-121">Contains XML data property content for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="e7609-122">BinaryData</span><span class="sxs-lookup"><span data-stu-id="e7609-122">BinaryData</span></span>](binarydata.md) <br/> |<span data-ttu-id="e7609-123">Contiene el contenido de la propiedad de datos binarios de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7609-123">Contains binary data property content for a user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e7609-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e7609-124">Parent elements</span></span>

|<span data-ttu-id="e7609-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e7609-125">**Element**</span></span>|<span data-ttu-id="e7609-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7609-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7609-127">CreateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7609-127">CreateUserConfiguration</span></span>](createuserconfiguration.md) <br/> |<span data-ttu-id="e7609-128">Representa una solicitud para crear un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7609-128">Represents a request to create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="e7609-129">GetUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e7609-129">GetUserConfigurationResponseMessage</span></span>](getuserconfigurationresponsemessage.md) <br/> |<span data-ttu-id="e7609-130">Representa una respuesta que devuelve un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7609-130">Represents a response that returns a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="e7609-131">UpdateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7609-131">UpdateUserConfiguration</span></span>](updateuserconfiguration.md) <br/> |<span data-ttu-id="e7609-132">Representa una solicitud para actualizar un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7609-132">Represents a request to update a user configuration object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7609-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7609-133">Remarks</span></span>

<span data-ttu-id="e7609-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7609-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7609-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e7609-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7609-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7609-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e7609-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e7609-137">Schema Name</span></span>  <br/> |<span data-ttu-id="e7609-138">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e7609-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e7609-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e7609-139">Validation File</span></span>  <br/> |<span data-ttu-id="e7609-140">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e7609-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e7609-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e7609-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="e7609-142">Falso</span><span class="sxs-lookup"><span data-stu-id="e7609-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7609-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7609-143">See also</span></span>



- [<span data-ttu-id="e7609-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e7609-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

