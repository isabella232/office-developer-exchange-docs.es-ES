---
title: EcpUrl-mt (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: El elemento EcpUrl mt especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para tener acceso a la configuración de un usuario habilitado para correo de seguimiento de mensajes de correo electrónico.
ms.openlocfilehash: 13954a4dab8e81f4ba75b3578e6ba7f67f4b8b96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764292"
---
# <a name="ecpurl-mt-pox"></a><span data-ttu-id="4db2b-103">EcpUrl-mt (POX)</span><span class="sxs-lookup"><span data-stu-id="4db2b-103">EcpUrl-mt (POX)</span></span>

<span data-ttu-id="4db2b-104">El elemento **EcpUrl mt** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de un usuario habilitado para correo de seguimiento de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4db2b-104">The **EcpUrl-mt** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="4db2b-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="4db2b-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="4db2b-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="4db2b-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="4db2b-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="4db2b-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="4db2b-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="4db2b-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="4db2b-109">EcpUrl-mt (POX)</span><span class="sxs-lookup"><span data-stu-id="4db2b-109">EcpUrl-mt (POX)</span></span>](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="4db2b-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4db2b-110">Attributes and elements</span></span>

<span data-ttu-id="4db2b-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4db2b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4db2b-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="4db2b-112">Attributes</span></span>

<span data-ttu-id="4db2b-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4db2b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4db2b-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4db2b-114">Child elements</span></span>

<span data-ttu-id="4db2b-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4db2b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4db2b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4db2b-116">Parent elements</span></span>

|<span data-ttu-id="4db2b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4db2b-117">**Element**</span></span>|<span data-ttu-id="4db2b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4db2b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4db2b-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="4db2b-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="4db2b-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4db2b-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4db2b-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4db2b-121">Text value</span></span>

<span data-ttu-id="4db2b-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración para el usuario de seguimiento de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4db2b-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email tracking settings for the user.</span></span> <span data-ttu-id="4db2b-123">El valor del elemento **EcpUrl mt** contiene parámetros contenidos en ' <' y ' >' caracteres que se sustituyen por el cliente, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4db2b-123">The value of the **EcpUrl-mt** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="4db2b-124">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="4db2b-124">**Parameter**</span></span>|<span data-ttu-id="4db2b-125">**Sustituir con**</span><span class="sxs-lookup"><span data-stu-id="4db2b-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4db2b-126">_IsOwa_</span><span class="sxs-lookup"><span data-stu-id="4db2b-126">_IsOwa_</span></span> <br/> |<span data-ttu-id="4db2b-127">n</span><span class="sxs-lookup"><span data-stu-id="4db2b-127">n</span></span>  <br/> |
| <span data-ttu-id="4db2b-128">_ID mensaje_</span><span class="sxs-lookup"><span data-stu-id="4db2b-128">_MsgID_</span></span> <br/> |<span data-ttu-id="4db2b-129">Identificador de mensaje de Internet del mensaje para su seguimiento según se especifica en el encabezado de identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4db2b-129">Internet message identifier of the message to be tracked as specified by the Message-ID header.</span></span>  <br/> |
| <span data-ttu-id="4db2b-130">_Buzones_</span><span class="sxs-lookup"><span data-stu-id="4db2b-130">_Mbx_</span></span> <br/> |<span data-ttu-id="4db2b-131">La dirección SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="4db2b-131">The SMTP address of the mailbox owner.</span></span>  <br/> |
| <span data-ttu-id="4db2b-132">_Sender_</span><span class="sxs-lookup"><span data-stu-id="4db2b-132">_Sender_</span></span> <br/> |<span data-ttu-id="4db2b-133">La dirección SMTP del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4db2b-133">The SMTP address of the message's sender.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4db2b-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4db2b-134">Remarks</span></span>

<span data-ttu-id="4db2b-135">El elemento **EcpUrl mt** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="4db2b-135">The **EcpUrl-mt** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4db2b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="4db2b-136">See also</span></span>



[<span data-ttu-id="4db2b-137">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="4db2b-137">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

