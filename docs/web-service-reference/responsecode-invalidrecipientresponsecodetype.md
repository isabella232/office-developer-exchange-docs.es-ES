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
description: El elemento ResponseCode proporciona información sobre por qué el destinatario no es válido.
ms.openlocfilehash: d78de64de7725007ec51a55dad13d1cc892a25e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529724"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a><span data-ttu-id="fc0d1-103">ResponseCode (InvalidRecipientResponseCodeType)</span><span class="sxs-lookup"><span data-stu-id="fc0d1-103">ResponseCode (InvalidRecipientResponseCodeType)</span></span>

<span data-ttu-id="fc0d1-104">El elemento **ResponseCode** proporciona información sobre por qué el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-104">The **ResponseCode** element provides information about why the recipient is invalid.</span></span> 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 <span data-ttu-id="fc0d1-105">**InvalidRecipientResponseCodeType**</span><span class="sxs-lookup"><span data-stu-id="fc0d1-105">**InvalidRecipientResponseCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fc0d1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fc0d1-106">Attributes and elements</span></span>

<span data-ttu-id="fc0d1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc0d1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc0d1-108">Attributes</span></span>

<span data-ttu-id="fc0d1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc0d1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fc0d1-110">Child elements</span></span>

<span data-ttu-id="fc0d1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fc0d1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fc0d1-112">Parent elements</span></span>

|<span data-ttu-id="fc0d1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fc0d1-113">**Element**</span></span>|<span data-ttu-id="fc0d1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc0d1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc0d1-115">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="fc0d1-115">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="fc0d1-116">Contiene la dirección SMTP del destinatario no válido e información sobre por qué el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-116">Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fc0d1-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fc0d1-117">Text value</span></span>

<span data-ttu-id="fc0d1-118">En la siguiente tabla se enumeran los valores posibles para el elemento **ResponseCode** .</span><span class="sxs-lookup"><span data-stu-id="fc0d1-118">The following table lists the possible values for the **ResponseCode** element.</span></span> 
  
|<span data-ttu-id="fc0d1-119">**Código**</span><span class="sxs-lookup"><span data-stu-id="fc0d1-119">**Code**</span></span>|<span data-ttu-id="fc0d1-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc0d1-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc0d1-121">OtherError</span><span class="sxs-lookup"><span data-stu-id="fc0d1-121">OtherError</span></span>  <br/> |<span data-ttu-id="fc0d1-122">Indica que el error no está especificado por otro código de respuesta de error.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-122">Indicates that the error is not specified by another error response code.</span></span>  <br/> |
|<span data-ttu-id="fc0d1-123">RecipientOrganizationNotFederated</span><span class="sxs-lookup"><span data-stu-id="fc0d1-123">RecipientOrganizationNotFederated</span></span>  <br/> |<span data-ttu-id="fc0d1-124">Indica que una relación de uso compartido no está disponible en la organización especificada en la dirección de correo electrónico SMTP del destinatario.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-124">Indicates that a sharing relationship is not available with the organization specified in the recipient's SMTP e-mail address.</span></span>  <br/> |
|<span data-ttu-id="fc0d1-125">CannotObtainTokenFromSTS</span><span class="sxs-lookup"><span data-stu-id="fc0d1-125">CannotObtainTokenFromSTS</span></span>  <br/> |<span data-ttu-id="fc0d1-126">Indica que hubo un problema al obtener un token de seguridad del servidor de tokens.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-126">Indicates that there was a problem obtaining a security token from the token server.</span></span>  <br/> |
|<span data-ttu-id="fc0d1-127">SystemPolicyBlocksSharingWithThisRecipient</span><span class="sxs-lookup"><span data-stu-id="fc0d1-127">SystemPolicyBlocksSharingWithThisRecipient</span></span>  <br/> |<span data-ttu-id="fc0d1-128">Indica que el administrador del sistema ha establecido una directiva del sistema que bloquea el uso compartido con el destinatario especificado.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-128">Indicates that the system administrator has set a system policy that blocks sharing with the specified recipient.</span></span>  <br/> |
|<span data-ttu-id="fc0d1-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="fc0d1-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span></span>  <br/> |<span data-ttu-id="fc0d1-130">Indica que el servicio de token seguro que usa el destinatario especificado es desconocido.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-130">Indicates that the secure token service that is used by the specified recipient is unknown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc0d1-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc0d1-131">Remarks</span></span>

<span data-ttu-id="fc0d1-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fc0d1-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc0d1-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fc0d1-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc0d1-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc0d1-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fc0d1-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fc0d1-135">Schema Name</span></span>  <br/> |<span data-ttu-id="fc0d1-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fc0d1-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="fc0d1-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fc0d1-137">Validation File</span></span>  <br/> |<span data-ttu-id="fc0d1-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fc0d1-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fc0d1-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fc0d1-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="fc0d1-140">Falso</span><span class="sxs-lookup"><span data-stu-id="fc0d1-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc0d1-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc0d1-141">See also</span></span>



[<span data-ttu-id="fc0d1-142">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="fc0d1-142">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="fc0d1-143">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fc0d1-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

