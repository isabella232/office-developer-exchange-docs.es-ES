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
description: El elemento GetMailTips representa los destinatarios y los tipos de sugerencias de correo para recuperar.
ms.openlocfilehash: aad3b3d9dd578d0c92bf7d48ee8b78b58c63e23d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764901"
---
# <a name="getmailtips"></a><span data-ttu-id="42779-103">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="42779-103">GetMailTips</span></span>

<span data-ttu-id="42779-104">El elemento **GetMailTips** representa los destinatarios y los tipos de sugerencias de correo para recuperar.</span><span class="sxs-lookup"><span data-stu-id="42779-104">The **GetMailTips** element represents the recipients and types of mail tips to retrieve.</span></span> 
  
```XML
<GetMailTips>
   <SendingAs/>
   <Recipients/>
   <MailTipsRequested/>
</GetMailTips>
```

 <span data-ttu-id="42779-105">**GetMailTipsType**</span><span class="sxs-lookup"><span data-stu-id="42779-105">**GetMailTipsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="42779-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="42779-106">Attributes and elements</span></span>

<span data-ttu-id="42779-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="42779-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42779-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="42779-108">Attributes</span></span>

<span data-ttu-id="42779-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="42779-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42779-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="42779-110">Child elements</span></span>

|<span data-ttu-id="42779-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="42779-111">**Element**</span></span>|<span data-ttu-id="42779-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42779-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42779-113">SendingAs</span><span class="sxs-lookup"><span data-stu-id="42779-113">SendingAs</span></span>](sendingas.md) <br/> |<span data-ttu-id="42779-114">Contiene una dirección de correo electrónico que un usuario está intentando enviar como.</span><span class="sxs-lookup"><span data-stu-id="42779-114">Contains an e-mail address that a user is trying to send as.</span></span>  <br/> |
|[<span data-ttu-id="42779-115">Recipients (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="42779-115">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md) <br/> |<span data-ttu-id="42779-116">Contiene una lista de destinatarios para comprobar si las sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="42779-116">Contains a list of recipients to check for mail tips.</span></span>  <br/> |
|[<span data-ttu-id="42779-117">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="42779-117">MailTipsRequested</span></span>](mailtipsrequested.md) <br/> |<span data-ttu-id="42779-118">Contiene los tipos de sugerencias de correo solicitados desde el servicio.</span><span class="sxs-lookup"><span data-stu-id="42779-118">Contains the types of mail tips requested from the service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="42779-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="42779-119">Parent elements</span></span>

<span data-ttu-id="42779-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="42779-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="42779-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="42779-121">Text value</span></span>

<span data-ttu-id="42779-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="42779-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42779-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42779-123">Remarks</span></span>

<span data-ttu-id="42779-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="42779-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42779-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="42779-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42779-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="42779-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="42779-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="42779-127">Schema Name</span></span>  <br/> |<span data-ttu-id="42779-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="42779-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="42779-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="42779-129">Validation File</span></span>  <br/> |<span data-ttu-id="42779-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="42779-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="42779-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="42779-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="42779-132">False</span><span class="sxs-lookup"><span data-stu-id="42779-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42779-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="42779-133">See also</span></span>



- [<span data-ttu-id="42779-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="42779-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

