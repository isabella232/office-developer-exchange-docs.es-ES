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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840901"
---
# <a name="userconfiguration"></a><span data-ttu-id="3eb40-103">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="3eb40-103">UserConfiguration</span></span>

<span data-ttu-id="3eb40-104">El elemento **UserConfiguration** define un objeto de configuración de usuario único.</span><span class="sxs-lookup"><span data-stu-id="3eb40-104">The **UserConfiguration** element defines a single user configuration object.</span></span> 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 <span data-ttu-id="3eb40-105">**UserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="3eb40-105">**UserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3eb40-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3eb40-106">Attributes and elements</span></span>

<span data-ttu-id="3eb40-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3eb40-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3eb40-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3eb40-108">Attributes</span></span>

<span data-ttu-id="3eb40-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3eb40-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3eb40-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3eb40-110">Child elements</span></span>

|<span data-ttu-id="3eb40-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3eb40-111">**Element**</span></span>|<span data-ttu-id="3eb40-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3eb40-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3eb40-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3eb40-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="3eb40-114">Representa el nombre de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3eb40-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="3eb40-115">Este elemento se debe usar al crear un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3eb40-115">This element must be used when you create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="3eb40-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="3eb40-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3eb40-117">Define el identificador de elemento de objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3eb40-117">Defines the user configuration object item identifier.</span></span>  <br/> |
|[<span data-ttu-id="3eb40-118">Diccionario</span><span class="sxs-lookup"><span data-stu-id="3eb40-118">Dictionary</span></span>](dictionary.md) <br/> |<span data-ttu-id="3eb40-119">Define un conjunto de entradas de diccionario (propiedad) para un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3eb40-119">Defines a set of dictionary property entries for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="3eb40-120">Nota</span><span class="sxs-lookup"><span data-stu-id="3eb40-120">XmlData</span></span>](xmldata.md) <br/> |<span data-ttu-id="3eb40-121">Contiene contenido de propiedad de datos XML para un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3eb40-121">Contains XML data property content for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="3eb40-122">BinaryData</span><span class="sxs-lookup"><span data-stu-id="3eb40-122">BinaryData</span></span>](binarydata.md) <br/> |<span data-ttu-id="3eb40-123">Contiene el contenido de la propiedad de datos binarios para un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3eb40-123">Contains binary data property content for a user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3eb40-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3eb40-124">Parent elements</span></span>

|<span data-ttu-id="3eb40-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="3eb40-125">**Element**</span></span>|<span data-ttu-id="3eb40-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3eb40-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3eb40-127">CreateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="3eb40-127">CreateUserConfiguration</span></span>](createuserconfiguration.md) <br/> |<span data-ttu-id="3eb40-128">Representa una solicitud para crear un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3eb40-128">Represents a request to create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="3eb40-129">GetUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3eb40-129">GetUserConfigurationResponseMessage</span></span>](getuserconfigurationresponsemessage.md) <br/> |<span data-ttu-id="3eb40-130">Representa una respuesta que devuelve un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3eb40-130">Represents a response that returns a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="3eb40-131">UpdateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="3eb40-131">UpdateUserConfiguration</span></span>](updateuserconfiguration.md) <br/> |<span data-ttu-id="3eb40-132">Representa una solicitud para actualizar un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3eb40-132">Represents a request to update a user configuration object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3eb40-133">Notas</span><span class="sxs-lookup"><span data-stu-id="3eb40-133">Remarks</span></span>

<span data-ttu-id="3eb40-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3eb40-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3eb40-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3eb40-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3eb40-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3eb40-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3eb40-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3eb40-137">Schema Name</span></span>  <br/> |<span data-ttu-id="3eb40-138">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3eb40-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3eb40-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3eb40-139">Validation File</span></span>  <br/> |<span data-ttu-id="3eb40-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3eb40-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3eb40-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3eb40-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="3eb40-142">False</span><span class="sxs-lookup"><span data-stu-id="3eb40-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3eb40-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="3eb40-143">See also</span></span>



- [<span data-ttu-id="3eb40-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3eb40-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

