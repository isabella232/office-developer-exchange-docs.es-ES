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
ms.openlocfilehash: 61603038ce93780f690d72226b1356b239d2002d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468610"
---
# <a name="usersettingerror-soap"></a><span data-ttu-id="20313-103">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20313-103">UserSettingError (SOAP)</span></span>

<span data-ttu-id="20313-104">El elemento **UserSettingError** representa un error que se devuelve como resultado de un intento de obtener una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="20313-104">The **UserSettingError** element represents an error that is returned as a result of an attempt to get a user setting.</span></span> 
  
```XML
<UserSettingError>
    <ErrorCode/>
    <ErrorMessage/>
    <SettingName/>
</UserSettingError>
```

 <span data-ttu-id="20313-105">**UserSettingError**</span><span class="sxs-lookup"><span data-stu-id="20313-105">**UserSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20313-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="20313-106">Attributes and elements</span></span>

<span data-ttu-id="20313-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="20313-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20313-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="20313-108">Attributes</span></span>

<span data-ttu-id="20313-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="20313-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20313-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="20313-110">Child elements</span></span>

|<span data-ttu-id="20313-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="20313-111">**Element**</span></span>|<span data-ttu-id="20313-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20313-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20313-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20313-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="20313-114">Representa un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="20313-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="20313-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20313-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="20313-116">Representado por un mensaje asociado con un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="20313-116">Respresents a message associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="20313-117">SettingName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20313-117">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="20313-118">Representa el nombre de una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="20313-118">Represents the name of a user setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="20313-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="20313-119">Parent elements</span></span>

|<span data-ttu-id="20313-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="20313-120">**Element**</span></span>|<span data-ttu-id="20313-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20313-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20313-122">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20313-122">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="20313-123">Representa una colección de información sobre la configuración que no se pudo devolver.</span><span class="sxs-lookup"><span data-stu-id="20313-123">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="20313-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="20313-124">Text value</span></span>

<span data-ttu-id="20313-125">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="20313-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20313-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="20313-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20313-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="20313-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="20313-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="20313-128">Schema Name</span></span>  <br/> |<span data-ttu-id="20313-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="20313-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="20313-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="20313-130">Validation File</span></span>  <br/> |<span data-ttu-id="20313-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="20313-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="20313-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="20313-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="20313-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="20313-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20313-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="20313-134">See also</span></span>



[<span data-ttu-id="20313-135">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="20313-135">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

