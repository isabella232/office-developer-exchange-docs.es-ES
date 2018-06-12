---
title: SearchPreviewItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 59b0b2db-a0ae-4162-a2cb-5f37f42fe872
description: El elemento SearchPreviewItem especifica la vista previa de elemento para una búsqueda de detección.
ms.openlocfilehash: 46b9d6049f856ce6e93b9e49e07516ec4b52d932
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837308"
---
# <a name="searchpreviewitem"></a><span data-ttu-id="41eb9-103">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="41eb9-103">SearchPreviewItem</span></span>

<span data-ttu-id="41eb9-104">El elemento **SearchPreviewItem** especifica la vista previa de elemento para una búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="41eb9-104">The **SearchPreviewItem** element specifies the item preview for a discovery search.</span></span> 
  
```XML
<SearchPreviewItem>
   <Id/>
   <Mailbox/>
   <ParentId/>
   <ItemClass/>
   <UniqueHash/>
   <SortValue/>
   <OwaLink/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <CreatedTime/>
   <ReceivedTime/>
   <SentTime/>
   <Subject/>
   <Size/>
   <Preview/>
   <Importance/>
   <Read/>
   <HasAttachment/>
   <ExtendedProperties/>
</SearchPreviewItem>
```

 <span data-ttu-id="41eb9-105">**SearchPreviewItemType**</span><span class="sxs-lookup"><span data-stu-id="41eb9-105">**SearchPreviewItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41eb9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="41eb9-106">Attributes and elements</span></span>

<span data-ttu-id="41eb9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="41eb9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41eb9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="41eb9-108">Attributes</span></span>

<span data-ttu-id="41eb9-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="41eb9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41eb9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="41eb9-110">Child elements</span></span>

<span data-ttu-id="41eb9-111">[Identificador (ItemIdType)](id-itemidtype.md) | [buzón (PreviewItemMailboxType)](mailbox-previewitemmailboxtype.md) | [ParentId](parentid.md) | [ItemClass](itemclass.md) | [UniqueHash](uniquehash.md) | [SortValue](sortvalue.md) | [OwaLink](owalink.md)  |  [ Remitente (string)](sender-string.md) | [ToRecipients (ArrayOfSmtpAddressType)](torecipients-arrayofsmtpaddresstype.md) | [CcRecipients](ccrecipients.md) | [BccRecipients](bccrecipients.md) | [CreatedTime](createdtime.md) | [ReceivedTime](receivedtime.md)  |  [ArrivedTime](senttime.md)  |  [Asunto](subject.md) | [tamaño (long)](size-long.md) | [Preview](preview-ex15websvcsotherref.md) | [importancia](importance.md) | [lectura](read.md) | [HasAttachment](hasattachment.md) | [() ExtendedProperties NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)</span><span class="sxs-lookup"><span data-stu-id="41eb9-111">[ID (ItemIdType)](id-itemidtype.md) | [Mailbox (PreviewItemMailboxType)](mailbox-previewitemmailboxtype.md) | [ParentId](parentid.md) | [ItemClass](itemclass.md) | [UniqueHash](uniquehash.md) | [SortValue](sortvalue.md) | [OwaLink](owalink.md) | [Sender (string)](sender-string.md) | [ToRecipients (ArrayOfSmtpAddressType)](torecipients-arrayofsmtpaddresstype.md) | [CcRecipients](ccrecipients.md) | [BccRecipients](bccrecipients.md) | [CreatedTime](createdtime.md) | [ReceivedTime](receivedtime.md) | [SentTime](senttime.md) | [Subject](subject.md) | [Size (long)](size-long.md) | [Preview](preview-ex15websvcsotherref.md) | [Importance](importance.md) | [Read](read.md) | [HasAttachment](hasattachment.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="41eb9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="41eb9-112">Parent elements</span></span>

[<span data-ttu-id="41eb9-113">Elementos (ArrayOfSearchPreviewItemsType)</span><span class="sxs-lookup"><span data-stu-id="41eb9-113">Items (ArrayOfSearchPreviewItemsType)</span></span>](items-arrayofsearchpreviewitemstype.md)
  
## <a name="remarks"></a><span data-ttu-id="41eb9-114">Notas</span><span class="sxs-lookup"><span data-stu-id="41eb9-114">Remarks</span></span>

<span data-ttu-id="41eb9-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="41eb9-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="41eb9-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="41eb9-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41eb9-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="41eb9-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41eb9-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="41eb9-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="41eb9-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="41eb9-119">Schema name</span></span>  <br/> |<span data-ttu-id="41eb9-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="41eb9-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="41eb9-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="41eb9-121">Validation file</span></span>  <br/> |<span data-ttu-id="41eb9-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="41eb9-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="41eb9-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="41eb9-123">Can be empty</span></span>  <br/> ||
   

