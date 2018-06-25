---
title: MSExchangeCertificate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c514f22f-be3e-4cad-ac56-bdff6bafcee6
description: El elemento MSExchangeCertificate contiene un valor que se codifica el certificado de Microsoft Exchange de un contacto.
ms.openlocfilehash: 8d07198012485b5c6d22e1fb4721890bf9a5eb39
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836498"
---
# <a name="msexchangecertificate"></a><span data-ttu-id="d0df2-103">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="d0df2-103">MSExchangeCertificate</span></span>

<span data-ttu-id="d0df2-104">El elemento **MSExchangeCertificate** contiene un valor que se codifica el certificado de Microsoft Exchange de un contacto.</span><span class="sxs-lookup"><span data-stu-id="d0df2-104">The **MSExchangeCertificate** element contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span> 
  
```XML
<MSExchangeCertificate/>
```

 <span data-ttu-id="d0df2-105">**ArrayOfBinaryType**</span><span class="sxs-lookup"><span data-stu-id="d0df2-105">**ArrayOfBinaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0df2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d0df2-106">Attributes and elements</span></span>

<span data-ttu-id="d0df2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d0df2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0df2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d0df2-108">Attributes</span></span>

<span data-ttu-id="d0df2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d0df2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0df2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d0df2-110">Child elements</span></span>

|<span data-ttu-id="d0df2-111">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="d0df2-111">**Element name**</span></span>|<span data-ttu-id="d0df2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0df2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0df2-113">Base64Binary</span><span class="sxs-lookup"><span data-stu-id="d0df2-113">Base64Binary</span></span>](base64binary.md) <br/> |<span data-ttu-id="d0df2-114">Contiene un valor con codificación Base64.</span><span class="sxs-lookup"><span data-stu-id="d0df2-114">Contains a Base64-encoded value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d0df2-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d0df2-115">Parent elements</span></span>

|<span data-ttu-id="d0df2-116">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="d0df2-116">**Element name**</span></span>|<span data-ttu-id="d0df2-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0df2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0df2-118">Contact</span><span class="sxs-lookup"><span data-stu-id="d0df2-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="d0df2-119">Representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0df2-119">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d0df2-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d0df2-120">Text value</span></span>

<span data-ttu-id="d0df2-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d0df2-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0df2-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0df2-122">Remarks</span></span>

<span data-ttu-id="d0df2-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0df2-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="d0df2-124">Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="d0df2-124">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0df2-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d0df2-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0df2-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d0df2-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0df2-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d0df2-127">Schema name</span></span>  <br/> |<span data-ttu-id="d0df2-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d0df2-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0df2-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d0df2-129">Validation file</span></span>  <br/> |<span data-ttu-id="d0df2-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d0df2-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0df2-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d0df2-131">Can be empty</span></span>  <br/> |<span data-ttu-id="d0df2-132">False</span><span class="sxs-lookup"><span data-stu-id="d0df2-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0df2-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0df2-133">See also</span></span>



- [<span data-ttu-id="d0df2-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d0df2-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d0df2-135">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="d0df2-135">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

