---
title: ProtocolConnection (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6eef2188-6194-48f1-ad7e-46104aecdf56
description: El elemento ProtocolConnection representa la conexión de protocolo del cliente web del servidor.
ms.openlocfilehash: b9df3febe36db53d7c5bf0610ba857f13aa96abc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528863"
---
# <a name="protocolconnection-soap"></a><span data-ttu-id="4a32f-103">ProtocolConnection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4a32f-103">ProtocolConnection (SOAP)</span></span>

<span data-ttu-id="4a32f-104">El elemento **ProtocolConnection** representa la conexión de protocolo del cliente web del servidor.</span><span class="sxs-lookup"><span data-stu-id="4a32f-104">The **ProtocolConnection** element represents the protocol connection of the server Web client.</span></span> 
  
```XML
<ProtocolConnection>
   <Hostname/>
   <Port/>
   <EncryptionMethod/>
</ProtocolConnection>
```

 <span data-ttu-id="4a32f-105">**ProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="4a32f-105">**ProtocolConnection**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4a32f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4a32f-106">Attributes and elements</span></span>

<span data-ttu-id="4a32f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4a32f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a32f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4a32f-108">Attributes</span></span>

<span data-ttu-id="4a32f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4a32f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4a32f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4a32f-110">Child elements</span></span>

|<span data-ttu-id="4a32f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a32f-111">**Element**</span></span>|<span data-ttu-id="4a32f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a32f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a32f-113">Nombre de host (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4a32f-113">Hostname (SOAP)</span></span>](hostname-soap.md) <br/> |<span data-ttu-id="4a32f-114">Representa la parte de nombre de host del nombre de equipo completo del equipo.</span><span class="sxs-lookup"><span data-stu-id="4a32f-114">Represents the host name portion of the full computer name of the computer.</span></span>  <br/> |
|[<span data-ttu-id="4a32f-115">Puerto (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4a32f-115">Port (SOAP)</span></span>](port-soap.md) <br/> |<span data-ttu-id="4a32f-116">Representa el número de puerto que se va a usar para el protocolo.</span><span class="sxs-lookup"><span data-stu-id="4a32f-116">Represents the port number to use for the protocol.</span></span>  <br/> |
|[<span data-ttu-id="4a32f-117">EncryptionMethod (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4a32f-117">EncryptionMethod (SOAP)</span></span>](encryptionmethod-soap.md) <br/> |<span data-ttu-id="4a32f-118">Representa el método criptográfico que se usa para los protocolos POP, IMAP y SMTP.</span><span class="sxs-lookup"><span data-stu-id="4a32f-118">Represents the cryptographic method that is used for the POP, IMAP, and SMTP protocols.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4a32f-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4a32f-119">Parent elements</span></span>

|<span data-ttu-id="4a32f-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a32f-120">**Element**</span></span>|<span data-ttu-id="4a32f-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a32f-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a32f-122">ProtocolConnections (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4a32f-122">ProtocolConnections (SOAP)</span></span>](protocolconnections-soap.md) <br/> |<span data-ttu-id="4a32f-123">Contiene cero o más conexiones de protocolo.</span><span class="sxs-lookup"><span data-stu-id="4a32f-123">Contains zero or more protocol connections.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4a32f-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4a32f-124">Text value</span></span>

<span data-ttu-id="4a32f-125">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4a32f-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a32f-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4a32f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a32f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a32f-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="4a32f-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4a32f-128">Schema Name</span></span>  <br/> |<span data-ttu-id="4a32f-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="4a32f-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="4a32f-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4a32f-130">Validation File</span></span>  <br/> |<span data-ttu-id="4a32f-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4a32f-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4a32f-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4a32f-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="4a32f-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="4a32f-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a32f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a32f-134">See also</span></span>



[<span data-ttu-id="4a32f-135">ProtocolConnectionCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4a32f-135">ProtocolConnectionCollectionSetting (SOAP)</span></span>](protocolconnectioncollectionsetting-soap.md)

