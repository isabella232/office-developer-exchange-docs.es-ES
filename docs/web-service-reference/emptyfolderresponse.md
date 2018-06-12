---
title: EmptyFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c900be49-3c90-41aa-aba5-bcf1116ec2aa
description: El elemento EmptyFolderResponse define una respuesta a una solicitud de operación EmptyFolder.
ms.openlocfilehash: ab753351a1eb7deba83823875989816ba75b9809
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764383"
---
# <a name="emptyfolderresponse"></a><span data-ttu-id="eeee9-103">EmptyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="eeee9-103">EmptyFolderResponse</span></span>

<span data-ttu-id="eeee9-104">El elemento **EmptyFolderResponse** define una respuesta a una solicitud de [operación EmptyFolder](emptyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="eeee9-104">The **EmptyFolderResponse** element defines a response to an [EmptyFolder operation](emptyfolder-operation.md) request.</span></span> 
  
```XML
<EmptyFolderResponse>
   <ResponseMessages/>
</EmptyFolderResponse>
```

 <span data-ttu-id="eeee9-105">**EmptyFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="eeee9-105">**EmptyFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eeee9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eeee9-106">Attributes and elements</span></span>

<span data-ttu-id="eeee9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eeee9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eeee9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eeee9-108">Attributes</span></span>

<span data-ttu-id="eeee9-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eeee9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eeee9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eeee9-110">Child elements</span></span>

|<span data-ttu-id="eeee9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="eeee9-111">**Element**</span></span>|<span data-ttu-id="eeee9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eeee9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eeee9-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="eeee9-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="eeee9-114">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="eeee9-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eeee9-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eeee9-115">Parent elements</span></span>

<span data-ttu-id="eeee9-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eeee9-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eeee9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eeee9-117">Remarks</span></span>

<span data-ttu-id="eeee9-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="eeee9-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eeee9-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eeee9-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eeee9-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eeee9-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eeee9-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eeee9-121">Schema name</span></span>  <br/> |<span data-ttu-id="eeee9-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="eeee9-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eeee9-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eeee9-123">Validation file</span></span>  <br/> |<span data-ttu-id="eeee9-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eeee9-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eeee9-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eeee9-125">Can be empty</span></span>  <br/> |<span data-ttu-id="eeee9-126">False</span><span class="sxs-lookup"><span data-stu-id="eeee9-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eeee9-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="eeee9-127">See also</span></span>



[<span data-ttu-id="eeee9-128">Operación EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="eeee9-128">EmptyFolder operation</span></span>](emptyfolder-operation.md)
  
[<span data-ttu-id="eeee9-129">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="eeee9-129">EmptyFolder</span></span>](emptyfolder.md)


- [<span data-ttu-id="eeee9-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="eeee9-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

