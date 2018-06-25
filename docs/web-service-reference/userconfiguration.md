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
description: El elemento UserConfiguration define un objeto de configuración de usuario único.
ms.openlocfilehash: ce3eaa470ef592c5a8e5a7ef24c377bb2feeca2e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840901"
---
# <a name="userconfiguration"></a><span data-ttu-id="ba264-103">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba264-103">UserConfiguration</span></span>

<span data-ttu-id="ba264-104">El elemento **UserConfiguration** define un objeto de configuración de usuario único.</span><span class="sxs-lookup"><span data-stu-id="ba264-104">The **UserConfiguration** element defines a single user configuration object.</span></span> 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 <span data-ttu-id="ba264-105">**UserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="ba264-105">**UserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba264-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ba264-106">Attributes and elements</span></span>

<span data-ttu-id="ba264-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ba264-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba264-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba264-108">Attributes</span></span>

<span data-ttu-id="ba264-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba264-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba264-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba264-110">Child elements</span></span>

|<span data-ttu-id="ba264-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba264-111">**Element**</span></span>|<span data-ttu-id="ba264-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba264-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba264-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ba264-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="ba264-114">Representa el nombre de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ba264-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="ba264-115">Este elemento se debe usar al crear un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ba264-115">This element must be used when you create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ba264-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="ba264-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="ba264-117">Define el identificador de elemento de objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ba264-117">Defines the user configuration object item identifier.</span></span>  <br/> |
|[<span data-ttu-id="ba264-118">Diccionario</span><span class="sxs-lookup"><span data-stu-id="ba264-118">Dictionary</span></span>](dictionary.md) <br/> |<span data-ttu-id="ba264-119">Define un conjunto de entradas de diccionario (propiedad) para un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ba264-119">Defines a set of dictionary property entries for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ba264-120">Nota</span><span class="sxs-lookup"><span data-stu-id="ba264-120">XmlData</span></span>](xmldata.md) <br/> |<span data-ttu-id="ba264-121">Contiene contenido de propiedad de datos XML para un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ba264-121">Contains XML data property content for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ba264-122">BinaryData</span><span class="sxs-lookup"><span data-stu-id="ba264-122">BinaryData</span></span>](binarydata.md) <br/> |<span data-ttu-id="ba264-123">Contiene el contenido de la propiedad de datos binarios para un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ba264-123">Contains binary data property content for a user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba264-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba264-124">Parent elements</span></span>

|<span data-ttu-id="ba264-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba264-125">**Element**</span></span>|<span data-ttu-id="ba264-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba264-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba264-127">CreateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba264-127">CreateUserConfiguration</span></span>](createuserconfiguration.md) <br/> |<span data-ttu-id="ba264-128">Representa una solicitud para crear un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ba264-128">Represents a request to create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ba264-129">GetUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ba264-129">GetUserConfigurationResponseMessage</span></span>](getuserconfigurationresponsemessage.md) <br/> |<span data-ttu-id="ba264-130">Representa una respuesta que devuelve un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ba264-130">Represents a response that returns a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ba264-131">UpdateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba264-131">UpdateUserConfiguration</span></span>](updateuserconfiguration.md) <br/> |<span data-ttu-id="ba264-132">Representa una solicitud para actualizar un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ba264-132">Represents a request to update a user configuration object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba264-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba264-133">Remarks</span></span>

<span data-ttu-id="ba264-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba264-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba264-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba264-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba264-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ba264-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ba264-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ba264-137">Schema Name</span></span>  <br/> |<span data-ttu-id="ba264-138">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ba264-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ba264-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ba264-139">Validation File</span></span>  <br/> |<span data-ttu-id="ba264-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ba264-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ba264-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba264-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba264-142">False</span><span class="sxs-lookup"><span data-stu-id="ba264-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba264-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba264-143">See also</span></span>



- [<span data-ttu-id="ba264-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ba264-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

