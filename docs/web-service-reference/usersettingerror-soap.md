---
title: UserSettingError (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: abb175c5-4f38-4dcc-81e3-b511686862eb
description: El elemento UserSettingError representa un error que se devuelve como resultado de un intento de obtener una configuración de usuario.
ms.openlocfilehash: 886e0be0aa900ce3a00902c21cc115e866d0cd99
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840930"
---
# <a name="usersettingerror-soap"></a><span data-ttu-id="426b3-103">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="426b3-103">UserSettingError (SOAP)</span></span>

<span data-ttu-id="426b3-104">El elemento **UserSettingError** representa un error que se devuelve como resultado de un intento de obtener una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="426b3-104">The **UserSettingError** element represents an error that is returned as a result of an attempt to get a user setting.</span></span> 
  
```XML
<UserSettingError>
    <ErrorCode/>
    <ErrorMessage/>
    <SettingName/>
</UserSettingError>
```

 <span data-ttu-id="426b3-105">**UserSettingError**</span><span class="sxs-lookup"><span data-stu-id="426b3-105">**UserSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="426b3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="426b3-106">Attributes and elements</span></span>

<span data-ttu-id="426b3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="426b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="426b3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="426b3-108">Attributes</span></span>

<span data-ttu-id="426b3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="426b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="426b3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="426b3-110">Child elements</span></span>

|<span data-ttu-id="426b3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="426b3-111">**Element**</span></span>|<span data-ttu-id="426b3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="426b3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="426b3-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="426b3-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="426b3-114">Representa un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="426b3-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="426b3-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="426b3-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="426b3-116">Representado por un mensaje asociado a un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="426b3-116">Respresents a message associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="426b3-117">NombreDeOpción (SOAP)</span><span class="sxs-lookup"><span data-stu-id="426b3-117">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="426b3-118">Representa el nombre de una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="426b3-118">Represents the name of a user setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="426b3-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="426b3-119">Parent elements</span></span>

|<span data-ttu-id="426b3-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="426b3-120">**Element**</span></span>|<span data-ttu-id="426b3-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="426b3-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="426b3-122">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="426b3-122">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="426b3-123">Representa una colección de información sobre la configuración que no se pudo devolver.</span><span class="sxs-lookup"><span data-stu-id="426b3-123">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="426b3-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="426b3-124">Text value</span></span>

<span data-ttu-id="426b3-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="426b3-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="426b3-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="426b3-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="426b3-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="426b3-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="426b3-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="426b3-128">Schema Name</span></span>  <br/> |<span data-ttu-id="426b3-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="426b3-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="426b3-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="426b3-130">Validation File</span></span>  <br/> |<span data-ttu-id="426b3-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="426b3-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="426b3-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="426b3-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="426b3-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="426b3-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="426b3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="426b3-134">See also</span></span>



[<span data-ttu-id="426b3-135">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="426b3-135">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

