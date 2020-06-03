---
title: GetSharingMetadata
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: b609ee26-6d28-4559-81b6-b8e8d4759a23
description: El elemento GetSharingMetadata define una solicitud para obtener un token de autenticación opaco que identifique la invitación para uso compartido. Este elemento es el elemento base para la operación GetSharingMetadata.
ms.openlocfilehash: 406908e566d6d4249003b1a19a9ce79b8b328c4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530849"
---
# <a name="getsharingmetadata"></a><span data-ttu-id="018a0-104">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="018a0-104">GetSharingMetadata</span></span>

<span data-ttu-id="018a0-105">El elemento **GetSharingMetadata** define una solicitud para obtener un token de autenticación opaco que identifique la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="018a0-105">The **GetSharingMetadata** element defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span> <span data-ttu-id="018a0-106">Este elemento es el elemento base para la [operación GetSharingMetadata](getsharingmetadata-operation.md).</span><span class="sxs-lookup"><span data-stu-id="018a0-106">This element is the base element for the [GetSharingMetadata operation](getsharingmetadata-operation.md).</span></span>
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 <span data-ttu-id="018a0-107">**GetSharingMetadataType**</span><span class="sxs-lookup"><span data-stu-id="018a0-107">**GetSharingMetadataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="018a0-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="018a0-108">Attributes and elements</span></span>

<span data-ttu-id="018a0-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="018a0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="018a0-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="018a0-110">Attributes</span></span>

<span data-ttu-id="018a0-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="018a0-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="018a0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="018a0-112">Child elements</span></span>

|<span data-ttu-id="018a0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="018a0-113">**Element**</span></span>|<span data-ttu-id="018a0-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="018a0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="018a0-115">IdOfFolderToShare</span><span class="sxs-lookup"><span data-stu-id="018a0-115">IdOfFolderToShare</span></span>](idoffoldertoshare.md) <br/> |<span data-ttu-id="018a0-116">Representa el identificador de la carpeta en el servidor que se va a compartir.</span><span class="sxs-lookup"><span data-stu-id="018a0-116">Represents the identifier of the folder on the server that will be shared.</span></span> <span data-ttu-id="018a0-117">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="018a0-117">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="018a0-118">SenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="018a0-118">SenderSmtpAddress</span></span>](sendersmtpaddress.md) <br/> |<span data-ttu-id="018a0-119">Representa la dirección de correo electrónico SMTP que corresponde al buzón de correo que contiene la carpeta identificada por el elemento [IdOfFolderToShare](idoffoldertoshare.md) .</span><span class="sxs-lookup"><span data-stu-id="018a0-119">Represents the SMTP email address that corresponds to the mailbox that contains the folder that is identified by the [IdOfFolderToShare](idoffoldertoshare.md) element.</span></span> <span data-ttu-id="018a0-120">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="018a0-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="018a0-121">Recipients (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="018a0-121">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="018a0-122">Representa las direcciones de correo electrónico SMTP de una o más entidades a las que se va a conceder acceso a los datos de la carpeta identificada por el elemento [IdOfFolderToShare](idoffoldertoshare.md) .</span><span class="sxs-lookup"><span data-stu-id="018a0-122">Represents the SMTP email addresses of one or more entities that will be granted access to the data in the folder that is identified by the [IdOfFolderToShare](idoffoldertoshare.md) element.</span></span> <span data-ttu-id="018a0-123">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="018a0-123">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="018a0-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="018a0-124">Parent elements</span></span>

<span data-ttu-id="018a0-125">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="018a0-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="018a0-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="018a0-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="018a0-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="018a0-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="018a0-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="018a0-128">Schema Name</span></span>  <br/> |<span data-ttu-id="018a0-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="018a0-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="018a0-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="018a0-130">Validation File</span></span>  <br/> |<span data-ttu-id="018a0-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="018a0-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="018a0-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="018a0-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="018a0-133">Falso</span><span class="sxs-lookup"><span data-stu-id="018a0-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="018a0-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="018a0-134">See also</span></span>



[<span data-ttu-id="018a0-135">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="018a0-135">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="018a0-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="018a0-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

