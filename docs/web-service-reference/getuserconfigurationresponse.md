---
title: GetUserConfigurationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserConfigurationResponse
api_type:
- schema
ms.assetid: 5e418c91-c836-4de0-a80d-f0dad0c684d7
description: El elemento GetUserConfigurationResponse define una respuesta a una única solicitud de GetUserConfiguration.
ms.openlocfilehash: b720809a66c75dbf75f6e597a0064992b9f741e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835689"
---
# <a name="getuserconfigurationresponse"></a><span data-ttu-id="0924e-103">GetUserConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="0924e-103">GetUserConfigurationResponse</span></span>

<span data-ttu-id="0924e-104">El elemento **GetUserConfigurationResponse** define una respuesta a una única solicitud de GetUserConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0924e-104">The **GetUserConfigurationResponse** element defines a response to a single GetUserConfiguration request.</span></span> 
  
```xml
<GetUserConfigurationResponse>   <ResponseMessages/></GetUserConfigurationResponse>
```

 <span data-ttu-id="0924e-105">**GetUserConfigurationResponseType**</span><span class="sxs-lookup"><span data-stu-id="0924e-105">**GetUserConfigurationResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0924e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0924e-106">Attributes and elements</span></span>

<span data-ttu-id="0924e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0924e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0924e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0924e-108">Attributes</span></span>

<span data-ttu-id="0924e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0924e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0924e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0924e-110">Child elements</span></span>

|<span data-ttu-id="0924e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0924e-111">**Element**</span></span>|<span data-ttu-id="0924e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0924e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0924e-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0924e-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0924e-114">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0924e-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0924e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0924e-115">Parent elements</span></span>

<span data-ttu-id="0924e-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0924e-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0924e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0924e-117">Remarks</span></span>

<span data-ttu-id="0924e-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0924e-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0924e-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0924e-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0924e-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0924e-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0924e-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0924e-121">Schema Name</span></span>  <br/> |<span data-ttu-id="0924e-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0924e-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0924e-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0924e-123">Validation File</span></span>  <br/> |<span data-ttu-id="0924e-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0924e-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0924e-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0924e-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="0924e-126">False</span><span class="sxs-lookup"><span data-stu-id="0924e-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0924e-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="0924e-127">See also</span></span>



- [<span data-ttu-id="0924e-128">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0924e-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

