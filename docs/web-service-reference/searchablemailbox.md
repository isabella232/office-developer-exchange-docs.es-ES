---
title: SearchableMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 339005cd-a3b9-47dd-bc7b-a860b699625b
description: El elemento SearchableMailbox especifica un buzón devuelto desde una solicitud GetSearchableMailboxes.
ms.openlocfilehash: f790d9a707f10f64a776b2fc35255c233ad854b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467455"
---
# <a name="searchablemailbox"></a><span data-ttu-id="02e78-103">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="02e78-103">SearchableMailbox</span></span>

<span data-ttu-id="02e78-104">El elemento **SearchableMailbox** especifica un buzón devuelto desde una solicitud **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="02e78-104">The **SearchableMailbox** element specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<SearchableMailbox>
   <Guid/>
   <PrimarySmtpAddress/>
   <IsExternalMailbox/>
   <ExternalEmailAddress/>
   <DisplayName/>
   <IsMembershipGroup/>
   <ReferenceId/>
</SearchableMailbox>
```

 <span data-ttu-id="02e78-105">**SearchableMailboxType**</span><span class="sxs-lookup"><span data-stu-id="02e78-105">**SearchableMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02e78-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="02e78-106">Attributes and elements</span></span>

<span data-ttu-id="02e78-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="02e78-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02e78-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="02e78-108">Attributes</span></span>

<span data-ttu-id="02e78-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="02e78-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02e78-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02e78-110">Child elements</span></span>

<span data-ttu-id="02e78-111">[GUID](guid-ex15websvcsotherref.md)  |  [PrimarySmtpAddress (cadena)](primarysmtpaddress-string.md)  |  [IsExternalMailbox](isexternalmailbox.md)  |  [ExternalEmailAddress](externalemailaddress.md)  |  [DisplayName (cadena)](displayname-string.md)  |  [IsMembershipGroup](ismembershipgroup.md)  |  [Identificador](referenceid.md)</span><span class="sxs-lookup"><span data-stu-id="02e78-111">[Guid](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [DisplayName (string)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md) | [ReferenceId](referenceid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="02e78-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="02e78-112">Parent elements</span></span>

[<span data-ttu-id="02e78-113">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="02e78-113">SearchableMailboxes</span></span>](searchablemailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="02e78-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02e78-114">Remarks</span></span>

<span data-ttu-id="02e78-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="02e78-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="02e78-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="02e78-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02e78-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="02e78-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02e78-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="02e78-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="02e78-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="02e78-119">Schema name</span></span>  <br/> |<span data-ttu-id="02e78-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="02e78-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="02e78-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="02e78-121">Validation file</span></span>  <br/> |<span data-ttu-id="02e78-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="02e78-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="02e78-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="02e78-123">Can be empty</span></span>  <br/> ||
   

