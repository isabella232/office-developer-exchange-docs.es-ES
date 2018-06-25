---
title: Salones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rooms
api_type:
- schema
ms.assetid: 57b6079a-3d83-4429-861e-c551e9e1a991
description: El elemento de salones es una lista de uno o más elementos que representan las salas de reuniones.
ms.openlocfilehash: e95112d3d565da29c309e45710ffc0ea9b4d5064
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837249"
---
# <a name="rooms"></a><span data-ttu-id="9bd50-103">Salones</span><span class="sxs-lookup"><span data-stu-id="9bd50-103">Rooms</span></span>

<span data-ttu-id="9bd50-104">El elemento de **salones** es una lista de uno o más elementos que representan las salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="9bd50-104">The **Rooms** element is a list of one or more elements that represent meeting rooms.</span></span> 
  
[<span data-ttu-id="9bd50-105">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="9bd50-105">GetRoomsResponse</span></span>](getroomsresponse.md)
  
[<span data-ttu-id="9bd50-106">Salones</span><span class="sxs-lookup"><span data-stu-id="9bd50-106">Rooms</span></span>](rooms.md)
  
```xml
<Rooms>   <Room/></Rooms>
```

 <span data-ttu-id="9bd50-107">**ArrayOfRoomsType**</span><span class="sxs-lookup"><span data-stu-id="9bd50-107">**ArrayOfRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9bd50-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9bd50-108">Attributes and elements</span></span>

<span data-ttu-id="9bd50-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9bd50-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9bd50-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="9bd50-110">Attributes</span></span>

<span data-ttu-id="9bd50-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9bd50-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9bd50-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9bd50-112">Child elements</span></span>

|<span data-ttu-id="9bd50-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9bd50-113">**Element**</span></span>|<span data-ttu-id="9bd50-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bd50-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bd50-115">Salón</span><span class="sxs-lookup"><span data-stu-id="9bd50-115">Room</span></span>](room.md) <br/> |<span data-ttu-id="9bd50-116">Define una dirección de correo electrónico y el nombre para mostrar que representa una sala de reuniones.</span><span class="sxs-lookup"><span data-stu-id="9bd50-116">Defines an e-mail address and display name that represents a meeting room.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9bd50-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9bd50-117">Parent elements</span></span>

|<span data-ttu-id="9bd50-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="9bd50-118">**Element**</span></span>|<span data-ttu-id="9bd50-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bd50-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bd50-120">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="9bd50-120">GetRoomsResponse</span></span>](getroomsresponse.md) <br/> ||
   
## <a name="remarks"></a><span data-ttu-id="9bd50-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9bd50-121">Remarks</span></span>

<span data-ttu-id="9bd50-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="9bd50-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9bd50-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9bd50-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bd50-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9bd50-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9bd50-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9bd50-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9bd50-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9bd50-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9bd50-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9bd50-127">Validation File</span></span>  <br/> |<span data-ttu-id="9bd50-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9bd50-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9bd50-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9bd50-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="9bd50-130">False</span><span class="sxs-lookup"><span data-stu-id="9bd50-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bd50-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bd50-131">See also</span></span>



[<span data-ttu-id="9bd50-132">Operación GetRooms</span><span class="sxs-lookup"><span data-stu-id="9bd50-132">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="9bd50-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9bd50-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

