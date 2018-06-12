---
title: MailboxCulture
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxCulture
api_type:
- schema
ms.assetid: 105cc061-3c35-455f-b102-8023e2055632
description: El elemento MailboxCulture indica la referencia cultural que se utilizará al abrir un buzón de correo. Este elemento se produce en el encabezado SOAP.
ms.openlocfilehash: 9003560a89b83032b4dd1b7ff54f3101819cc3c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836266"
---
# <a name="mailboxculture"></a><span data-ttu-id="d3d38-104">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d3d38-104">MailboxCulture</span></span>

<span data-ttu-id="d3d38-105">El elemento **MailboxCulture** indica la referencia cultural que se utilizará al abrir un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d3d38-105">The **MailboxCulture** element indicates the culture to use when opening a mailbox.</span></span> <span data-ttu-id="d3d38-106">Este elemento se produce en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="d3d38-106">This element occurs in the SOAP header.</span></span> 
  
```xml
<MailboxCulture/>
```

<span data-ttu-id="d3d38-107">**MailboxCultureType**</span><span class="sxs-lookup"><span data-stu-id="d3d38-107">**MailboxCultureType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d3d38-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d3d38-108">Attributes and elements</span></span>

<span data-ttu-id="d3d38-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d3d38-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3d38-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="d3d38-110">Attributes</span></span>

<span data-ttu-id="d3d38-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d3d38-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3d38-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d3d38-112">Child elements</span></span>

<span data-ttu-id="d3d38-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d3d38-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d3d38-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d3d38-114">Parent elements</span></span>

<span data-ttu-id="d3d38-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d3d38-115">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d3d38-116">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d3d38-116">Text value</span></span>

<span data-ttu-id="d3d38-117">El valor de texto indica el idioma que se usa en las operaciones del servicio Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d3d38-117">The text value indicates the language that is used in the Exchange Web Service operations.</span></span> <span data-ttu-id="d3d38-118">Los valores posibles para este elemento se describen en RFC 3066.</span><span class="sxs-lookup"><span data-stu-id="d3d38-118">The possible values for this element are described by RFC 3066.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d3d38-119">Notas</span><span class="sxs-lookup"><span data-stu-id="d3d38-119">Remarks</span></span>

<span data-ttu-id="d3d38-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="d3d38-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3d38-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d3d38-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3d38-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d3d38-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d3d38-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d3d38-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d3d38-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d3d38-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="d3d38-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d3d38-125">Validation File</span></span>  <br/> |<span data-ttu-id="d3d38-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d3d38-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d3d38-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d3d38-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3d38-128">False</span><span class="sxs-lookup"><span data-stu-id="d3d38-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3d38-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="d3d38-129">See also</span></span>

- [<span data-ttu-id="d3d38-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d3d38-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

