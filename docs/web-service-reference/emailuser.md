---
title: EmailUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc8133ff-c34e-4921-bb56-06e79aee0a8a
description: El elemento EmailUser especifica a un destinatario de correo electrónico.
ms.openlocfilehash: e724b3996d37a42527ec1183cef9bb6b312b8c93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764382"
---
# <a name="emailuser"></a><span data-ttu-id="61903-103">EmailUser</span><span class="sxs-lookup"><span data-stu-id="61903-103">EmailUser</span></span>

<span data-ttu-id="61903-104">El elemento **EmailUser** especifica a un destinatario de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="61903-104">The **EmailUser** element specifies an email recipient.</span></span> 
  
```XML
<EmailUser>
    <Name/>
    <UserId/>
</EmailUser>
```

 <span data-ttu-id="61903-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="61903-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61903-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="61903-106">Attributes and elements</span></span>

<span data-ttu-id="61903-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="61903-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61903-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="61903-108">Attributes</span></span>

<span data-ttu-id="61903-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="61903-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61903-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61903-110">Child elements</span></span>

|<span data-ttu-id="61903-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="61903-111">**Element**</span></span>|<span data-ttu-id="61903-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61903-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61903-113">Name (cadena)</span><span class="sxs-lookup"><span data-stu-id="61903-113">Name (string)</span></span>](name-string.md) <br/> |<span data-ttu-id="61903-114">Especifica un nombre de búsqueda refinador o clave o el nombre de un usuario de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="61903-114">Specifies a search refiner name or key or the name of an email user.</span></span>  <br/> |
|[<span data-ttu-id="61903-115">UserId (cadena)</span><span class="sxs-lookup"><span data-stu-id="61903-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="61903-116">Especifica el identificador de usuario de un usuario de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="61903-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61903-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="61903-117">Parent elements</span></span>

|<span data-ttu-id="61903-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="61903-118">**Element**</span></span>|<span data-ttu-id="61903-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61903-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61903-120">Asistentes</span><span class="sxs-lookup"><span data-stu-id="61903-120">Attendees</span></span>](attendees.md) <br/> |<span data-ttu-id="61903-121">Especifica a los destinatarios de una invitación a una reunión.</span><span class="sxs-lookup"><span data-stu-id="61903-121">Specifies the recipients of an invitation to a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61903-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61903-122">Remarks</span></span>

<span data-ttu-id="61903-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61903-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="61903-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="61903-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61903-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="61903-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61903-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61903-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="61903-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="61903-127">Schema Name</span></span>  <br/> |<span data-ttu-id="61903-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="61903-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="61903-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="61903-129">Validation File</span></span>  <br/> |<span data-ttu-id="61903-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="61903-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="61903-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="61903-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="61903-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="61903-132">See also</span></span>



- [<span data-ttu-id="61903-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="61903-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

