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
description: El elemento GetUserOofSettingsResponse contiene el mensaje de respuesta y la configuración de fuera de oficina (OOF) para un usuario.
ms.openlocfilehash: dc63b6d54471973ce5961a5a5ad6a23f6521fc0e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835693"
---
# <a name="getuseroofsettingsresponse"></a><span data-ttu-id="dcb6e-103">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="dcb6e-103">GetUserOofSettingsResponse</span></span>

<span data-ttu-id="dcb6e-104">El elemento **GetUserOofSettingsResponse** contiene el mensaje de respuesta y la configuración de fuera de oficina (OOF) para un usuario.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-104">The **GetUserOofSettingsResponse** element contains the response message and the Out of Office (OOF) settings for a user.</span></span> 
  
```xml
<GetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
   <OofSettings>...</OofSettings>
   <AllowExternalOof>...</AllowExternalOof>
</GetUserOofSettingsResponse>
```

 <span data-ttu-id="dcb6e-105">**GetUserOofSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="dcb6e-105">**GetUserOofSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dcb6e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dcb6e-106">Attributes and elements</span></span>

<span data-ttu-id="dcb6e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dcb6e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dcb6e-108">Attributes</span></span>

<span data-ttu-id="dcb6e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dcb6e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dcb6e-110">Child elements</span></span>

|<span data-ttu-id="dcb6e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dcb6e-111">**Element**</span></span>|<span data-ttu-id="dcb6e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dcb6e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dcb6e-113">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="dcb6e-113">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="dcb6e-114">Proporciona información descriptiva sobre el estado de respuesta.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-114">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="dcb6e-115">OofSettings</span><span class="sxs-lookup"><span data-stu-id="dcb6e-115">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="dcb6e-116">Contiene la configuración de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-116">Contains the OOF settings.</span></span>  <br/> |
|[<span data-ttu-id="dcb6e-117">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="dcb6e-117">AllowExternalOof</span></span>](allowexternaloof.md) <br/> |<span data-ttu-id="dcb6e-118">Contiene un valor que identifica a la que se envían los mensajes externos de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-118">Contains a value that identifies to whom external OOF messages are sent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dcb6e-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dcb6e-119">Parent elements</span></span>

<span data-ttu-id="dcb6e-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dcb6e-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcb6e-121">Remarks</span></span>

<span data-ttu-id="dcb6e-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dcb6e-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dcb6e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcb6e-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dcb6e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dcb6e-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dcb6e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="dcb6e-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="dcb6e-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dcb6e-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dcb6e-127">Validation File</span></span>  <br/> |<span data-ttu-id="dcb6e-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dcb6e-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dcb6e-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dcb6e-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="dcb6e-130">False</span><span class="sxs-lookup"><span data-stu-id="dcb6e-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dcb6e-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="dcb6e-131">See also</span></span>



[<span data-ttu-id="dcb6e-132">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="dcb6e-132">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="dcb6e-133">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="dcb6e-133">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

