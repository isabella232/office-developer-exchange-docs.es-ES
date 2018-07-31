---
title: OutOfOffice
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutOfOffice
api_type:
- schema
ms.assetid: fe1256ab-5c0f-467d-abb3-b38a2dc312ae
description: El elemento de fuera de la oficina representa el mensaje de respuesta y un tiempo de duración para enviar el mensaje de respuesta.
ms.openlocfilehash: f35b84d7a8a37c7a57b58c97fd0d37318bb50a33
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354270"
---
# <a name="outofoffice"></a><span data-ttu-id="a9456-103">OutOfOffice</span><span class="sxs-lookup"><span data-stu-id="a9456-103">OutOfOffice</span></span>

<span data-ttu-id="a9456-104">El elemento de **fuera de la oficina** representa el mensaje de respuesta y un tiempo de duración para enviar el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a9456-104">The **OutOfOffice** element represents the response message and a duration time for sending the response message.</span></span> 
  
```XML
<OutOfOffice>
   <ReplyBody/>
   <Duration/>
</OutOfOffice>
```

```XML
<OutOfOffice>
   <ReplyBody/>
</OutOfOffice>
```

<span data-ttu-id="a9456-105">**OutOfOfficeMailTip**</span><span class="sxs-lookup"><span data-stu-id="a9456-105">**OutOfOfficeMailTip**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a9456-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a9456-106">Attributes and elements</span></span>

<span data-ttu-id="a9456-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a9456-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9456-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9456-108">Attributes</span></span>

<span data-ttu-id="a9456-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a9456-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9456-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9456-110">Child elements</span></span>

|<span data-ttu-id="a9456-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9456-111">**Element**</span></span>|<span data-ttu-id="a9456-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9456-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9456-113">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="a9456-113">ReplyBody</span></span>](replybody.md) <br/> |<span data-ttu-id="a9456-114">Contiene un mensaje de fuera de oficina (OOF) y el idioma utilizado para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a9456-114">Contains an Out of Office (OOF) message and the language used for the message.</span></span>  <br/> |
|[<span data-ttu-id="a9456-115">Duration (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="a9456-115">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="a9456-116">Contiene la duración que está habilitado el estado de fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en programado.</span><span class="sxs-lookup"><span data-stu-id="a9456-116">Contains the duration that the OOF status is enabled if the [OofState](oofstate.md) element is set to Scheduled.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a9456-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a9456-117">Parent elements</span></span>

|<span data-ttu-id="a9456-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9456-118">**Element**</span></span>|<span data-ttu-id="a9456-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9456-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9456-120">MailTips</span><span class="sxs-lookup"><span data-stu-id="a9456-120">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="a9456-121">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="a9456-121">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9456-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a9456-122">Text value</span></span>

<span data-ttu-id="a9456-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a9456-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9456-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9456-124">Remarks</span></span>

<span data-ttu-id="a9456-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a9456-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9456-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a9456-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9456-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9456-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9456-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a9456-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a9456-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a9456-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9456-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a9456-130">Validation File</span></span>  <br/> |<span data-ttu-id="a9456-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9456-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9456-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a9456-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a9456-133">False</span><span class="sxs-lookup"><span data-stu-id="a9456-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9456-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9456-134">See also</span></span>

- [<span data-ttu-id="a9456-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a9456-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

