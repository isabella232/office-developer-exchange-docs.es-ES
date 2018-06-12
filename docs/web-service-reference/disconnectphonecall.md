---
title: DisconnectPhoneCall
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DisconnectPhoneCall
api_type:
- schema
ms.assetid: f9252536-9852-4dd9-9ebc-91f5cf281171
description: El elemento DisconnectPhoneCall representa una solicitud para desconectar la llamada.
ms.openlocfilehash: 56947ea9ba56c76bb02d6a425ff43b3b846a2f60
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764195"
---
# <a name="disconnectphonecall"></a><span data-ttu-id="d8b7d-103">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="d8b7d-103">DisconnectPhoneCall</span></span>

<span data-ttu-id="d8b7d-104">El elemento **DisconnectPhoneCall** representa una solicitud para desconectar la llamada.</span><span class="sxs-lookup"><span data-stu-id="d8b7d-104">The **DisconnectPhoneCall** element represents a request to disconnect a call.</span></span> 
  
```xml
<DisconnectPhoneCall>
   <PhoneCallId/>
</DisconnectPhoneCall>
```

 <span data-ttu-id="d8b7d-105">**DisconnectPhoneCallType**</span><span class="sxs-lookup"><span data-stu-id="d8b7d-105">**DisconnectPhoneCallType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8b7d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d8b7d-106">Attributes and elements</span></span>

<span data-ttu-id="d8b7d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d8b7d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8b7d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8b7d-108">Attributes</span></span>

<span data-ttu-id="d8b7d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d8b7d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d8b7d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d8b7d-110">Child elements</span></span>

|<span data-ttu-id="d8b7d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8b7d-111">**Element**</span></span>|<span data-ttu-id="d8b7d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8b7d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8b7d-113">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="d8b7d-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="d8b7d-114">Especifica el identificador de la llamada a desconectar.</span><span class="sxs-lookup"><span data-stu-id="d8b7d-114">Specifies the identifier of the call to disconnect.</span></span> <span data-ttu-id="d8b7d-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="d8b7d-115">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d8b7d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d8b7d-116">Parent elements</span></span>

<span data-ttu-id="d8b7d-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d8b7d-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d8b7d-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d8b7d-118">Text value</span></span>

<span data-ttu-id="d8b7d-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d8b7d-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d8b7d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8b7d-120">Remarks</span></span>

<span data-ttu-id="d8b7d-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8b7d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8b7d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d8b7d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8b7d-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d8b7d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d8b7d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d8b7d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d8b7d-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d8b7d-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d8b7d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d8b7d-126">Validation File</span></span>  <br/> |<span data-ttu-id="d8b7d-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d8b7d-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d8b7d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d8b7d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d8b7d-129">False</span><span class="sxs-lookup"><span data-stu-id="d8b7d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8b7d-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="d8b7d-130">See also</span></span>

- [<span data-ttu-id="d8b7d-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d8b7d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

