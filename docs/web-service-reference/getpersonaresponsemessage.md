---
title: GetPersonaResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a5bf44c6-c46b-442d-98d4-8b49fdf14b30
description: El GetPersonaResponseMessage contiene los datos de la respuesta resultante de una solicitud de GetPersona.
ms.openlocfilehash: 7d38daac9c7c3a74ba9d9670c2bd16dcf2cd47e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764949"
---
# <a name="getpersonaresponsemessage"></a><span data-ttu-id="28333-103">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="28333-103">GetPersonaResponseMessage</span></span>

<span data-ttu-id="28333-104">El **GetPersonaResponseMessage** contiene los datos de la respuesta resultante de una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="28333-104">The **GetPersonaResponseMessage** contains the response data resulting from a **GetPersona** request.</span></span> 
  
```XML
<GetPersonaResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Persona/>
</GetPersonaResponseMessage>
```

 <span data-ttu-id="28333-105">**GetUserPhotoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="28333-105">**GetUserPhotoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28333-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="28333-106">Attributes and elements</span></span>

<span data-ttu-id="28333-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="28333-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28333-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="28333-108">Attributes</span></span>

<span data-ttu-id="28333-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="28333-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28333-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="28333-110">Child elements</span></span>

<span data-ttu-id="28333-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [rol](persona.md)</span><span class="sxs-lookup"><span data-stu-id="28333-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Persona](persona.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="28333-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="28333-112">Parent elements</span></span>

[<span data-ttu-id="28333-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="28333-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="28333-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28333-114">Remarks</span></span>

<span data-ttu-id="28333-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="28333-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="28333-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="28333-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28333-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="28333-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28333-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="28333-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="28333-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="28333-119">Schema name</span></span>  <br/> |<span data-ttu-id="28333-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="28333-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="28333-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="28333-121">Validation file</span></span>  <br/> |<span data-ttu-id="28333-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="28333-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28333-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="28333-123">Can be empty</span></span>  <br/> ||
   

