---
title: AccessLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 09475586-00fa-4e82-a915-5ca263ab4d1c
description: El elemento AccessLevel especifica el nivel de acceso para una reunión en línea.
ms.openlocfilehash: 3c1375ef37ea666c6c4fafce7daa46ae0d0a2696
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462342"
---
# <a name="accesslevel"></a><span data-ttu-id="aa363-103">AccessLevel</span><span class="sxs-lookup"><span data-stu-id="aa363-103">AccessLevel</span></span>

<span data-ttu-id="aa363-104">El elemento **AccessLevel** especifica el nivel de acceso para una reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="aa363-104">The **AccessLevel** element specifies the access level for an online meeting.</span></span> 
  
```XML
<AccessLevel/>
```

 <span data-ttu-id="aa363-105">**OnlineMeetingSettingsType**</span><span class="sxs-lookup"><span data-stu-id="aa363-105">**OnlineMeetingSettingsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa363-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aa363-106">Attributes and elements</span></span>

<span data-ttu-id="aa363-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aa363-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa363-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aa363-108">Attributes</span></span>

<span data-ttu-id="aa363-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aa363-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa363-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aa363-110">Child elements</span></span>

<span data-ttu-id="aa363-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aa363-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aa363-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aa363-112">Parent elements</span></span>

|<span data-ttu-id="aa363-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aa363-113">**Element**</span></span>|<span data-ttu-id="aa363-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa363-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa363-115">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="aa363-115">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md) <br/> |<span data-ttu-id="aa363-116">Especifica la configuración de las reuniones en línea.</span><span class="sxs-lookup"><span data-stu-id="aa363-116">Specifies the settings for online meetings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aa363-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="aa363-117">Text value</span></span>

<span data-ttu-id="aa363-118">En la siguiente tabla se enumeran los valores de texto para el elemento **AccessLevel** .</span><span class="sxs-lookup"><span data-stu-id="aa363-118">The following table lists the text values for the **AccessLevel** element.</span></span> 
  
<span data-ttu-id="aa363-119">**Valores de texto del elemento AccessLevel**</span><span class="sxs-lookup"><span data-stu-id="aa363-119">**AccessLevel element text values**</span></span>

|<span data-ttu-id="aa363-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="aa363-120">**Value**</span></span>|<span data-ttu-id="aa363-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa363-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa363-122">Todos</span><span class="sxs-lookup"><span data-stu-id="aa363-122">Everyone</span></span>  <br/> |<span data-ttu-id="aa363-123">El nivel de acceso está abierto a todos.</span><span class="sxs-lookup"><span data-stu-id="aa363-123">The access level is open to all.</span></span>  <br/> |
|<span data-ttu-id="aa363-124">Interno</span><span class="sxs-lookup"><span data-stu-id="aa363-124">Internal</span></span>  <br/> |<span data-ttu-id="aa363-125">El nivel de acceso es solo interno.</span><span class="sxs-lookup"><span data-stu-id="aa363-125">The access level is internal only.</span></span>  <br/> |
|<span data-ttu-id="aa363-126">Invitado</span><span class="sxs-lookup"><span data-stu-id="aa363-126">Invited</span></span>  <br/> |<span data-ttu-id="aa363-127">El nivel de acceso solo es participante invitado.</span><span class="sxs-lookup"><span data-stu-id="aa363-127">The access level is invited participants only.</span></span>  <br/> |
|<span data-ttu-id="aa363-128">Bloqueado</span><span class="sxs-lookup"><span data-stu-id="aa363-128">Locked</span></span>  <br/> |<span data-ttu-id="aa363-129">El nivel de acceso está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="aa363-129">The access level is locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa363-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa363-130">Remarks</span></span>

<span data-ttu-id="aa363-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa363-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="aa363-132">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aa363-132">This element was introduced in Exchange Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa363-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aa363-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa363-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa363-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aa363-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aa363-135">Schema name</span></span>  <br/> |<span data-ttu-id="aa363-136">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="aa363-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="aa363-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aa363-137">Validation file</span></span>  <br/> |<span data-ttu-id="aa363-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="aa363-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aa363-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aa363-139">Can be empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="aa363-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa363-140">See also</span></span>

- [<span data-ttu-id="aa363-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa363-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

