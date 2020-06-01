---
title: SenderSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SenderSmtpAddress
api_type:
- schema
ms.assetid: e39c7df7-4bfa-455f-b4bb-1f1d05398eec
description: El elemento SenderSmtpAddress representa la dirección de correo electrónico SMTP correspondiente al buzón de correo que contiene la carpeta que se va a compartir.
ms.openlocfilehash: 73047dcecfbccb55d74e373891c3154bc7baeeba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464899"
---
# <a name="sendersmtpaddress"></a><span data-ttu-id="3a5c3-103">SenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="3a5c3-103">SenderSmtpAddress</span></span>

<span data-ttu-id="3a5c3-104">El elemento **SenderSmtpAddress** representa la dirección de correo electrónico SMTP correspondiente al buzón de correo que contiene la carpeta que se va a compartir.</span><span class="sxs-lookup"><span data-stu-id="3a5c3-104">The **SenderSmtpAddress** element represents the SMTP e-mail address corresponding to the mailbox that contains the folder that will be shared.</span></span> 
  
```xml
<SenderSmtpAddress/>
```

 <span data-ttu-id="3a5c3-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="3a5c3-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a5c3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3a5c3-106">Attributes and elements</span></span>

<span data-ttu-id="3a5c3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3a5c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a5c3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a5c3-108">Attributes</span></span>

<span data-ttu-id="3a5c3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3a5c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a5c3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3a5c3-110">Child elements</span></span>

<span data-ttu-id="3a5c3-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3a5c3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3a5c3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3a5c3-112">Parent elements</span></span>

|<span data-ttu-id="3a5c3-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3a5c3-113">**Element**</span></span>|<span data-ttu-id="3a5c3-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a5c3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a5c3-115">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="3a5c3-115">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="3a5c3-116">Define una solicitud para obtener un token de autenticación opaco que identifique la invitación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="3a5c3-116">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3a5c3-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3a5c3-117">Text value</span></span>

<span data-ttu-id="3a5c3-118">Se necesita un valor de texto que represente una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="3a5c3-118">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3a5c3-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a5c3-119">Remarks</span></span>

<span data-ttu-id="3a5c3-120">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="3a5c3-120">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a5c3-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3a5c3-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a5c3-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a5c3-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3a5c3-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3a5c3-123">Schema Name</span></span>  <br/> |<span data-ttu-id="3a5c3-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3a5c3-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3a5c3-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3a5c3-125">Validation File</span></span>  <br/> |<span data-ttu-id="3a5c3-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3a5c3-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3a5c3-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3a5c3-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a5c3-128">Falso</span><span class="sxs-lookup"><span data-stu-id="3a5c3-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a5c3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a5c3-129">See also</span></span>



[<span data-ttu-id="3a5c3-130">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="3a5c3-130">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="3a5c3-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3a5c3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

