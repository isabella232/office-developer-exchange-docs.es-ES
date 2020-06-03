---
title: FindPeopleResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba686738-e654-404d-ab54-83c71d030350
description: El elemento FindPeopleResponseMessage especifica el mensaje de respuesta para una solicitud de FindPeople.
ms.openlocfilehash: 5a2ce7b8643fff9d4a93b62459638d3a99605c98
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466377"
---
# <a name="findpeopleresponsemessage"></a><span data-ttu-id="04e30-103">FindPeopleResponseMessage</span><span class="sxs-lookup"><span data-stu-id="04e30-103">FindPeopleResponseMessage</span></span>

<span data-ttu-id="04e30-104">El elemento **FindPeopleResponseMessage** especifica el mensaje de respuesta para una solicitud de **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="04e30-104">The **FindPeopleResponseMessage** element specifies the response message for a **FindPeople** request.</span></span> 
  
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

 <span data-ttu-id="04e30-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="04e30-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04e30-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="04e30-106">Attributes and elements</span></span>

<span data-ttu-id="04e30-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="04e30-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04e30-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="04e30-108">Attributes</span></span>

<span data-ttu-id="04e30-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="04e30-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04e30-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="04e30-110">Child elements</span></span>

<span data-ttu-id="04e30-111">[MessageText](messagetext.md)  |  [ResponseCode](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [MessageXml](messagexml.md)  |  [Personas](people.md)  |  [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span><span class="sxs-lookup"><span data-stu-id="04e30-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [People](people.md) | [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="04e30-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="04e30-112">Parent elements</span></span>

[<span data-ttu-id="04e30-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="04e30-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="04e30-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04e30-114">Remarks</span></span>

<span data-ttu-id="04e30-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04e30-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="04e30-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="04e30-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04e30-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="04e30-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04e30-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="04e30-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="04e30-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="04e30-119">Schema name</span></span>  <br/> |<span data-ttu-id="04e30-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="04e30-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="04e30-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="04e30-121">Validation file</span></span>  <br/> |<span data-ttu-id="04e30-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="04e30-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="04e30-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="04e30-123">Can be empty</span></span>  <br/> |<span data-ttu-id="04e30-124">false</span><span class="sxs-lookup"><span data-stu-id="04e30-124">false</span></span>  <br/> |
   

