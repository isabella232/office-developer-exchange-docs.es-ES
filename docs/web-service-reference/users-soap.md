---
title: Usuarios (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4e051617-4eea-47d0-871a-ea1f17a0f711
description: El elemento de los usuarios representa una colección de direcciones de correo electrónico de los usuarios para el que se debe recuperar la configuración.
ms.openlocfilehash: d7655f0020a315dcb32adbbc58610ca0e630c1fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840928"
---
# <a name="users-soap"></a><span data-ttu-id="75619-103">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="75619-103">Users (SOAP)</span></span>

<span data-ttu-id="75619-104">El elemento de **los usuarios** representa una colección de direcciones de correo electrónico de los usuarios para el que se debe recuperar la configuración.</span><span class="sxs-lookup"><span data-stu-id="75619-104">The **Users** element represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span> 
  
```XML
<Users>
   <User/>
</Users>
```

 <span data-ttu-id="75619-105">**Usuarios**</span><span class="sxs-lookup"><span data-stu-id="75619-105">**Users**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75619-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="75619-106">Attributes and elements</span></span>

<span data-ttu-id="75619-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="75619-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75619-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="75619-108">Attributes</span></span>

<span data-ttu-id="75619-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="75619-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75619-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="75619-110">Child elements</span></span>

|<span data-ttu-id="75619-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="75619-111">**Element**</span></span>|<span data-ttu-id="75619-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="75619-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75619-113">Usuario (SOAP)</span><span class="sxs-lookup"><span data-stu-id="75619-113">User (SOAP)</span></span>](user-soap.md) <br/> |<span data-ttu-id="75619-114">Representa la dirección de correo electrónico de un usuario.</span><span class="sxs-lookup"><span data-stu-id="75619-114">Represents the e-mail address of a user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="75619-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="75619-115">Parent elements</span></span>

|<span data-ttu-id="75619-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="75619-116">**Element**</span></span>|<span data-ttu-id="75619-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="75619-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75619-118">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="75619-118">GetUserSettingsRequest (SOAP)</span></span>](getusersettingsrequest-soap.md) <br/> |<span data-ttu-id="75619-119">Representa una solicitud para recuperar la configuración especificada para uno o varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="75619-119">Represents a request to retrieve specified settings for one or more users.</span></span>  <br/> |
|[<span data-ttu-id="75619-120">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="75619-120">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="75619-121">Contiene las opciones de configuración solicitado y los usuarios de destino.</span><span class="sxs-lookup"><span data-stu-id="75619-121">Contains the requested configuration settings and the target users.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="75619-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="75619-122">Text value</span></span>

<span data-ttu-id="75619-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="75619-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75619-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="75619-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75619-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75619-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="75619-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="75619-126">Schema Name</span></span>  <br/> |<span data-ttu-id="75619-127">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="75619-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="75619-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="75619-128">Validation File</span></span>  <br/> |<span data-ttu-id="75619-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="75619-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="75619-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="75619-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="75619-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="75619-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75619-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="75619-132">See also</span></span>



[<span data-ttu-id="75619-133">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="75619-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

