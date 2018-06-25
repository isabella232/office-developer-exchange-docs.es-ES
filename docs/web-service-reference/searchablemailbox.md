---
title: SearchableMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 339005cd-a3b9-47dd-bc7b-a860b699625b
description: El elemento SearchableMailbox especifica un buzón de correo devuelto desde una solicitud de GetSearchableMailboxes.
ms.openlocfilehash: 0d0981d050fa388e83eaa8408b60d305296c1f36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837284"
---
# <a name="searchablemailbox"></a><span data-ttu-id="49119-103">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="49119-103">SearchableMailbox</span></span>

<span data-ttu-id="49119-104">El elemento **SearchableMailbox** especifica un buzón de correo devuelto desde una solicitud de **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="49119-104">The **SearchableMailbox** element specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="49119-105">**SearchableMailboxType**</span><span class="sxs-lookup"><span data-stu-id="49119-105">**SearchableMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49119-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="49119-106">Attributes and elements</span></span>

<span data-ttu-id="49119-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="49119-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49119-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="49119-108">Attributes</span></span>

<span data-ttu-id="49119-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="49119-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49119-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="49119-110">Child elements</span></span>

<span data-ttu-id="49119-111">[GUID](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [DisplayName (string)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md)  |  [ ReferenceId](referenceid.md)</span><span class="sxs-lookup"><span data-stu-id="49119-111">[Guid](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [DisplayName (string)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md) | [ReferenceId](referenceid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="49119-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="49119-112">Parent elements</span></span>

[<span data-ttu-id="49119-113">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="49119-113">SearchableMailboxes</span></span>](searchablemailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="49119-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49119-114">Remarks</span></span>

<span data-ttu-id="49119-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49119-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="49119-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="49119-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49119-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="49119-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49119-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="49119-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="49119-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="49119-119">Schema name</span></span>  <br/> |<span data-ttu-id="49119-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="49119-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="49119-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="49119-121">Validation file</span></span>  <br/> |<span data-ttu-id="49119-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="49119-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="49119-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="49119-123">Can be empty</span></span>  <br/> ||
   

