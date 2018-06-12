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
description: El elemento de símbolo (token) contiene datos cifrados que representa el símbolo (token) de identificación para los datos compartidos.
ms.openlocfilehash: cec11d9f2c24a250483c5be6e273f981fdf0a8e6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840697"
---
# <a name="token"></a><span data-ttu-id="40503-103">Token</span><span class="sxs-lookup"><span data-stu-id="40503-103">Token</span></span>

<span data-ttu-id="40503-104">El elemento de **símbolo (token)** contiene datos cifrados que representa el símbolo (token) de identificación para los datos compartidos.</span><span class="sxs-lookup"><span data-stu-id="40503-104">The **Token** element contains encrypted data that represents the identification token for the shared data.</span></span> 
  
```xml
<Token/>
```

 <span data-ttu-id="40503-105">**EncryptedDataContainerType**</span><span class="sxs-lookup"><span data-stu-id="40503-105">**EncryptedDataContainerType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="40503-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="40503-106">Attributes and elements</span></span>

<span data-ttu-id="40503-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="40503-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40503-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="40503-108">Attributes</span></span>

<span data-ttu-id="40503-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="40503-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="40503-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40503-110">Child elements</span></span>

<span data-ttu-id="40503-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="40503-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="40503-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="40503-112">Parent elements</span></span>

|<span data-ttu-id="40503-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="40503-113">**Element**</span></span>|<span data-ttu-id="40503-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40503-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40503-115">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="40503-115">EncryptedSharedFolderData</span></span>](encryptedsharedfolderdata.md) <br/> |<span data-ttu-id="40503-116">Contiene los datos cifrados que un cliente puede usar para autorizar el uso compartido de su calendario o póngase en contacto con datos con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="40503-116">Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40503-117">Notas</span><span class="sxs-lookup"><span data-stu-id="40503-117">Remarks</span></span>

<span data-ttu-id="40503-118">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="40503-118">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40503-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="40503-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40503-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40503-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="40503-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="40503-121">Schema Name</span></span>  <br/> |<span data-ttu-id="40503-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="40503-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="40503-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="40503-123">Validation File</span></span>  <br/> |<span data-ttu-id="40503-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="40503-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="40503-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="40503-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="40503-126">False</span><span class="sxs-lookup"><span data-stu-id="40503-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40503-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="40503-127">See also</span></span>



[<span data-ttu-id="40503-128">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="40503-128">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="40503-129">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="40503-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

