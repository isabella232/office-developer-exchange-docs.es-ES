---
title: CopyFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolderResponse
api_type:
- schema
ms.assetid: 5bfbb4d3-e2ed-4b84-96f7-2175f1947aed
description: El elemento CopyFolderResponse define una respuesta a una solicitud CopyFolder.
ms.openlocfilehash: aaf5d2bde8c9ba6b0c8aa6345af39dd9a6006ae5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458519"
---
# <a name="copyfolderresponse"></a><span data-ttu-id="f257a-103">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="f257a-103">CopyFolderResponse</span></span>

<span data-ttu-id="f257a-104">El elemento **CopyFolderResponse** define una respuesta a una solicitud CopyFolder.</span><span class="sxs-lookup"><span data-stu-id="f257a-104">The **CopyFolderResponse** element defines a response to a CopyFolder request.</span></span> 
  
```xml
<CopyFolderResponse>
   <ResponseMessages/>
</CopyFolderResponse>
```

 <span data-ttu-id="f257a-105">**CopyFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="f257a-105">**CopyFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f257a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f257a-106">Attributes and elements</span></span>

<span data-ttu-id="f257a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f257a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f257a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f257a-108">Attributes</span></span>

<span data-ttu-id="f257a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f257a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f257a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f257a-110">Child elements</span></span>

|<span data-ttu-id="f257a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f257a-111">**Element**</span></span>|<span data-ttu-id="f257a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f257a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f257a-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f257a-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f257a-114">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f257a-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f257a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f257a-115">Parent elements</span></span>

<span data-ttu-id="f257a-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f257a-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f257a-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f257a-117">Remarks</span></span>

<span data-ttu-id="f257a-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f257a-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f257a-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f257a-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f257a-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="f257a-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f257a-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f257a-121">Schema name</span></span>  <br/> |<span data-ttu-id="f257a-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f257a-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f257a-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f257a-123">Validation file</span></span>  <br/> |<span data-ttu-id="f257a-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f257a-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f257a-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f257a-125">Can be empty</span></span>  <br/> |<span data-ttu-id="f257a-126">Falso</span><span class="sxs-lookup"><span data-stu-id="f257a-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f257a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f257a-127">See also</span></span>



[<span data-ttu-id="f257a-128">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="f257a-128">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="f257a-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="f257a-129">CopyFolder</span></span>](copyfolder.md)


- [<span data-ttu-id="f257a-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f257a-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

