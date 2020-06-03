---
title: DeleteFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderResponse
api_type:
- schema
ms.assetid: 27578bda-ef0a-4a33-bccc-2c1bc1735424
description: El elemento DeleteFolderResponse define una respuesta a una solicitud DeleteFolder.
ms.openlocfilehash: 58b814662c769784c5fd682a9e039863a9787d8d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458491"
---
# <a name="deletefolderresponse"></a><span data-ttu-id="5d52c-103">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="5d52c-103">DeleteFolderResponse</span></span>

<span data-ttu-id="5d52c-104">El elemento **DeleteFolderResponse** define una respuesta a una solicitud DeleteFolder.</span><span class="sxs-lookup"><span data-stu-id="5d52c-104">The **DeleteFolderResponse** element defines a response to a DeleteFolder request.</span></span> 
  
```xml
<DeleteFolderResponse>
   <ResponseMessages/>
</DeleteFolderResponse>
```

 <span data-ttu-id="5d52c-105">**DeleteFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="5d52c-105">**DeleteFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d52c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5d52c-106">Attributes and elements</span></span>

<span data-ttu-id="5d52c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5d52c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d52c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d52c-108">Attributes</span></span>

<span data-ttu-id="5d52c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5d52c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d52c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5d52c-110">Child elements</span></span>

|<span data-ttu-id="5d52c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5d52c-111">**Element**</span></span>|<span data-ttu-id="5d52c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d52c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d52c-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5d52c-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="5d52c-114">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d52c-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5d52c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5d52c-115">Parent elements</span></span>

<span data-ttu-id="5d52c-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5d52c-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d52c-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d52c-117">Remarks</span></span>

<span data-ttu-id="5d52c-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5d52c-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d52c-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5d52c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d52c-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d52c-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5d52c-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5d52c-121">Schema name</span></span>  <br/> |<span data-ttu-id="5d52c-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5d52c-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5d52c-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5d52c-123">Validation file</span></span>  <br/> |<span data-ttu-id="5d52c-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5d52c-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5d52c-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5d52c-125">Can be empty</span></span>  <br/> |<span data-ttu-id="5d52c-126">Falso</span><span class="sxs-lookup"><span data-stu-id="5d52c-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d52c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d52c-127">See also</span></span>

- [<span data-ttu-id="5d52c-128">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="5d52c-128">DeleteFolder operation</span></span>](deletefolder-operation.md) 
- [<span data-ttu-id="5d52c-129">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="5d52c-129">DeleteFolder</span></span>](deletefolder.md)
- [<span data-ttu-id="5d52c-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5d52c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

