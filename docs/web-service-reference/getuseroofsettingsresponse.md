---
title: GetUserOofSettingsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserOofSettingsResponse
api_type:
- schema
ms.assetid: 011cb38b-da3c-4b1b-8836-a6b212b511f6
description: El elemento GetUserOofSettingsResponse contiene el mensaje de respuesta y la configuración de fuera de la oficina (OOF) de un usuario.
ms.openlocfilehash: f7f28c67fd36630ffb5294ab35c0fef2f467ba22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457819"
---
# <a name="getuseroofsettingsresponse"></a><span data-ttu-id="771b9-103">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="771b9-103">GetUserOofSettingsResponse</span></span>

<span data-ttu-id="771b9-104">El elemento **GetUserOofSettingsResponse** contiene el mensaje de respuesta y la configuración de fuera de la oficina (OOF) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="771b9-104">The **GetUserOofSettingsResponse** element contains the response message and the Out of Office (OOF) settings for a user.</span></span> 
  
```xml
<GetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
   <OofSettings>...</OofSettings>
   <AllowExternalOof>...</AllowExternalOof>
</GetUserOofSettingsResponse>
```

 <span data-ttu-id="771b9-105">**GetUserOofSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="771b9-105">**GetUserOofSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="771b9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="771b9-106">Attributes and elements</span></span>

<span data-ttu-id="771b9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="771b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="771b9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="771b9-108">Attributes</span></span>

<span data-ttu-id="771b9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="771b9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="771b9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="771b9-110">Child elements</span></span>

|<span data-ttu-id="771b9-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="771b9-111">**Element**</span></span>|<span data-ttu-id="771b9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="771b9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="771b9-113">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="771b9-113">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="771b9-114">Proporciona información descriptiva sobre el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="771b9-114">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="771b9-115">OofSettings</span><span class="sxs-lookup"><span data-stu-id="771b9-115">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="771b9-116">Contiene la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="771b9-116">Contains the OOF settings.</span></span>  <br/> |
|[<span data-ttu-id="771b9-117">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="771b9-117">AllowExternalOof</span></span>](allowexternaloof.md) <br/> |<span data-ttu-id="771b9-118">Contiene un valor que identifica a quién se envían los mensajes externos de OOF.</span><span class="sxs-lookup"><span data-stu-id="771b9-118">Contains a value that identifies to whom external OOF messages are sent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="771b9-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="771b9-119">Parent elements</span></span>

<span data-ttu-id="771b9-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="771b9-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="771b9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="771b9-121">Remarks</span></span>

<span data-ttu-id="771b9-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="771b9-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="771b9-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="771b9-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="771b9-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="771b9-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="771b9-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="771b9-125">Schema Name</span></span>  <br/> |<span data-ttu-id="771b9-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="771b9-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="771b9-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="771b9-127">Validation File</span></span>  <br/> |<span data-ttu-id="771b9-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="771b9-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="771b9-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="771b9-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="771b9-130">Falso</span><span class="sxs-lookup"><span data-stu-id="771b9-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="771b9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="771b9-131">See also</span></span>



[<span data-ttu-id="771b9-132">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="771b9-132">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="771b9-133">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="771b9-133">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

