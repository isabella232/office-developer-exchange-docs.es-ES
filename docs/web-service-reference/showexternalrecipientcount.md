---
title: ShowExternalRecipientCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ShowExternalRecipientCount
api_type:
- schema
ms.assetid: db28dbcb-d051-4e5c-a9c2-4b8d5149b4e1
description: El elemento ShowExternalRecipientCount indica si los consumidores de la operación GetMailTips tienen que Mostrar sugerencias de correo que indican el número de destinatarios externos a los que se dirige un mensaje.
ms.openlocfilehash: fc32e5c4a95f0e33b5532af9c77d31bd6446e641
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460473"
---
# <a name="showexternalrecipientcount"></a><span data-ttu-id="815e5-103">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="815e5-103">ShowExternalRecipientCount</span></span>

<span data-ttu-id="815e5-104">El elemento **ShowExternalRecipientCount** indica si los consumidores de la [operación GetMailTips](getmailtips-operation.md) tienen que Mostrar sugerencias de correo que indican el número de destinatarios externos a los que se dirige un mensaje.</span><span class="sxs-lookup"><span data-stu-id="815e5-104">The **ShowExternalRecipientCount** element indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> 
  
```XML
<ShowExternalRecipientCount>true | false</ShowExternalRecipientCount>
```

 <span data-ttu-id="815e5-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="815e5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="815e5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="815e5-106">Attributes and elements</span></span>

<span data-ttu-id="815e5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="815e5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="815e5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="815e5-108">Attributes</span></span>

<span data-ttu-id="815e5-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="815e5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="815e5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="815e5-110">Child elements</span></span>

<span data-ttu-id="815e5-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="815e5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="815e5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="815e5-112">Parent elements</span></span>

|<span data-ttu-id="815e5-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="815e5-113">**Element**</span></span>|<span data-ttu-id="815e5-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="815e5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="815e5-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="815e5-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="815e5-116">Contiene información de configuración del servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="815e5-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="815e5-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="815e5-117">Text value</span></span>

<span data-ttu-id="815e5-118">El valor de texto de este elemento es **true** si los consumidores de la [operación GetMailTips](getmailtips-operation.md) tienen que Mostrar sugerencias de correo que indican el número de destinatarios externos a los que se dirige un mensaje.</span><span class="sxs-lookup"><span data-stu-id="815e5-118">The text value of this element is **true** if consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="815e5-119">El valor es **false** si los consumidores de la [operación GetMailTips](getmailtips-operation.md) no tienen que Mostrar sugerencias de correo que indican el número de destinatarios externos a los que se dirige un mensaje.</span><span class="sxs-lookup"><span data-stu-id="815e5-119">The value is **false** if consumers of the [GetMailTips operation](getmailtips-operation.md) do not have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="815e5-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="815e5-120">Remarks</span></span>

<span data-ttu-id="815e5-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="815e5-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="815e5-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="815e5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="815e5-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="815e5-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="815e5-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="815e5-124">Schema Name</span></span>  <br/> |<span data-ttu-id="815e5-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="815e5-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="815e5-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="815e5-126">Validation File</span></span>  <br/> |<span data-ttu-id="815e5-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="815e5-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="815e5-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="815e5-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="815e5-129">Falso</span><span class="sxs-lookup"><span data-stu-id="815e5-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="815e5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="815e5-130">See also</span></span>



[<span data-ttu-id="815e5-131">Operación GetMailTips</span><span class="sxs-lookup"><span data-stu-id="815e5-131">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="815e5-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="815e5-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

