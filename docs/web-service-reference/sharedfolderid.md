---
title: SharedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharedFolderId
api_type:
- schema
ms.assetid: 21181ba3-9626-4284-9717-0b1c16948e8f
description: El elemento SharedFolderId representa el identificador de la carpeta compartida que se debe devolver el identificador de la carpeta local para la que una solicitud de operación GetSharingFolder.
ms.openlocfilehash: 6d4e541ef3cae89e413efa8cc5f1beaf651dc4dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837477"
---
# <a name="sharedfolderid"></a><span data-ttu-id="5170d-103">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="5170d-103">SharedFolderId</span></span>

<span data-ttu-id="5170d-104">El elemento **SharedFolderId** representa el identificador de la carpeta compartida que se debe devolver el identificador de la carpeta local para la que una solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="5170d-104">The **SharedFolderId** element represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```xml
<SharedFolderId/>
```

 <span data-ttu-id="5170d-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="5170d-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5170d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5170d-106">Attributes and elements</span></span>

<span data-ttu-id="5170d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5170d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5170d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5170d-108">Attributes</span></span>

<span data-ttu-id="5170d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5170d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5170d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5170d-110">Child elements</span></span>

<span data-ttu-id="5170d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5170d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5170d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5170d-112">Parent elements</span></span>

|<span data-ttu-id="5170d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5170d-113">**Element**</span></span>|<span data-ttu-id="5170d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5170d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5170d-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="5170d-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="5170d-116">Define una solicitud para obtener el identificador de la carpeta local de una carpeta compartida especificada.</span><span class="sxs-lookup"><span data-stu-id="5170d-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5170d-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5170d-117">Text value</span></span>

<span data-ttu-id="5170d-118">El valor de texto es una cadena que representa el identificador de la carpeta compartida que se debe devolver el identificador de la carpeta local para la que una solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="5170d-118">The text value is a string that represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5170d-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5170d-119">Remarks</span></span>

<span data-ttu-id="5170d-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5170d-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5170d-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5170d-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5170d-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5170d-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5170d-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5170d-123">Schema Name</span></span>  <br/> |<span data-ttu-id="5170d-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5170d-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5170d-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5170d-125">Validation File</span></span>  <br/> |<span data-ttu-id="5170d-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5170d-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5170d-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5170d-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="5170d-128">False</span><span class="sxs-lookup"><span data-stu-id="5170d-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5170d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5170d-129">See also</span></span>



[<span data-ttu-id="5170d-130">Operación GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="5170d-130">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="5170d-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5170d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

