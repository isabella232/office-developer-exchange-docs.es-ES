---
title: Token
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Token
api_type:
- schema
ms.assetid: 62b700e1-88c7-41ef-b431-d7af4a8b54a7
description: El elemento token contiene datos cifrados que representan el token de identificación para los datos compartidos.
ms.openlocfilehash: c2e80082f9b4ecb96defdca8c5f0223a945661ba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458911"
---
# <a name="token"></a><span data-ttu-id="5453e-103">Token</span><span class="sxs-lookup"><span data-stu-id="5453e-103">Token</span></span>

<span data-ttu-id="5453e-104">El elemento **token** contiene datos cifrados que representan el token de identificación para los datos compartidos.</span><span class="sxs-lookup"><span data-stu-id="5453e-104">The **Token** element contains encrypted data that represents the identification token for the shared data.</span></span> 
  
```xml
<Token/>
```

 <span data-ttu-id="5453e-105">**EncryptedDataContainerType**</span><span class="sxs-lookup"><span data-stu-id="5453e-105">**EncryptedDataContainerType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5453e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5453e-106">Attributes and elements</span></span>

<span data-ttu-id="5453e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5453e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5453e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5453e-108">Attributes</span></span>

<span data-ttu-id="5453e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5453e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5453e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5453e-110">Child elements</span></span>

<span data-ttu-id="5453e-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5453e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5453e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5453e-112">Parent elements</span></span>

|<span data-ttu-id="5453e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5453e-113">**Element**</span></span>|<span data-ttu-id="5453e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5453e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5453e-115">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="5453e-115">EncryptedSharedFolderData</span></span>](encryptedsharedfolderdata.md) <br/> |<span data-ttu-id="5453e-116">Contiene los datos cifrados que un cliente puede usar para autorizar el uso compartido de sus datos de contacto o calendario con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="5453e-116">Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5453e-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5453e-117">Remarks</span></span>

<span data-ttu-id="5453e-118">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5453e-118">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5453e-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5453e-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5453e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="5453e-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5453e-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5453e-121">Schema Name</span></span>  <br/> |<span data-ttu-id="5453e-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5453e-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="5453e-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5453e-123">Validation File</span></span>  <br/> |<span data-ttu-id="5453e-124">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5453e-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5453e-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5453e-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="5453e-126">Falso</span><span class="sxs-lookup"><span data-stu-id="5453e-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5453e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5453e-127">See also</span></span>



[<span data-ttu-id="5453e-128">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="5453e-128">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="5453e-129">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5453e-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

