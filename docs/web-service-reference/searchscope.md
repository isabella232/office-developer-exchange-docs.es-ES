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
ms.openlocfilehash: 352292952c735e7d3893790a660096c6b6966536
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837315"
---
# <a name="searchscope"></a><span data-ttu-id="f8438-103">SearchScope</span><span class="sxs-lookup"><span data-stu-id="f8438-103">SearchScope</span></span>

<span data-ttu-id="f8438-104">El elemento **SearchScope** especifica el ámbito de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f8438-104">The **SearchScope** element specifies the scope of a search.</span></span> 
  
```XML
<SearchScope> PrimaryOnly | ArchiveOnly | All </SearchScope>
```

 <span data-ttu-id="f8438-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="f8438-105">**MailboxSearchLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f8438-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f8438-106">Attributes and elements</span></span>

<span data-ttu-id="f8438-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f8438-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8438-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f8438-108">Attributes</span></span>

<span data-ttu-id="f8438-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f8438-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f8438-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f8438-110">Child elements</span></span>

<span data-ttu-id="f8438-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f8438-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f8438-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f8438-112">Parent elements</span></span>

[<span data-ttu-id="f8438-113">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="f8438-113">MailboxSearchScope</span></span>](mailboxsearchscope.md)
  
## <a name="text-value"></a><span data-ttu-id="f8438-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f8438-114">Text value</span></span>

<span data-ttu-id="f8438-115">El valor de texto del elemento **SearchScope** indica el tipo de buzón de correo que se va a buscar una búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="f8438-115">The text value of the **SearchScope** element indicates the mailbox type that is searched for a discovery search.</span></span> <span data-ttu-id="f8438-116">Un valor de texto de **PrimaryOnly** indica que se busca en el buzón principal.</span><span class="sxs-lookup"><span data-stu-id="f8438-116">A text value of **PrimaryOnly** indicates that the primary mailbox is searched.</span></span> <span data-ttu-id="f8438-117">Un valor de texto de **ArchiveOnly** indica que se busca en el buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="f8438-117">A text value of **ArchiveOnly** indicates that the archive mailbox is searched.</span></span> <span data-ttu-id="f8438-118">Indica un valor de texto de **todos los** que ambos la principal y se buscan los buzones de archivo.</span><span class="sxs-lookup"><span data-stu-id="f8438-118">A text value of **All** indicates that both the primary and archive mailboxes are searched.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f8438-119">Notas</span><span class="sxs-lookup"><span data-stu-id="f8438-119">Remarks</span></span>

<span data-ttu-id="f8438-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f8438-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f8438-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f8438-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8438-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f8438-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8438-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8438-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f8438-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f8438-124">Schema name</span></span>  <br/> |<span data-ttu-id="f8438-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f8438-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f8438-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f8438-126">Validation file</span></span>  <br/> |<span data-ttu-id="f8438-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f8438-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f8438-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f8438-128">Can be empty</span></span>  <br/> ||
   

