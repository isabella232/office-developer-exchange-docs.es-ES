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
description: El elemento GetPhoneCallInformation especifica una solicitud para obtener información sobre llamadas telefónicas.
ms.openlocfilehash: b835cd301b1c243e88034d1057026ef1305b9038
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530200"
---
# <a name="getphonecallinformation"></a><span data-ttu-id="66f88-103">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="66f88-103">GetPhoneCallInformation</span></span>

<span data-ttu-id="66f88-104">El elemento **GetPhoneCallInformation** especifica una solicitud para obtener información sobre llamadas telefónicas.</span><span class="sxs-lookup"><span data-stu-id="66f88-104">The **GetPhoneCallInformation** element specifies a request to get telephone call information.</span></span> 
  
```xml
<GetPhoneCallInformation>
   <PhoneCallId/>
</GetPhoneCallInformation>
```

 <span data-ttu-id="66f88-105">**GetPhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="66f88-105">**GetPhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66f88-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="66f88-106">Attributes and elements</span></span>

<span data-ttu-id="66f88-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="66f88-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66f88-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="66f88-108">Attributes</span></span>

<span data-ttu-id="66f88-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="66f88-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66f88-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="66f88-110">Child elements</span></span>

|<span data-ttu-id="66f88-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="66f88-111">**Element**</span></span>|<span data-ttu-id="66f88-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="66f88-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66f88-113">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="66f88-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="66f88-114">Especifica el identificador de una llamada telefónica.</span><span class="sxs-lookup"><span data-stu-id="66f88-114">Specifies the identifier of a phone call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="66f88-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="66f88-115">Parent elements</span></span>

<span data-ttu-id="66f88-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="66f88-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="66f88-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="66f88-117">Text value</span></span>

<span data-ttu-id="66f88-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="66f88-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66f88-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66f88-119">Remarks</span></span>

<span data-ttu-id="66f88-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="66f88-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66f88-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="66f88-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66f88-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="66f88-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="66f88-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="66f88-123">Schema Name</span></span>  <br/> |<span data-ttu-id="66f88-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="66f88-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="66f88-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="66f88-125">Validation File</span></span>  <br/> |<span data-ttu-id="66f88-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="66f88-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="66f88-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="66f88-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="66f88-128">Falso</span><span class="sxs-lookup"><span data-stu-id="66f88-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66f88-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="66f88-129">See also</span></span>



- [<span data-ttu-id="66f88-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="66f88-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

