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
description: El elemento GetUserSettingsRequest representa una solicitud para recuperar la configuración especificada de uno o más usuarios.
ms.openlocfilehash: 353facb5d0bbf922a23b33cbaf6f9d2e7d82bd6b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530165"
---
# <a name="getusersettingsrequest-soap"></a><span data-ttu-id="ba0c2-103">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ba0c2-103">GetUserSettingsRequest (SOAP)</span></span>

<span data-ttu-id="ba0c2-104">El elemento **GetUserSettingsRequest** representa una solicitud para recuperar la configuración especificada de uno o más usuarios.</span><span class="sxs-lookup"><span data-stu-id="ba0c2-104">The **GetUserSettingsRequest** element represents a request to retrieve specified settings for one or more users.</span></span> 
  
```XML
<GetUserSettingsRequest>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetUserSettingsRequest>
```

 <span data-ttu-id="ba0c2-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="ba0c2-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba0c2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ba0c2-106">Attributes and elements</span></span>

<span data-ttu-id="ba0c2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ba0c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba0c2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba0c2-108">Attributes</span></span>

<span data-ttu-id="ba0c2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ba0c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba0c2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba0c2-110">Child elements</span></span>

|<span data-ttu-id="ba0c2-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ba0c2-111">**Element**</span></span>|<span data-ttu-id="ba0c2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba0c2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba0c2-113">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ba0c2-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="ba0c2-114">Representa una colección de direcciones de correo electrónico de los usuarios para los que se debe recuperar la configuración.</span><span class="sxs-lookup"><span data-stu-id="ba0c2-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="ba0c2-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ba0c2-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="ba0c2-116">Contiene los nombres de las opciones de configuración solicitadas.</span><span class="sxs-lookup"><span data-stu-id="ba0c2-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="ba0c2-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ba0c2-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="ba0c2-118">Especifica la versión de servidor específica que el proveedor desea usar.</span><span class="sxs-lookup"><span data-stu-id="ba0c2-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba0c2-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba0c2-119">Parent elements</span></span>

<span data-ttu-id="ba0c2-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ba0c2-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ba0c2-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ba0c2-121">Text value</span></span>

<span data-ttu-id="ba0c2-122">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ba0c2-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba0c2-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba0c2-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba0c2-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba0c2-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ba0c2-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ba0c2-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ba0c2-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="ba0c2-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ba0c2-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ba0c2-127">Validation File</span></span>  <br/> |<span data-ttu-id="ba0c2-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ba0c2-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ba0c2-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba0c2-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba0c2-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ba0c2-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba0c2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba0c2-131">See also</span></span>



[<span data-ttu-id="ba0c2-132">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ba0c2-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

