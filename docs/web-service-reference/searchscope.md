---
title: SearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4a53989e-eca6-45c4-afac-4d6ac19597d2
description: El elemento SearchScope especifica el ámbito de una búsqueda.
ms.openlocfilehash: df11c8db418ac90d1166030aeed3672c0b810052
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466867"
---
# <a name="searchscope"></a><span data-ttu-id="e8c12-103">SearchScope</span><span class="sxs-lookup"><span data-stu-id="e8c12-103">SearchScope</span></span>

<span data-ttu-id="e8c12-104">El elemento **SearchScope** especifica el ámbito de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e8c12-104">The **SearchScope** element specifies the scope of a search.</span></span> 
  
```XML
<SearchScope> PrimaryOnly | ArchiveOnly | All </SearchScope>
```

 <span data-ttu-id="e8c12-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="e8c12-105">**MailboxSearchLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8c12-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e8c12-106">Attributes and elements</span></span>

<span data-ttu-id="e8c12-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e8c12-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8c12-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e8c12-108">Attributes</span></span>

<span data-ttu-id="e8c12-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e8c12-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8c12-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e8c12-110">Child elements</span></span>

<span data-ttu-id="e8c12-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e8c12-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e8c12-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e8c12-112">Parent elements</span></span>

[<span data-ttu-id="e8c12-113">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="e8c12-113">MailboxSearchScope</span></span>](mailboxsearchscope.md)
  
## <a name="text-value"></a><span data-ttu-id="e8c12-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e8c12-114">Text value</span></span>

<span data-ttu-id="e8c12-115">El valor de texto del elemento **SearchScope** indica el tipo de buzón en el que se busca una búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="e8c12-115">The text value of the **SearchScope** element indicates the mailbox type that is searched for a discovery search.</span></span> <span data-ttu-id="e8c12-116">Un valor de texto de **PrimaryOnly** indica que se busca en el buzón principal.</span><span class="sxs-lookup"><span data-stu-id="e8c12-116">A text value of **PrimaryOnly** indicates that the primary mailbox is searched.</span></span> <span data-ttu-id="e8c12-117">Un valor de texto de **ArchiveOnly** indica que se busca en el buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="e8c12-117">A text value of **ArchiveOnly** indicates that the archive mailbox is searched.</span></span> <span data-ttu-id="e8c12-118">Un valor de texto de **All** indica que se busca en los buzones de archivo y los principales.</span><span class="sxs-lookup"><span data-stu-id="e8c12-118">A text value of **All** indicates that both the primary and archive mailboxes are searched.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e8c12-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8c12-119">Remarks</span></span>

<span data-ttu-id="e8c12-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e8c12-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e8c12-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8c12-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8c12-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e8c12-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8c12-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8c12-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e8c12-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e8c12-124">Schema name</span></span>  <br/> |<span data-ttu-id="e8c12-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e8c12-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="e8c12-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e8c12-126">Validation file</span></span>  <br/> |<span data-ttu-id="e8c12-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e8c12-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e8c12-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e8c12-128">Can be empty</span></span>  <br/> ||
   

