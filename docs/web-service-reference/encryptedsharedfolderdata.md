---
title: EncryptedSharedFolderData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EncryptedSharedFolderData
api_type:
- schema
ms.assetid: c1d4ca18-c5ce-41ff-bab4-f75e358c8b9f
description: El elemento EncryptedSharedFolderData contiene los datos cifrados que un cliente puede usar para autorizar el uso compartido de sus datos de contacto o calendario con otros clientes.
ms.openlocfilehash: 52e91eaf1ded31602b11e50c1b62159f72c101cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530666"
---
# <a name="encryptedsharedfolderdata"></a><span data-ttu-id="cfacc-103">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="cfacc-103">EncryptedSharedFolderData</span></span>

<span data-ttu-id="cfacc-104">El elemento **EncryptedSharedFolderData** contiene los datos cifrados que un cliente puede usar para autorizar el uso compartido de sus datos de contacto o calendario con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="cfacc-104">The **EncryptedSharedFolderData** element contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span> 
  
```xml
<EncryptedSharedFolderData>   <Token/>   <Data/></EncryptedSharedFolderData>
```

 <span data-ttu-id="cfacc-105">**EncryptedSharedFolderDataType**</span><span class="sxs-lookup"><span data-stu-id="cfacc-105">**EncryptedSharedFolderDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cfacc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cfacc-106">Attributes and elements</span></span>

<span data-ttu-id="cfacc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cfacc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cfacc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cfacc-108">Attributes</span></span>

<span data-ttu-id="cfacc-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cfacc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cfacc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cfacc-110">Child elements</span></span>

|<span data-ttu-id="cfacc-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cfacc-111">**Element**</span></span>|<span data-ttu-id="cfacc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cfacc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cfacc-113">Token</span><span class="sxs-lookup"><span data-stu-id="cfacc-113">Token</span></span>](token.md) <br/> |<span data-ttu-id="cfacc-114">Contiene datos cifrados que representan el token de identificación para los datos compartidos.</span><span class="sxs-lookup"><span data-stu-id="cfacc-114">Contains encrypted data that represents the identification token for the shared data.</span></span>  <br/> |
|[<span data-ttu-id="cfacc-115">Datos</span><span class="sxs-lookup"><span data-stu-id="cfacc-115">Data</span></span>](data.md) <br/> |<span data-ttu-id="cfacc-116">Contiene datos cifrados que representan los datos compartidos.</span><span class="sxs-lookup"><span data-stu-id="cfacc-116">Contains encrypted data that represents the shared data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cfacc-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cfacc-117">Parent elements</span></span>

|<span data-ttu-id="cfacc-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cfacc-118">**Element**</span></span>|<span data-ttu-id="cfacc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cfacc-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cfacc-120">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="cfacc-120">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="cfacc-121">Representa una colección de estructuras de datos que un cliente puede usar para autorizar el uso compartido de sus datos de contacto o calendario con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="cfacc-121">Represents a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfacc-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cfacc-122">Remarks</span></span>

<span data-ttu-id="cfacc-123">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="cfacc-123">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cfacc-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cfacc-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cfacc-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfacc-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cfacc-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cfacc-126">Schema Name</span></span>  <br/> |<span data-ttu-id="cfacc-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cfacc-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="cfacc-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cfacc-128">Validation File</span></span>  <br/> |<span data-ttu-id="cfacc-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cfacc-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cfacc-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cfacc-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="cfacc-131">Falso</span><span class="sxs-lookup"><span data-stu-id="cfacc-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cfacc-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfacc-132">See also</span></span>

- [<span data-ttu-id="cfacc-133">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="cfacc-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="cfacc-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cfacc-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

