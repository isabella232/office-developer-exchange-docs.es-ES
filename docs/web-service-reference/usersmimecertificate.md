---
title: UserSMIMECertificate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66e6b4ba-368d-4469-bd47-e59441b7d64d
description: El elemento UserSMIMECertificate contiene un valor que se codifica certificado SMIME de un contacto.
ms.openlocfilehash: 8b16f6768e3324c6d725a976210b8f7652155bf5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840938"
---
# <a name="usersmimecertificate"></a><span data-ttu-id="7fd90-103">UserSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="7fd90-103">UserSMIMECertificate</span></span>

<span data-ttu-id="7fd90-104">El elemento **UserSMIMECertificate** contiene un valor que se codifica certificado SMIME de un contacto.</span><span class="sxs-lookup"><span data-stu-id="7fd90-104">The **UserSMIMECertificate** element contains a value that encodes a contact's SMIME certificate.</span></span> 
  
```XML
<UserSMIMECertificate/>
```

 <span data-ttu-id="7fd90-105">**ArrayOfBinaryType**</span><span class="sxs-lookup"><span data-stu-id="7fd90-105">**ArrayOfBinaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7fd90-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7fd90-106">Attributes and elements</span></span>

<span data-ttu-id="7fd90-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7fd90-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fd90-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7fd90-108">Attributes</span></span>

<span data-ttu-id="7fd90-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7fd90-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7fd90-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7fd90-110">Child elements</span></span>

|<span data-ttu-id="7fd90-111">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="7fd90-111">**Element name**</span></span>|<span data-ttu-id="7fd90-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fd90-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fd90-113">Base64Binary</span><span class="sxs-lookup"><span data-stu-id="7fd90-113">Base64Binary</span></span>](base64binary.md) <br/> |<span data-ttu-id="7fd90-114">Contiene un valor con codificación Base64.</span><span class="sxs-lookup"><span data-stu-id="7fd90-114">Contains a Base64-encoded value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7fd90-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7fd90-115">Parent elements</span></span>

|<span data-ttu-id="7fd90-116">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="7fd90-116">**Element name**</span></span>|<span data-ttu-id="7fd90-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fd90-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fd90-118">Contact</span><span class="sxs-lookup"><span data-stu-id="7fd90-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="7fd90-119">Representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7fd90-119">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7fd90-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7fd90-120">Text value</span></span>

<span data-ttu-id="7fd90-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7fd90-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7fd90-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fd90-122">Remarks</span></span>

<span data-ttu-id="7fd90-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7fd90-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="7fd90-124">Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="7fd90-124">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fd90-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7fd90-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fd90-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7fd90-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7fd90-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7fd90-127">Schema name</span></span>  <br/> |<span data-ttu-id="7fd90-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7fd90-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="7fd90-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7fd90-129">Validation file</span></span>  <br/> |<span data-ttu-id="7fd90-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7fd90-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7fd90-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7fd90-131">Can be empty</span></span>  <br/> |<span data-ttu-id="7fd90-132">False</span><span class="sxs-lookup"><span data-stu-id="7fd90-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7fd90-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="7fd90-133">See also</span></span>



- [<span data-ttu-id="7fd90-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7fd90-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="7fd90-135">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="7fd90-135">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

