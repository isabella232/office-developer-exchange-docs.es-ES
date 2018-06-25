---
title: ResponseCode (InvalidRecipientResponseCodeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 582e9caa-d2bc-4be1-a460-739294f9ef18
description: El elemento ResponseCode proporciona información acerca de por qué el destinatario no es válido.
ms.openlocfilehash: 3bff99dd1ac6603ce31d5ceb074e73ef48190bb2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837186"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a><span data-ttu-id="8428a-103">ResponseCode (InvalidRecipientResponseCodeType)</span><span class="sxs-lookup"><span data-stu-id="8428a-103">ResponseCode (InvalidRecipientResponseCodeType)</span></span>

<span data-ttu-id="8428a-104">El elemento **ResponseCode** proporciona información acerca de por qué el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="8428a-104">The **ResponseCode** element provides information about why the recipient is invalid.</span></span> 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 <span data-ttu-id="8428a-105">**InvalidRecipientResponseCodeType**</span><span class="sxs-lookup"><span data-stu-id="8428a-105">**InvalidRecipientResponseCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8428a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8428a-106">Attributes and elements</span></span>

<span data-ttu-id="8428a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8428a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8428a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8428a-108">Attributes</span></span>

<span data-ttu-id="8428a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8428a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8428a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8428a-110">Child elements</span></span>

<span data-ttu-id="8428a-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8428a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8428a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8428a-112">Parent elements</span></span>

|<span data-ttu-id="8428a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8428a-113">**Element**</span></span>|<span data-ttu-id="8428a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8428a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8428a-115">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="8428a-115">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="8428a-116">Contiene la dirección SMTP del destinatario no válido y la información acerca de por qué el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="8428a-116">Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8428a-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8428a-117">Text value</span></span>

<span data-ttu-id="8428a-118">En la siguiente tabla se enumera los valores posibles para el elemento **ResponseCode** .</span><span class="sxs-lookup"><span data-stu-id="8428a-118">The following table lists the possible values for the **ResponseCode** element.</span></span> 
  
|<span data-ttu-id="8428a-119">**Código**</span><span class="sxs-lookup"><span data-stu-id="8428a-119">**Code**</span></span>|<span data-ttu-id="8428a-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8428a-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8428a-121">OtherError</span><span class="sxs-lookup"><span data-stu-id="8428a-121">OtherError</span></span>  <br/> |<span data-ttu-id="8428a-122">Indica que el error no se especifica por otro código de respuesta de error.</span><span class="sxs-lookup"><span data-stu-id="8428a-122">Indicates that the error is not specified by another error response code.</span></span>  <br/> |
|<span data-ttu-id="8428a-123">RecipientOrganizationNotFederated</span><span class="sxs-lookup"><span data-stu-id="8428a-123">RecipientOrganizationNotFederated</span></span>  <br/> |<span data-ttu-id="8428a-124">Indica que una relación de uso compartida no está disponible con la organización especificada en la dirección de correo electrónico SMTP del destinatario.</span><span class="sxs-lookup"><span data-stu-id="8428a-124">Indicates that a sharing relationship is not available with the organization specified in the recipient's SMTP e-mail address.</span></span>  <br/> |
|<span data-ttu-id="8428a-125">CannotObtainTokenFromSTS</span><span class="sxs-lookup"><span data-stu-id="8428a-125">CannotObtainTokenFromSTS</span></span>  <br/> |<span data-ttu-id="8428a-126">Indica que se ha producido un problema al obtener un token de seguridad desde el servidor de token.</span><span class="sxs-lookup"><span data-stu-id="8428a-126">Indicates that there was a problem obtaining a security token from the token server.</span></span>  <br/> |
|<span data-ttu-id="8428a-127">SystemPolicyBlocksSharingWithThisRecipient</span><span class="sxs-lookup"><span data-stu-id="8428a-127">SystemPolicyBlocksSharingWithThisRecipient</span></span>  <br/> |<span data-ttu-id="8428a-128">Indica que el administrador del sistema ha establecido una directiva del sistema que bloquea el uso compartido con el destinatario especificado.</span><span class="sxs-lookup"><span data-stu-id="8428a-128">Indicates that the system administrator has set a system policy that blocks sharing with the specified recipient.</span></span>  <br/> |
|<span data-ttu-id="8428a-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="8428a-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span></span>  <br/> |<span data-ttu-id="8428a-130">Indica que el servicio de token seguro que se usa el destinatario especificado es desconocido.</span><span class="sxs-lookup"><span data-stu-id="8428a-130">Indicates that the secure token service that is used by the specified recipient is unknown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8428a-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8428a-131">Remarks</span></span>

<span data-ttu-id="8428a-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8428a-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8428a-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8428a-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8428a-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8428a-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8428a-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8428a-135">Schema Name</span></span>  <br/> |<span data-ttu-id="8428a-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8428a-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="8428a-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8428a-137">Validation File</span></span>  <br/> |<span data-ttu-id="8428a-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8428a-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8428a-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8428a-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="8428a-140">False</span><span class="sxs-lookup"><span data-stu-id="8428a-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8428a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="8428a-141">See also</span></span>



[<span data-ttu-id="8428a-142">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="8428a-142">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="8428a-143">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8428a-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

