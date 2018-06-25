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
description: El elemento ShowExternalRecipientCount indica si los consumidores de la operación de GetMailTips tienen que mostrar sugerencias de correo que indican el número de destinatarios externos a la que se envía un mensaje.
ms.openlocfilehash: 1fd3ceb629689c560dc60afe01f0413602f79a0d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837491"
---
# <a name="showexternalrecipientcount"></a><span data-ttu-id="f3079-103">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="f3079-103">ShowExternalRecipientCount</span></span>

<span data-ttu-id="f3079-104">El elemento **ShowExternalRecipientCount** indica si los consumidores de la [operación de GetMailTips](getmailtips-operation.md) tienen que mostrar sugerencias de correo que indican el número de destinatarios externos a la que se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f3079-104">The **ShowExternalRecipientCount** element indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> 
  
```XML
<ShowExternalRecipientCount>true | false</ShowExternalRecipientCount>
```

 <span data-ttu-id="f3079-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3079-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f3079-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f3079-106">Attributes and elements</span></span>

<span data-ttu-id="f3079-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f3079-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3079-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3079-108">Attributes</span></span>

<span data-ttu-id="f3079-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f3079-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3079-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f3079-110">Child elements</span></span>

<span data-ttu-id="f3079-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f3079-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f3079-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f3079-112">Parent elements</span></span>

|<span data-ttu-id="f3079-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3079-113">**Element**</span></span>|<span data-ttu-id="f3079-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3079-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3079-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="f3079-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="f3079-116">Contiene información de configuración de servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="f3079-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f3079-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f3079-117">Text value</span></span>

<span data-ttu-id="f3079-118">El valor de texto de este elemento es **true** si los consumidores de la [operación de GetMailTips](getmailtips-operation.md) tienen que mostrar sugerencias de correo que indican el número de destinatarios externos a la que se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f3079-118">The text value of this element is **true** if consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="f3079-119">El valor es **false** si no es necesario que los consumidores de la [operación de GetMailTips](getmailtips-operation.md) Mostrar sugerencias de correo que indican el número de destinatarios externos a la que se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f3079-119">The value is **false** if consumers of the [GetMailTips operation](getmailtips-operation.md) do not have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f3079-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3079-120">Remarks</span></span>

<span data-ttu-id="f3079-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f3079-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3079-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f3079-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3079-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f3079-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f3079-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f3079-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f3079-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f3079-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f3079-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f3079-126">Validation File</span></span>  <br/> |<span data-ttu-id="f3079-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f3079-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f3079-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f3079-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f3079-129">False</span><span class="sxs-lookup"><span data-stu-id="f3079-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3079-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3079-130">See also</span></span>



[<span data-ttu-id="f3079-131">Operación GetMailTips</span><span class="sxs-lookup"><span data-stu-id="f3079-131">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="f3079-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f3079-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

