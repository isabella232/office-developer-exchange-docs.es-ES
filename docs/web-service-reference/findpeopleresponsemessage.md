---
title: FindPeopleResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba686738-e654-404d-ab54-83c71d030350
description: El elemento FindPeopleResponseMessage especifica el mensaje de respuesta de una solicitud de FindPeople.
ms.openlocfilehash: 205f20b26b5097d24de45c5a5f9681f3557a6f87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764655"
---
# <a name="findpeopleresponsemessage"></a><span data-ttu-id="e77de-103">FindPeopleResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e77de-103">FindPeopleResponseMessage</span></span>

<span data-ttu-id="e77de-104">El elemento **FindPeopleResponseMessage** especifica el mensaje de respuesta de una solicitud de **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="e77de-104">The **FindPeopleResponseMessage** element specifies the response message for a **FindPeople** request.</span></span> 
  
```XML
<FindPeopleResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <People/>
   <TotalNumberOfPeopleInView/>
</FindPeopleResponseMessage>
```

 <span data-ttu-id="e77de-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e77de-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e77de-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e77de-106">Attributes and elements</span></span>

<span data-ttu-id="e77de-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e77de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e77de-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e77de-108">Attributes</span></span>

<span data-ttu-id="e77de-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e77de-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e77de-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e77de-110">Child elements</span></span>

<span data-ttu-id="e77de-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [personas](people.md) | [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span><span class="sxs-lookup"><span data-stu-id="e77de-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [People](people.md) | [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e77de-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e77de-112">Parent elements</span></span>

[<span data-ttu-id="e77de-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e77de-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="e77de-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e77de-114">Remarks</span></span>

<span data-ttu-id="e77de-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e77de-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e77de-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e77de-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e77de-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e77de-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e77de-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e77de-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e77de-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e77de-119">Schema name</span></span>  <br/> |<span data-ttu-id="e77de-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e77de-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e77de-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e77de-121">Validation file</span></span>  <br/> |<span data-ttu-id="e77de-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e77de-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e77de-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e77de-123">Can be empty</span></span>  <br/> |<span data-ttu-id="e77de-124">falso</span><span class="sxs-lookup"><span data-stu-id="e77de-124">false</span></span>  <br/> |
   

