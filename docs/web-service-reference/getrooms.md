---
title: GetRooms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRooms
api_type:
- schema
ms.assetid: 82a737c7-da41-4777-8ad8-89851a0b602b
description: El elemento GetRooms es el elemento raíz en una solicitud para obtener una lista de salas dentro de una lista de salas determinado.
ms.openlocfilehash: a787097752cfeee9489e5f118549c2d939ba4c9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764967"
---
# <a name="getrooms"></a><span data-ttu-id="191d0-103">GetRooms</span><span class="sxs-lookup"><span data-stu-id="191d0-103">GetRooms</span></span>

<span data-ttu-id="191d0-104">El elemento **GetRooms** es el elemento raíz en una solicitud para obtener una lista de salas dentro de una lista de salas determinado.</span><span class="sxs-lookup"><span data-stu-id="191d0-104">The **GetRooms** element is the root element in a request to get a list of rooms within a particular room list.</span></span> 
  
```XML
<GetRooms>
   <RoomList/>
</GetRooms>
```

 <span data-ttu-id="191d0-105">**GetRoomsType**</span><span class="sxs-lookup"><span data-stu-id="191d0-105">**GetRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="191d0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="191d0-106">Attributes and elements</span></span>

<span data-ttu-id="191d0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="191d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="191d0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="191d0-108">Attributes</span></span>

<span data-ttu-id="191d0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="191d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="191d0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="191d0-110">Child elements</span></span>

|<span data-ttu-id="191d0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="191d0-111">**Element**</span></span>|<span data-ttu-id="191d0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="191d0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="191d0-113">RoomList</span><span class="sxs-lookup"><span data-stu-id="191d0-113">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="191d0-114">Representa una dirección de correo electrónico que identifica una lista de las salas de reuniones</span><span class="sxs-lookup"><span data-stu-id="191d0-114">Represents an e-mail address that identifies a list of meeting rooms</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="191d0-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="191d0-115">Parent elements</span></span>

<span data-ttu-id="191d0-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="191d0-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="191d0-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="191d0-117">Text value</span></span>

<span data-ttu-id="191d0-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="191d0-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="191d0-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="191d0-119">Remarks</span></span>

<span data-ttu-id="191d0-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="191d0-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="191d0-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="191d0-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="191d0-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="191d0-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="191d0-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="191d0-123">Schema Name</span></span>  <br/> |<span data-ttu-id="191d0-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="191d0-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="191d0-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="191d0-125">Validation File</span></span>  <br/> |<span data-ttu-id="191d0-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="191d0-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="191d0-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="191d0-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="191d0-128">False</span><span class="sxs-lookup"><span data-stu-id="191d0-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="191d0-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="191d0-129">See also</span></span>



- [<span data-ttu-id="191d0-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="191d0-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

