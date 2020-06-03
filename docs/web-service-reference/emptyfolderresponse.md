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
ms.openlocfilehash: 9b20df8c0b095870185aab14dbd1f7ff4fc47def
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530680"
---
# <a name="emptyfolderresponse"></a><span data-ttu-id="18859-103">EmptyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="18859-103">EmptyFolderResponse</span></span>

<span data-ttu-id="18859-104">El elemento **EmptyFolderResponse** define una respuesta a una solicitud de [operación EmptyFolder](emptyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="18859-104">The **EmptyFolderResponse** element defines a response to an [EmptyFolder operation](emptyfolder-operation.md) request.</span></span> 
  
```XML
<EmptyFolderResponse>
   <ResponseMessages/>
</EmptyFolderResponse>
```

 <span data-ttu-id="18859-105">**EmptyFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="18859-105">**EmptyFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18859-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="18859-106">Attributes and elements</span></span>

<span data-ttu-id="18859-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="18859-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18859-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="18859-108">Attributes</span></span>

<span data-ttu-id="18859-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="18859-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18859-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="18859-110">Child elements</span></span>

|<span data-ttu-id="18859-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="18859-111">**Element**</span></span>|<span data-ttu-id="18859-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18859-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18859-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="18859-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="18859-114">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="18859-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18859-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="18859-115">Parent elements</span></span>

<span data-ttu-id="18859-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="18859-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18859-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18859-117">Remarks</span></span>

<span data-ttu-id="18859-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="18859-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18859-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="18859-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18859-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="18859-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="18859-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="18859-121">Schema name</span></span>  <br/> |<span data-ttu-id="18859-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="18859-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="18859-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="18859-123">Validation file</span></span>  <br/> |<span data-ttu-id="18859-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="18859-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18859-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="18859-125">Can be empty</span></span>  <br/> |<span data-ttu-id="18859-126">Falso</span><span class="sxs-lookup"><span data-stu-id="18859-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18859-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="18859-127">See also</span></span>



[<span data-ttu-id="18859-128">Operación EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="18859-128">EmptyFolder operation</span></span>](emptyfolder-operation.md)
  
[<span data-ttu-id="18859-129">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="18859-129">EmptyFolder</span></span>](emptyfolder.md)


- [<span data-ttu-id="18859-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="18859-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

