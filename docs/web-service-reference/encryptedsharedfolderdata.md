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
description: El elemento EncryptedSharedFolderData contiene los datos cifrados que un cliente puede usar para autorizar el uso compartido de su calendario o póngase en contacto con datos con otros clientes.
ms.openlocfilehash: 63966e95becaab4b3b1e54aa81f1b20a8b09dfd3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764391"
---
# <a name="encryptedsharedfolderdata"></a><span data-ttu-id="6b74b-103">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="6b74b-103">EncryptedSharedFolderData</span></span>

<span data-ttu-id="6b74b-104">El elemento **EncryptedSharedFolderData** contiene los datos cifrados que un cliente puede usar para autorizar el uso compartido de su calendario o póngase en contacto con datos con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="6b74b-104">The **EncryptedSharedFolderData** element contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span> 
  
```xml
<EncryptedSharedFolderData>   <Token/>   <Data/></EncryptedSharedFolderData>
```

 <span data-ttu-id="6b74b-105">**EncryptedSharedFolderDataType**</span><span class="sxs-lookup"><span data-stu-id="6b74b-105">**EncryptedSharedFolderDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b74b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6b74b-106">Attributes and elements</span></span>

<span data-ttu-id="6b74b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6b74b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b74b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b74b-108">Attributes</span></span>

<span data-ttu-id="6b74b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6b74b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b74b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6b74b-110">Child elements</span></span>

|<span data-ttu-id="6b74b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b74b-111">**Element**</span></span>|<span data-ttu-id="6b74b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b74b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b74b-113">Token</span><span class="sxs-lookup"><span data-stu-id="6b74b-113">Token</span></span>](token.md) <br/> |<span data-ttu-id="6b74b-114">Contiene los datos cifrados que representa el símbolo (token) de identificación para los datos compartidos.</span><span class="sxs-lookup"><span data-stu-id="6b74b-114">Contains encrypted data that represents the identification token for the shared data.</span></span>  <br/> |
|[<span data-ttu-id="6b74b-115">Datos</span><span class="sxs-lookup"><span data-stu-id="6b74b-115">Data</span></span>](data.md) <br/> |<span data-ttu-id="6b74b-116">Contiene los datos cifrados que representa los datos compartidos.</span><span class="sxs-lookup"><span data-stu-id="6b74b-116">Contains encrypted data that represents the shared data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6b74b-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6b74b-117">Parent elements</span></span>

|<span data-ttu-id="6b74b-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b74b-118">**Element**</span></span>|<span data-ttu-id="6b74b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b74b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b74b-120">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="6b74b-120">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="6b74b-121">Representa una colección de estructuras de datos que un cliente puede usar para autorizar el uso compartido de su calendario o póngase en contacto con datos con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="6b74b-121">Represents a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b74b-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b74b-122">Remarks</span></span>

<span data-ttu-id="6b74b-123">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="6b74b-123">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b74b-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6b74b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b74b-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6b74b-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6b74b-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6b74b-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6b74b-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6b74b-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="6b74b-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6b74b-128">Validation File</span></span>  <br/> |<span data-ttu-id="6b74b-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6b74b-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6b74b-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6b74b-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6b74b-131">False</span><span class="sxs-lookup"><span data-stu-id="6b74b-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b74b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b74b-132">See also</span></span>

- [<span data-ttu-id="6b74b-133">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="6b74b-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="6b74b-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6b74b-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

