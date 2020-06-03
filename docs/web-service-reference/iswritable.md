---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: El elemento IsWritable especifica si se puede escribir en el contacto subyacente o en el destinatario de Active Directory.
ms.openlocfilehash: 96075adc1772027456f8829eee43bdc734644c09
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467574"
---
# <a name="iswritable"></a><span data-ttu-id="0551e-103">IsWritable</span><span class="sxs-lookup"><span data-stu-id="0551e-103">IsWritable</span></span>

<span data-ttu-id="0551e-104">El elemento **IsWritable** especifica si se puede escribir en el contacto subyacente o en el destinatario de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0551e-104">The **IsWritable** element specifies whether the underlying contact or Active Directory recipient can be written to.</span></span> 
  
```XML
<IsWritable> true | false </IsWritable>
```

 <span data-ttu-id="0551e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0551e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0551e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0551e-106">Attributes and elements</span></span>

<span data-ttu-id="0551e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0551e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0551e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0551e-108">Attributes</span></span>

<span data-ttu-id="0551e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0551e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0551e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0551e-110">Child elements</span></span>

<span data-ttu-id="0551e-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0551e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0551e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0551e-112">Parent elements</span></span>

[<span data-ttu-id="0551e-113">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="0551e-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
  
## <a name="text-value"></a><span data-ttu-id="0551e-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0551e-114">Text value</span></span>

<span data-ttu-id="0551e-115">Un valor de texto de **true** para el elemento **IsWritable** indica que el objeto de contacto o de Active Directory está disponible para el acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="0551e-115">A text value of **true** for the **IsWritable** element indicates that the contact or Active Directory object is available for write access.</span></span> <span data-ttu-id="0551e-116">Un valor de **false** indica que el contacto o el objeto de Active Directory no está disponible para el acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="0551e-116">A value of **false** indicates that the contact or Active Directory object is not available for write access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0551e-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0551e-117">Remarks</span></span>

<span data-ttu-id="0551e-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0551e-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0551e-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0551e-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

