---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: El elemento IsWritable especifica si se puede escribir en el contacto subyacente o el destinatario de Active Directory.
ms.openlocfilehash: 03f258d01ecfc12dfa4e09ac88f4a75340d2acf3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836158"
---
# <a name="iswritable"></a><span data-ttu-id="912c5-103">IsWritable</span><span class="sxs-lookup"><span data-stu-id="912c5-103">IsWritable</span></span>

<span data-ttu-id="912c5-104">El elemento **IsWritable** especifica si se puede escribir en el contacto subyacente o el destinatario de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="912c5-104">The **IsWritable** element specifies whether the underlying contact or Active Directory recipient can be written to.</span></span> 
  
```XML
<IsWritable> true | false </IsWritable>
```

 <span data-ttu-id="912c5-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="912c5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="912c5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="912c5-106">Attributes and elements</span></span>

<span data-ttu-id="912c5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="912c5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="912c5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="912c5-108">Attributes</span></span>

<span data-ttu-id="912c5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="912c5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="912c5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="912c5-110">Child elements</span></span>

<span data-ttu-id="912c5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="912c5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="912c5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="912c5-112">Parent elements</span></span>

[<span data-ttu-id="912c5-113">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="912c5-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
  
## <a name="text-value"></a><span data-ttu-id="912c5-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="912c5-114">Text value</span></span>

<span data-ttu-id="912c5-115">Un valor de texto de **true** para el elemento **IsWritable** indica que el contacto o el objeto de Active Directory está disponible para el acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="912c5-115">A text value of **true** for the **IsWritable** element indicates that the contact or Active Directory object is available for write access.</span></span> <span data-ttu-id="912c5-116">Un valor de **false** indica que el contacto o el objeto de Active Directory no está disponible para el acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="912c5-116">A value of **false** indicates that the contact or Active Directory object is not available for write access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="912c5-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="912c5-117">Remarks</span></span>

<span data-ttu-id="912c5-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="912c5-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="912c5-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="912c5-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

