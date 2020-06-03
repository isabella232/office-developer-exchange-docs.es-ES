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
description: El elemento users representa una colección de direcciones de correo electrónico de los usuarios para los que se debe recuperar la configuración.
ms.openlocfilehash: 851447a2918e365b7c5d8812a61c9d425d26ffa2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461901"
---
# <a name="users-soap"></a><span data-ttu-id="6373a-103">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6373a-103">Users (SOAP)</span></span>

<span data-ttu-id="6373a-104">El elemento **users** representa una colección de direcciones de correo electrónico de los usuarios para los que se debe recuperar la configuración.</span><span class="sxs-lookup"><span data-stu-id="6373a-104">The **Users** element represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span> 
  
```XML
<Users>
   <User/>
</Users>
```

 <span data-ttu-id="6373a-105">**Usuarios**</span><span class="sxs-lookup"><span data-stu-id="6373a-105">**Users**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6373a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6373a-106">Attributes and elements</span></span>

<span data-ttu-id="6373a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6373a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6373a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6373a-108">Attributes</span></span>

<span data-ttu-id="6373a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6373a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6373a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6373a-110">Child elements</span></span>

|<span data-ttu-id="6373a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6373a-111">**Element**</span></span>|<span data-ttu-id="6373a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6373a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6373a-113">Usuario (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6373a-113">User (SOAP)</span></span>](user-soap.md) <br/> |<span data-ttu-id="6373a-114">Representa la dirección de correo electrónico de un usuario.</span><span class="sxs-lookup"><span data-stu-id="6373a-114">Represents the e-mail address of a user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6373a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6373a-115">Parent elements</span></span>

|<span data-ttu-id="6373a-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6373a-116">**Element**</span></span>|<span data-ttu-id="6373a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6373a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6373a-118">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6373a-118">GetUserSettingsRequest (SOAP)</span></span>](getusersettingsrequest-soap.md) <br/> |<span data-ttu-id="6373a-119">Representa una solicitud para recuperar la configuración especificada de uno o más usuarios.</span><span class="sxs-lookup"><span data-stu-id="6373a-119">Represents a request to retrieve specified settings for one or more users.</span></span>  <br/> |
|[<span data-ttu-id="6373a-120">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6373a-120">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="6373a-121">Contiene las opciones de configuración solicitadas y los usuarios de destino.</span><span class="sxs-lookup"><span data-stu-id="6373a-121">Contains the requested configuration settings and the target users.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6373a-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6373a-122">Text value</span></span>

<span data-ttu-id="6373a-123">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6373a-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6373a-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6373a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6373a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6373a-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6373a-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6373a-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6373a-127">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="6373a-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6373a-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6373a-128">Validation File</span></span>  <br/> |<span data-ttu-id="6373a-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6373a-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6373a-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6373a-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6373a-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="6373a-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6373a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6373a-132">See also</span></span>



[<span data-ttu-id="6373a-133">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6373a-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

