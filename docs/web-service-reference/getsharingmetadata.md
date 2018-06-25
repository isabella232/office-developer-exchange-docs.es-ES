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
description: El elemento GetSharingMetadata define una solicitud para obtener un token de autenticación opaco que identifica la invitación para compartir. Este elemento es el elemento base para la operación GetSharingMetadata.
ms.openlocfilehash: 5283d35e11350ef10ed8cc01527e787ef54be927
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835677"
---
# <a name="getsharingmetadata"></a><span data-ttu-id="61adb-104">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="61adb-104">GetSharingMetadata</span></span>

<span data-ttu-id="61adb-105">El elemento **GetSharingMetadata** define una solicitud para obtener un token de autenticación opaco que identifica la invitación para compartir.</span><span class="sxs-lookup"><span data-stu-id="61adb-105">The **GetSharingMetadata** element defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span> <span data-ttu-id="61adb-106">Este elemento es el elemento base para la [operación de GetSharingMetadata](getsharingmetadata-operation.md).</span><span class="sxs-lookup"><span data-stu-id="61adb-106">This element is the base element for the [GetSharingMetadata operation](getsharingmetadata-operation.md).</span></span>
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 <span data-ttu-id="61adb-107">**GetSharingMetadataType**</span><span class="sxs-lookup"><span data-stu-id="61adb-107">**GetSharingMetadataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61adb-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="61adb-108">Attributes and elements</span></span>

<span data-ttu-id="61adb-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="61adb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61adb-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="61adb-110">Attributes</span></span>

<span data-ttu-id="61adb-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="61adb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61adb-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61adb-112">Child elements</span></span>

|<span data-ttu-id="61adb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="61adb-113">**Element**</span></span>|<span data-ttu-id="61adb-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61adb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61adb-115">IdOfFolderToShare</span><span class="sxs-lookup"><span data-stu-id="61adb-115">IdOfFolderToShare</span></span>](idoffoldertoshare.md) <br/> |<span data-ttu-id="61adb-116">Representa el identificador de la carpeta en el servidor que se van a compartir.</span><span class="sxs-lookup"><span data-stu-id="61adb-116">Represents the identifier of the folder on the server that will be shared.</span></span> <span data-ttu-id="61adb-117">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="61adb-117">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="61adb-118">SenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="61adb-118">SenderSmtpAddress</span></span>](sendersmtpaddress.md) <br/> |<span data-ttu-id="61adb-119">Representa la dirección de correo electrónico SMTP que corresponde al buzón que contiene la carpeta que se identifica con el elemento [IdOfFolderToShare](idoffoldertoshare.md) .</span><span class="sxs-lookup"><span data-stu-id="61adb-119">Represents the SMTP email address that corresponds to the mailbox that contains the folder that is identified by the [IdOfFolderToShare](idoffoldertoshare.md) element.</span></span> <span data-ttu-id="61adb-120">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="61adb-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="61adb-121">Recipients (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="61adb-121">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="61adb-122">Representa las direcciones de correo electrónico SMTP de una o varias entidades que se concederá acceso a los datos de la carpeta que se identifica con el elemento [IdOfFolderToShare](idoffoldertoshare.md) .</span><span class="sxs-lookup"><span data-stu-id="61adb-122">Represents the SMTP email addresses of one or more entities that will be granted access to the data in the folder that is identified by the [IdOfFolderToShare](idoffoldertoshare.md) element.</span></span> <span data-ttu-id="61adb-123">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="61adb-123">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61adb-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="61adb-124">Parent elements</span></span>

<span data-ttu-id="61adb-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="61adb-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61adb-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="61adb-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61adb-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61adb-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="61adb-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="61adb-128">Schema Name</span></span>  <br/> |<span data-ttu-id="61adb-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="61adb-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="61adb-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="61adb-130">Validation File</span></span>  <br/> |<span data-ttu-id="61adb-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="61adb-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="61adb-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="61adb-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="61adb-133">False</span><span class="sxs-lookup"><span data-stu-id="61adb-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61adb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="61adb-134">See also</span></span>



[<span data-ttu-id="61adb-135">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="61adb-135">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="61adb-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="61adb-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

