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
description: El elemento DisconnectPhoneCall representa una solicitud para desconectar una llamada.
ms.openlocfilehash: 8d64ecb9dce1d8b7efcebc70686db8fcbf867217
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529710"
---
# <a name="disconnectphonecall"></a><span data-ttu-id="37a45-103">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="37a45-103">DisconnectPhoneCall</span></span>

<span data-ttu-id="37a45-104">El elemento **DisconnectPhoneCall** representa una solicitud para desconectar una llamada.</span><span class="sxs-lookup"><span data-stu-id="37a45-104">The **DisconnectPhoneCall** element represents a request to disconnect a call.</span></span> 
  
```xml
<DisconnectPhoneCall>
   <PhoneCallId/>
</DisconnectPhoneCall>
```

 <span data-ttu-id="37a45-105">**DisconnectPhoneCallType**</span><span class="sxs-lookup"><span data-stu-id="37a45-105">**DisconnectPhoneCallType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37a45-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="37a45-106">Attributes and elements</span></span>

<span data-ttu-id="37a45-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="37a45-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37a45-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="37a45-108">Attributes</span></span>

<span data-ttu-id="37a45-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="37a45-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37a45-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37a45-110">Child elements</span></span>

|<span data-ttu-id="37a45-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="37a45-111">**Element**</span></span>|<span data-ttu-id="37a45-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37a45-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37a45-113">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="37a45-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="37a45-114">Especifica el identificador de la llamada a Disconnect.</span><span class="sxs-lookup"><span data-stu-id="37a45-114">Specifies the identifier of the call to disconnect.</span></span> <span data-ttu-id="37a45-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="37a45-115">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37a45-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="37a45-116">Parent elements</span></span>

<span data-ttu-id="37a45-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="37a45-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="37a45-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="37a45-118">Text value</span></span>

<span data-ttu-id="37a45-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37a45-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37a45-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37a45-120">Remarks</span></span>

<span data-ttu-id="37a45-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="37a45-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37a45-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="37a45-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37a45-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="37a45-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="37a45-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="37a45-124">Schema Name</span></span>  <br/> |<span data-ttu-id="37a45-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="37a45-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="37a45-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="37a45-126">Validation File</span></span>  <br/> |<span data-ttu-id="37a45-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="37a45-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="37a45-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="37a45-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="37a45-129">Falso</span><span class="sxs-lookup"><span data-stu-id="37a45-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37a45-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="37a45-130">See also</span></span>

- [<span data-ttu-id="37a45-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="37a45-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

