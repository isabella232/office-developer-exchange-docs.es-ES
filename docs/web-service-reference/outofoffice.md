---
title: Oficina
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
description: El elemento Oficina representa el mensaje de respuesta y una duración de tiempo para enviar el mensaje de respuesta.
ms.openlocfilehash: 082a81b62e2b783b302b3e749e0066131a46d73e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456902"
---
# <a name="outofoffice"></a><span data-ttu-id="25913-103">Oficina</span><span class="sxs-lookup"><span data-stu-id="25913-103">OutOfOffice</span></span>

<span data-ttu-id="25913-104">El elemento **Oficina** representa el mensaje de respuesta y una duración de tiempo para enviar el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="25913-104">The **OutOfOffice** element represents the response message and a duration time for sending the response message.</span></span> 
  
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

<span data-ttu-id="25913-105">**OutOfOfficeMailTip**</span><span class="sxs-lookup"><span data-stu-id="25913-105">**OutOfOfficeMailTip**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="25913-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="25913-106">Attributes and elements</span></span>

<span data-ttu-id="25913-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="25913-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25913-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="25913-108">Attributes</span></span>

<span data-ttu-id="25913-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="25913-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25913-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25913-110">Child elements</span></span>

|<span data-ttu-id="25913-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="25913-111">**Element**</span></span>|<span data-ttu-id="25913-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25913-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25913-113">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="25913-113">ReplyBody</span></span>](replybody.md) <br/> |<span data-ttu-id="25913-114">Contiene un mensaje de fuera de la oficina (OOF) y el idioma que se usa para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="25913-114">Contains an Out of Office (OOF) message and the language used for the message.</span></span>  <br/> |
|[<span data-ttu-id="25913-115">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="25913-115">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="25913-116">Contiene la duración en la que se habilita el estado OOF si el elemento [OofState](oofstate.md) está establecido en programado.</span><span class="sxs-lookup"><span data-stu-id="25913-116">Contains the duration that the OOF status is enabled if the [OofState](oofstate.md) element is set to Scheduled.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="25913-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="25913-117">Parent elements</span></span>

|<span data-ttu-id="25913-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="25913-118">**Element**</span></span>|<span data-ttu-id="25913-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25913-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25913-120">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="25913-120">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="25913-121">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="25913-121">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="25913-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="25913-122">Text value</span></span>

<span data-ttu-id="25913-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25913-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="25913-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25913-124">Remarks</span></span>

<span data-ttu-id="25913-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="25913-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25913-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="25913-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25913-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="25913-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="25913-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="25913-128">Schema Name</span></span>  <br/> |<span data-ttu-id="25913-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="25913-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="25913-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="25913-130">Validation File</span></span>  <br/> |<span data-ttu-id="25913-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="25913-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="25913-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="25913-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="25913-133">Falso</span><span class="sxs-lookup"><span data-stu-id="25913-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25913-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="25913-134">See also</span></span>

- [<span data-ttu-id="25913-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="25913-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

