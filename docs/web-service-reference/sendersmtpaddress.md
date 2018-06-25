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
description: El elemento SenderSmtpAddress representa la dirección de correo electrónico SMTP correspondiente para el buzón de correo que contiene la carpeta que se van a compartir.
ms.openlocfilehash: 70905dd1ae2c3df18224aceeea246b542d1338e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837334"
---
# <a name="sendersmtpaddress"></a><span data-ttu-id="0d834-103">SenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="0d834-103">SenderSmtpAddress</span></span>

<span data-ttu-id="0d834-104">El elemento **SenderSmtpAddress** representa la dirección de correo electrónico SMTP correspondiente para el buzón de correo que contiene la carpeta que se van a compartir.</span><span class="sxs-lookup"><span data-stu-id="0d834-104">The **SenderSmtpAddress** element represents the SMTP e-mail address corresponding to the mailbox that contains the folder that will be shared.</span></span> 
  
```xml
<SenderSmtpAddress/>
```

 <span data-ttu-id="0d834-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="0d834-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d834-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0d834-106">Attributes and elements</span></span>

<span data-ttu-id="0d834-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0d834-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d834-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d834-108">Attributes</span></span>

<span data-ttu-id="0d834-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d834-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d834-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d834-110">Child elements</span></span>

<span data-ttu-id="0d834-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d834-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0d834-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0d834-112">Parent elements</span></span>

|<span data-ttu-id="0d834-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d834-113">**Element**</span></span>|<span data-ttu-id="0d834-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d834-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d834-115">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="0d834-115">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="0d834-116">Define una solicitud para obtener un token de autenticación opaco que identifica la invitación para compartir.</span><span class="sxs-lookup"><span data-stu-id="0d834-116">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0d834-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0d834-117">Text value</span></span>

<span data-ttu-id="0d834-118">Se requiere un valor de texto que representa una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="0d834-118">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d834-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d834-119">Remarks</span></span>

<span data-ttu-id="0d834-120">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0d834-120">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d834-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0d834-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d834-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d834-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0d834-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0d834-123">Schema Name</span></span>  <br/> |<span data-ttu-id="0d834-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0d834-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0d834-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0d834-125">Validation File</span></span>  <br/> |<span data-ttu-id="0d834-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0d834-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0d834-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0d834-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d834-128">False</span><span class="sxs-lookup"><span data-stu-id="0d834-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d834-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d834-129">See also</span></span>



[<span data-ttu-id="0d834-130">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="0d834-130">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="0d834-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0d834-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

