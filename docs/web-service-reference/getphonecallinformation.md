---
title: GetPhoneCallInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetPhoneCallInformation
api_type:
- schema
ms.assetid: 5f4ee71c-bde0-4b0d-b426-0c24dfe67585
description: El elemento GetPhoneCallInformation especifica una solicitud para obtener información de llamada de teléfono.
ms.openlocfilehash: 2084a8b5e13b3fa03e0bf62439978bbe81d86ce9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764951"
---
# <a name="getphonecallinformation"></a><span data-ttu-id="a2d61-103">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="a2d61-103">GetPhoneCallInformation</span></span>

<span data-ttu-id="a2d61-104">El elemento **GetPhoneCallInformation** especifica una solicitud para obtener información de llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="a2d61-104">The **GetPhoneCallInformation** element specifies a request to get telephone call information.</span></span> 
  
```xml
<GetPhoneCallInformation>
   <PhoneCallId/>
</GetPhoneCallInformation>
```

 <span data-ttu-id="a2d61-105">**GetPhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="a2d61-105">**GetPhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a2d61-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a2d61-106">Attributes and elements</span></span>

<span data-ttu-id="a2d61-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a2d61-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2d61-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a2d61-108">Attributes</span></span>

<span data-ttu-id="a2d61-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a2d61-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a2d61-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a2d61-110">Child elements</span></span>

|<span data-ttu-id="a2d61-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a2d61-111">**Element**</span></span>|<span data-ttu-id="a2d61-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a2d61-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2d61-113">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="a2d61-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="a2d61-114">Especifica el identificador de una llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="a2d61-114">Specifies the identifier of a phone call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a2d61-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a2d61-115">Parent elements</span></span>

<span data-ttu-id="a2d61-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a2d61-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a2d61-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a2d61-117">Text value</span></span>

<span data-ttu-id="a2d61-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a2d61-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2d61-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a2d61-119">Remarks</span></span>

<span data-ttu-id="a2d61-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a2d61-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2d61-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a2d61-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2d61-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a2d61-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a2d61-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a2d61-123">Schema Name</span></span>  <br/> |<span data-ttu-id="a2d61-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a2d61-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a2d61-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a2d61-125">Validation File</span></span>  <br/> |<span data-ttu-id="a2d61-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a2d61-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a2d61-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a2d61-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="a2d61-128">False</span><span class="sxs-lookup"><span data-stu-id="a2d61-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2d61-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2d61-129">See also</span></span>



- [<span data-ttu-id="a2d61-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a2d61-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

