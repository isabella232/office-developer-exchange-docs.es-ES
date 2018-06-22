---
title: GetUserSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 832a9211-d2d5-4a49-bcb3-1dc6dc3904ed
description: El elemento GetUserSettingsRequest representa una solicitud para recuperar la configuración especificada para uno o varios usuarios.
ms.openlocfilehash: dc22570144a6947dc6e7042326c7416422680cc1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835702"
---
# <a name="getusersettingsrequest-soap"></a><span data-ttu-id="37931-103">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="37931-103">GetUserSettingsRequest (SOAP)</span></span>

<span data-ttu-id="37931-104">El elemento **GetUserSettingsRequest** representa una solicitud para recuperar la configuración especificada para uno o varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="37931-104">The **GetUserSettingsRequest** element represents a request to retrieve specified settings for one or more users.</span></span> 
  
```XML
<GetUserSettingsRequest>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetUserSettingsRequest>
```

 <span data-ttu-id="37931-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="37931-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37931-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="37931-106">Attributes and elements</span></span>

<span data-ttu-id="37931-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="37931-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37931-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="37931-108">Attributes</span></span>

<span data-ttu-id="37931-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37931-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37931-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37931-110">Child elements</span></span>

|<span data-ttu-id="37931-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="37931-111">**Element**</span></span>|<span data-ttu-id="37931-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37931-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37931-113">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="37931-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="37931-114">Representa una colección de direcciones de correo electrónico de los usuarios para el que se debe recuperar la configuración.</span><span class="sxs-lookup"><span data-stu-id="37931-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="37931-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="37931-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="37931-116">Contiene los nombres de las opciones de configuración solicitado.</span><span class="sxs-lookup"><span data-stu-id="37931-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="37931-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="37931-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="37931-118">Especifica la versión de servidor específico que le gustaría usar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="37931-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37931-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="37931-119">Parent elements</span></span>

<span data-ttu-id="37931-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37931-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="37931-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="37931-121">Text value</span></span>

<span data-ttu-id="37931-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37931-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37931-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="37931-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37931-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37931-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="37931-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="37931-125">Schema Name</span></span>  <br/> |<span data-ttu-id="37931-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="37931-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="37931-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="37931-127">Validation File</span></span>  <br/> |<span data-ttu-id="37931-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="37931-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="37931-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="37931-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="37931-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="37931-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37931-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="37931-131">See also</span></span>



[<span data-ttu-id="37931-132">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="37931-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

