---
title: SetUserOofSettingsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettingsResponse
api_type:
- schema
ms.assetid: 8aa4025b-38df-4d63-a6a5-c3b932bec26e
description: El elemento SetUserOofSettingsResponse contiene el resultado de un intento de mensaje SetUserOofSettingsRequest.
ms.openlocfilehash: ab2eaaad1b7b094baad724ec56f4c26280f1f15f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837471"
---
# <a name="setuseroofsettingsresponse"></a><span data-ttu-id="8ae7a-103">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="8ae7a-103">SetUserOofSettingsResponse</span></span>

<span data-ttu-id="8ae7a-104">El elemento **SetUserOofSettingsResponse** contiene el resultado de un intento de mensaje [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="8ae7a-104">The **SetUserOofSettingsResponse** element contains the result of a [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) message attempt.</span></span> 
  
```xml
<SetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
<SetUserOofSettingsResponse>
```

 <span data-ttu-id="8ae7a-105">**SetUserOofSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="8ae7a-105">**SetUserOofSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ae7a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8ae7a-106">Attributes and elements</span></span>

<span data-ttu-id="8ae7a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8ae7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ae7a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8ae7a-108">Attributes</span></span>

<span data-ttu-id="8ae7a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8ae7a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ae7a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8ae7a-110">Child elements</span></span>

|<span data-ttu-id="8ae7a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ae7a-111">**Element**</span></span>|<span data-ttu-id="8ae7a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ae7a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ae7a-113">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8ae7a-113">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="8ae7a-114">Proporciona información descriptiva sobre el estado de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ae7a-114">Provides descriptive information about the response status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8ae7a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8ae7a-115">Parent elements</span></span>

<span data-ttu-id="8ae7a-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8ae7a-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ae7a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ae7a-117">Remarks</span></span>

<span data-ttu-id="8ae7a-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8ae7a-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ae7a-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8ae7a-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ae7a-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8ae7a-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8ae7a-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8ae7a-121">Schema Name</span></span>  <br/> |<span data-ttu-id="8ae7a-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8ae7a-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8ae7a-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8ae7a-123">Validation File</span></span>  <br/> |<span data-ttu-id="8ae7a-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8ae7a-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8ae7a-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8ae7a-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="8ae7a-126">False</span><span class="sxs-lookup"><span data-stu-id="8ae7a-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ae7a-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="8ae7a-127">See also</span></span>



[<span data-ttu-id="8ae7a-128">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="8ae7a-128">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

