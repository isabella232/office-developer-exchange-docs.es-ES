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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467455"
---
# <a name="searchablemailbox"></a><span data-ttu-id="d0c33-103">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="d0c33-103">SearchableMailbox</span></span>

<span data-ttu-id="d0c33-104">El elemento **SearchableMailbox** especifica un buzón devuelto desde una solicitud **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="d0c33-104">The **SearchableMailbox** element specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="d0c33-105">**SearchableMailboxType**</span><span class="sxs-lookup"><span data-stu-id="d0c33-105">**SearchableMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0c33-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d0c33-106">Attributes and elements</span></span>

<span data-ttu-id="d0c33-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d0c33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0c33-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d0c33-108">Attributes</span></span>

<span data-ttu-id="d0c33-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d0c33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0c33-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d0c33-110">Child elements</span></span>

<span data-ttu-id="d0c33-111">[GUID](guid-ex15websvcsotherref.md)  |  [PrimarySmtpAddress (cadena)](primarysmtpaddress-string.md)  |  [IsExternalMailbox](isexternalmailbox.md)  |  [ExternalEmailAddress](externalemailaddress.md)  |  [DisplayName (cadena)](displayname-string.md)  |  [IsMembershipGroup](ismembershipgroup.md)  |  [Identificador](referenceid.md)</span><span class="sxs-lookup"><span data-stu-id="d0c33-111">[Guid](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [DisplayName (string)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md) | [ReferenceId](referenceid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0c33-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d0c33-112">Parent elements</span></span>

[<span data-ttu-id="d0c33-113">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="d0c33-113">SearchableMailboxes</span></span>](searchablemailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="d0c33-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0c33-114">Remarks</span></span>

<span data-ttu-id="d0c33-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0c33-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d0c33-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0c33-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0c33-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d0c33-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0c33-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0c33-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0c33-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d0c33-119">Schema name</span></span>  <br/> |<span data-ttu-id="d0c33-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d0c33-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0c33-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d0c33-121">Validation file</span></span>  <br/> |<span data-ttu-id="d0c33-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d0c33-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0c33-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d0c33-123">Can be empty</span></span>  <br/> ||
   

