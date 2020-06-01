---
title: GetMailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMailTips
api_type:
- schema
ms.assetid: 4a24ff79-f1ae-43a1-9ac2-49baf3eaa173
description: El elemento GetMailTips representa los destinatarios y los tipos de sugerencias de correo que se van a recuperar.
ms.openlocfilehash: 8ff71ed5d52f713e11188b07c8c93aeee7dfa44d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458638"
---
# <a name="getmailtips"></a><span data-ttu-id="a5846-103">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="a5846-103">GetMailTips</span></span>

<span data-ttu-id="a5846-104">El elemento **GetMailTips** representa los destinatarios y los tipos de sugerencias de correo que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="a5846-104">The **GetMailTips** element represents the recipients and types of mail tips to retrieve.</span></span> 
  
```XML
<GetMailTips>
   <SendingAs/>
   <Recipients/>
   <MailTipsRequested/>
</GetMailTips>
```

 <span data-ttu-id="a5846-105">**GetMailTipsType**</span><span class="sxs-lookup"><span data-stu-id="a5846-105">**GetMailTipsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a5846-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a5846-106">Attributes and elements</span></span>

<span data-ttu-id="a5846-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a5846-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5846-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a5846-108">Attributes</span></span>

<span data-ttu-id="a5846-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a5846-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a5846-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a5846-110">Child elements</span></span>

|<span data-ttu-id="a5846-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a5846-111">**Element**</span></span>|<span data-ttu-id="a5846-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5846-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5846-113">Envíoas</span><span class="sxs-lookup"><span data-stu-id="a5846-113">SendingAs</span></span>](sendingas.md) <br/> |<span data-ttu-id="a5846-114">Contiene una dirección de correo electrónico que el usuario intenta enviar como.</span><span class="sxs-lookup"><span data-stu-id="a5846-114">Contains an e-mail address that a user is trying to send as.</span></span>  <br/> |
|[<span data-ttu-id="a5846-115">Recipients (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="a5846-115">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md) <br/> |<span data-ttu-id="a5846-116">Contiene una lista de destinatarios para buscar sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="a5846-116">Contains a list of recipients to check for mail tips.</span></span>  <br/> |
|[<span data-ttu-id="a5846-117">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="a5846-117">MailTipsRequested</span></span>](mailtipsrequested.md) <br/> |<span data-ttu-id="a5846-118">Contiene los tipos de sugerencias de correo solicitados desde el servicio.</span><span class="sxs-lookup"><span data-stu-id="a5846-118">Contains the types of mail tips requested from the service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a5846-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a5846-119">Parent elements</span></span>

<span data-ttu-id="a5846-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a5846-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a5846-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a5846-121">Text value</span></span>

<span data-ttu-id="a5846-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a5846-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5846-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5846-123">Remarks</span></span>

<span data-ttu-id="a5846-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a5846-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5846-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a5846-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5846-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5846-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a5846-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a5846-127">Schema Name</span></span>  <br/> |<span data-ttu-id="a5846-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a5846-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a5846-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a5846-129">Validation File</span></span>  <br/> |<span data-ttu-id="a5846-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a5846-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a5846-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a5846-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="a5846-132">Falso</span><span class="sxs-lookup"><span data-stu-id="a5846-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5846-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5846-133">See also</span></span>



- [<span data-ttu-id="a5846-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a5846-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

