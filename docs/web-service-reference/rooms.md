---
title: Sala
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
description: El elemento Rooms es una lista de uno o varios elementos que representan salas de reuniones.
ms.openlocfilehash: f8b60a9680f6abba459ebecc96613abfdd93766d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466188"
---
# <a name="rooms"></a><span data-ttu-id="f9024-103">Sala</span><span class="sxs-lookup"><span data-stu-id="f9024-103">Rooms</span></span>

<span data-ttu-id="f9024-104">El elemento **Rooms** es una lista de uno o varios elementos que representan salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="f9024-104">The **Rooms** element is a list of one or more elements that represent meeting rooms.</span></span> 
  
[<span data-ttu-id="f9024-105">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="f9024-105">GetRoomsResponse</span></span>](getroomsresponse.md)
  
[<span data-ttu-id="f9024-106">Sala</span><span class="sxs-lookup"><span data-stu-id="f9024-106">Rooms</span></span>](rooms.md)
  
```xml
<Rooms>   <Room/></Rooms>
```

 <span data-ttu-id="f9024-107">**ArrayOfRoomsType**</span><span class="sxs-lookup"><span data-stu-id="f9024-107">**ArrayOfRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9024-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f9024-108">Attributes and elements</span></span>

<span data-ttu-id="f9024-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f9024-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9024-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9024-110">Attributes</span></span>

<span data-ttu-id="f9024-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f9024-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9024-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f9024-112">Child elements</span></span>

|<span data-ttu-id="f9024-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f9024-113">**Element**</span></span>|<span data-ttu-id="f9024-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9024-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9024-115">Sala</span><span class="sxs-lookup"><span data-stu-id="f9024-115">Room</span></span>](room.md) <br/> |<span data-ttu-id="f9024-116">Define una dirección de correo electrónico y un nombre para mostrar que representan una sala de reuniones.</span><span class="sxs-lookup"><span data-stu-id="f9024-116">Defines an e-mail address and display name that represents a meeting room.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f9024-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f9024-117">Parent elements</span></span>

|<span data-ttu-id="f9024-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f9024-118">**Element**</span></span>|<span data-ttu-id="f9024-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9024-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9024-120">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="f9024-120">GetRoomsResponse</span></span>](getroomsresponse.md) <br/> ||
   
## <a name="remarks"></a><span data-ttu-id="f9024-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9024-121">Remarks</span></span>

<span data-ttu-id="f9024-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f9024-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9024-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f9024-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9024-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9024-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f9024-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f9024-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f9024-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f9024-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f9024-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f9024-127">Validation File</span></span>  <br/> |<span data-ttu-id="f9024-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f9024-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f9024-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f9024-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="f9024-130">Falso</span><span class="sxs-lookup"><span data-stu-id="f9024-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9024-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9024-131">See also</span></span>



[<span data-ttu-id="f9024-132">Operación GetRooms</span><span class="sxs-lookup"><span data-stu-id="f9024-132">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="f9024-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f9024-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

