---
title: RoomLists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoomLists
api_type:
- schema
ms.assetid: 2b190823-b11e-4635-97e4-3aba5865fd05
description: El elemento RoomLists es una lista de una o varias direcciones que representan una lista de salas de reuniones.
ms.openlocfilehash: 8f6393b617331e5878e48113c94ca3546cba095e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459051"
---
# <a name="roomlists"></a><span data-ttu-id="8314d-103">RoomLists</span><span class="sxs-lookup"><span data-stu-id="8314d-103">RoomLists</span></span>

<span data-ttu-id="8314d-104">El elemento **RoomLists** es una lista de una o varias direcciones que representan una lista de salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="8314d-104">The **RoomLists** element is a list of one or more addresses that represent a list of meeting rooms.</span></span> 
  
[<span data-ttu-id="8314d-105">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="8314d-105">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
  
[<span data-ttu-id="8314d-106">RoomLists</span><span class="sxs-lookup"><span data-stu-id="8314d-106">RoomLists</span></span>](roomlists.md)
  
```xml
<RoomLists>   <Address/></RoomLists>
```

 <span data-ttu-id="8314d-107">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="8314d-107">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8314d-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8314d-108">Attributes and elements</span></span>

<span data-ttu-id="8314d-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8314d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8314d-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="8314d-110">Attributes</span></span>

<span data-ttu-id="8314d-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8314d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8314d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8314d-112">Child elements</span></span>

|<span data-ttu-id="8314d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8314d-113">**Element**</span></span>|<span data-ttu-id="8314d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8314d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8314d-115">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="8314d-115">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="8314d-116">Define la dirección de correo electrónico y el nombre para mostrar que representan la lista de salas.</span><span class="sxs-lookup"><span data-stu-id="8314d-116">Defines the e-mail address and display name that represents the room list.</span></span> <span data-ttu-id="8314d-117">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8314d-117">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8314d-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8314d-118">Parent elements</span></span>

|<span data-ttu-id="8314d-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8314d-119">**Element**</span></span>|<span data-ttu-id="8314d-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8314d-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8314d-121">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="8314d-121">GetRoomListsResponse</span></span>](getroomlistsresponse.md) <br/> |<span data-ttu-id="8314d-122">Contiene el estado y el resultado de una solicitud de [operación GetRoomLists](getroomlists-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="8314d-122">Contains the status and result of a [GetRoomLists operation](getroomlists-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8314d-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8314d-123">Remarks</span></span>

<span data-ttu-id="8314d-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="8314d-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8314d-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8314d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8314d-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="8314d-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8314d-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8314d-127">Schema Name</span></span>  <br/> |<span data-ttu-id="8314d-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8314d-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8314d-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8314d-129">Validation File</span></span>  <br/> |<span data-ttu-id="8314d-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8314d-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8314d-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8314d-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="8314d-132">Falso</span><span class="sxs-lookup"><span data-stu-id="8314d-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8314d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="8314d-133">See also</span></span>



[<span data-ttu-id="8314d-134">Operación GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="8314d-134">GetRoomLists operation</span></span>](getroomlists-operation.md)


- [<span data-ttu-id="8314d-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8314d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

