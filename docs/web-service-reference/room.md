---
title: Salón
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Room
api_type:
- schema
ms.assetid: a2cde8b8-2d31-4ebf-8171-f4dfd650d079
description: El elemento de sala representa una sala de reuniones.
ms.openlocfilehash: e064a458b5a9265fc9dad63c87c641eaf47d7062
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837242"
---
# <a name="room"></a><span data-ttu-id="354b5-103">Salón</span><span class="sxs-lookup"><span data-stu-id="354b5-103">Room</span></span>

<span data-ttu-id="354b5-104">El elemento de **sala** representa una sala de reuniones.</span><span class="sxs-lookup"><span data-stu-id="354b5-104">The **Room** element represents a meeting room.</span></span> 
  
[<span data-ttu-id="354b5-105">Salones</span><span class="sxs-lookup"><span data-stu-id="354b5-105">Rooms</span></span>](rooms.md)
  
[<span data-ttu-id="354b5-106">Salón</span><span class="sxs-lookup"><span data-stu-id="354b5-106">Room</span></span>](room.md)
  
```XML
<Room>
   <Id/>
</Room>
```

 <span data-ttu-id="354b5-107">**RoomType**</span><span class="sxs-lookup"><span data-stu-id="354b5-107">**RoomType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="354b5-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="354b5-108">Attributes and elements</span></span>

<span data-ttu-id="354b5-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="354b5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="354b5-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="354b5-110">Attributes</span></span>

<span data-ttu-id="354b5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="354b5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="354b5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="354b5-112">Child elements</span></span>

|<span data-ttu-id="354b5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="354b5-113">**Element**</span></span>|<span data-ttu-id="354b5-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="354b5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="354b5-115">Identificador (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="354b5-115">Id (EmailAddressType)</span></span>](id-emailaddresstype.md) <br/> |<span data-ttu-id="354b5-116">Un identificador que contiene una dirección de correo electrónico y el nombre para mostrar que representa la sala de reuniones.</span><span class="sxs-lookup"><span data-stu-id="354b5-116">An identifier that contains an email address and display name that represents the meeting room.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="354b5-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="354b5-117">Parent elements</span></span>

|<span data-ttu-id="354b5-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="354b5-118">**Element**</span></span>|<span data-ttu-id="354b5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="354b5-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="354b5-120">Salones</span><span class="sxs-lookup"><span data-stu-id="354b5-120">Rooms</span></span>](rooms.md) <br/> |<span data-ttu-id="354b5-121">Define una lista de salas asociados con una característica común, como la que se encuentra en el mismo edificio de reuniones.</span><span class="sxs-lookup"><span data-stu-id="354b5-121">Defines a list of meeting rooms associated with a common feature, such as being located in the same building.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="354b5-122">Notas</span><span class="sxs-lookup"><span data-stu-id="354b5-122">Remarks</span></span>

<span data-ttu-id="354b5-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="354b5-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="354b5-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="354b5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="354b5-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="354b5-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="354b5-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="354b5-126">Schema Name</span></span>  <br/> |<span data-ttu-id="354b5-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="354b5-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="354b5-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="354b5-128">Validation File</span></span>  <br/> |<span data-ttu-id="354b5-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="354b5-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="354b5-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="354b5-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="354b5-131">False</span><span class="sxs-lookup"><span data-stu-id="354b5-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="354b5-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="354b5-132">See also</span></span>



[<span data-ttu-id="354b5-133">Operación GetRooms</span><span class="sxs-lookup"><span data-stu-id="354b5-133">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="354b5-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="354b5-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

