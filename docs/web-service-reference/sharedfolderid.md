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
description: El elemento SharedFolderId representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe ser devuelto por una solicitud de operación GetSharingFolder.
ms.openlocfilehash: 546e148540708725bcf335f39bf69d193124d210
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466125"
---
# <a name="sharedfolderid"></a><span data-ttu-id="a26c2-103">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="a26c2-103">SharedFolderId</span></span>

<span data-ttu-id="a26c2-104">El elemento **SharedFolderId** representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe ser devuelto por una solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a26c2-104">The **SharedFolderId** element represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```xml
<SharedFolderId/>
```

 <span data-ttu-id="a26c2-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="a26c2-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a26c2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a26c2-106">Attributes and elements</span></span>

<span data-ttu-id="a26c2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a26c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a26c2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a26c2-108">Attributes</span></span>

<span data-ttu-id="a26c2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a26c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a26c2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a26c2-110">Child elements</span></span>

<span data-ttu-id="a26c2-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a26c2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a26c2-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a26c2-112">Parent elements</span></span>

|<span data-ttu-id="a26c2-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a26c2-113">**Element**</span></span>|<span data-ttu-id="a26c2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a26c2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a26c2-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="a26c2-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="a26c2-116">Define una solicitud para obtener el identificador de carpeta local de una carpeta compartida especificada.</span><span class="sxs-lookup"><span data-stu-id="a26c2-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a26c2-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a26c2-117">Text value</span></span>

<span data-ttu-id="a26c2-118">El valor de texto es una cadena que representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe ser devuelto por una solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a26c2-118">The text value is a string that represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a26c2-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a26c2-119">Remarks</span></span>

<span data-ttu-id="a26c2-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a26c2-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a26c2-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a26c2-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a26c2-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="a26c2-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a26c2-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a26c2-123">Schema Name</span></span>  <br/> |<span data-ttu-id="a26c2-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a26c2-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a26c2-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a26c2-125">Validation File</span></span>  <br/> |<span data-ttu-id="a26c2-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a26c2-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a26c2-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a26c2-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="a26c2-128">Falso</span><span class="sxs-lookup"><span data-stu-id="a26c2-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a26c2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a26c2-129">See also</span></span>



[<span data-ttu-id="a26c2-130">Operación GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="a26c2-130">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="a26c2-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a26c2-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

