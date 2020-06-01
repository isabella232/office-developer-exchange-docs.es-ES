---
title: EncryptedSharedFolderDataCollection
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EncryptedSharedFolderDataCollection
api_type:
- schema
ms.assetid: 25c6ae87-bbb9-4dd5-a85a-d669fcea137f
description: El elemento EncryptedSharedFolderDataCollection contiene una colección de estructuras de datos que un cliente puede usar para autorizar el uso compartido de sus datos de contacto o calendario con otros clientes.
ms.openlocfilehash: e8ed9221952892abda7b4eac62b16cdc4976c6e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461271"
---
# <a name="encryptedsharedfolderdatacollection"></a><span data-ttu-id="bdef5-103">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="bdef5-103">EncryptedSharedFolderDataCollection</span></span>

<span data-ttu-id="bdef5-104">El elemento **EncryptedSharedFolderDataCollection** contiene una colección de estructuras de datos que un cliente puede usar para autorizar el uso compartido de sus datos de contacto o calendario con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="bdef5-104">The **EncryptedSharedFolderDataCollection** element contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span> 
  
```xml
<EncryptedSharedFolderDataCollection>   <EncryptedSharedFolderData/></EncryptedSharedFolderDataCollection>
```

 <span data-ttu-id="bdef5-105">**ArrayOfEncryptedSharedFolderDataType**</span><span class="sxs-lookup"><span data-stu-id="bdef5-105">**ArrayOfEncryptedSharedFolderDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bdef5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bdef5-106">Attributes and elements</span></span>

<span data-ttu-id="bdef5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bdef5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bdef5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bdef5-108">Attributes</span></span>

<span data-ttu-id="bdef5-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bdef5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bdef5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bdef5-110">Child elements</span></span>

|<span data-ttu-id="bdef5-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bdef5-111">**Element**</span></span>|<span data-ttu-id="bdef5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bdef5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdef5-113">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="bdef5-113">EncryptedSharedFolderData</span></span>](encryptedsharedfolderdata.md) <br/> |<span data-ttu-id="bdef5-114">Contiene los datos cifrados que un cliente puede usar para autorizar el uso compartido de sus datos de contacto o calendario con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="bdef5-114">Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bdef5-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bdef5-115">Parent elements</span></span>

|<span data-ttu-id="bdef5-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bdef5-116">**Element**</span></span>|<span data-ttu-id="bdef5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bdef5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdef5-118">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="bdef5-118">GetSharingMetadataResponse</span></span>](getsharingmetadataresponse.md) <br/> |<span data-ttu-id="bdef5-119">Define una respuesta a una solicitud de [operación de GetSharingMetadata](getsharingmetadata-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bdef5-119">Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="bdef5-120">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bdef5-120">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md) <br/> |<span data-ttu-id="bdef5-121">Contiene el estado y el resultado de una sola solicitud de [operación GetSharingMetadata](getsharingmetadata-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bdef5-121">Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdef5-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bdef5-122">Remarks</span></span>

<span data-ttu-id="bdef5-123">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="bdef5-123">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bdef5-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bdef5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdef5-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="bdef5-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bdef5-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bdef5-126">Schema Name</span></span>  <br/> |<span data-ttu-id="bdef5-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="bdef5-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bdef5-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bdef5-128">Validation File</span></span>  <br/> |<span data-ttu-id="bdef5-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bdef5-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bdef5-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bdef5-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="bdef5-131">Falso</span><span class="sxs-lookup"><span data-stu-id="bdef5-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bdef5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdef5-132">See also</span></span>

- [<span data-ttu-id="bdef5-133">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="bdef5-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="bdef5-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bdef5-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

