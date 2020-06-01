---
title: UserSMIMECertificate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66e6b4ba-368d-4469-bd47-e59441b7d64d
description: El elemento UserSMIMECertificate contiene un valor que codifica el certificado SMIME de un contacto.
ms.openlocfilehash: 7e2dbc6a9c8b04758ba99db036e237d8837850aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467658"
---
# <a name="usersmimecertificate"></a><span data-ttu-id="dc574-103">UserSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="dc574-103">UserSMIMECertificate</span></span>

<span data-ttu-id="dc574-104">El elemento **UserSMIMECertificate** contiene un valor que codifica el certificado SMIME de un contacto.</span><span class="sxs-lookup"><span data-stu-id="dc574-104">The **UserSMIMECertificate** element contains a value that encodes a contact's SMIME certificate.</span></span> 
  
```XML
<UserSMIMECertificate/>
```

 <span data-ttu-id="dc574-105">**ArrayOfBinaryType**</span><span class="sxs-lookup"><span data-stu-id="dc574-105">**ArrayOfBinaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc574-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dc574-106">Attributes and elements</span></span>

<span data-ttu-id="dc574-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dc574-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc574-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dc574-108">Attributes</span></span>

<span data-ttu-id="dc574-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dc574-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc574-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dc574-110">Child elements</span></span>

|<span data-ttu-id="dc574-111">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="dc574-111">**Element name**</span></span>|<span data-ttu-id="dc574-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc574-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc574-113">Base64Binary</span><span class="sxs-lookup"><span data-stu-id="dc574-113">Base64Binary</span></span>](base64binary.md) <br/> |<span data-ttu-id="dc574-114">Contiene un valor codificado en Base64.</span><span class="sxs-lookup"><span data-stu-id="dc574-114">Contains a Base64-encoded value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dc574-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dc574-115">Parent elements</span></span>

|<span data-ttu-id="dc574-116">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="dc574-116">**Element name**</span></span>|<span data-ttu-id="dc574-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc574-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc574-118">Contacto</span><span class="sxs-lookup"><span data-stu-id="dc574-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="dc574-119">Representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dc574-119">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dc574-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="dc574-120">Text value</span></span>

<span data-ttu-id="dc574-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dc574-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc574-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc574-122">Remarks</span></span>

<span data-ttu-id="dc574-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="dc574-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="dc574-124">Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="dc574-124">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc574-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dc574-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc574-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc574-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc574-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dc574-127">Schema name</span></span>  <br/> |<span data-ttu-id="dc574-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="dc574-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc574-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dc574-129">Validation file</span></span>  <br/> |<span data-ttu-id="dc574-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="dc574-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc574-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dc574-131">Can be empty</span></span>  <br/> |<span data-ttu-id="dc574-132">Falso</span><span class="sxs-lookup"><span data-stu-id="dc574-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc574-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc574-133">See also</span></span>



- [<span data-ttu-id="dc574-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="dc574-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="dc574-135">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="dc574-135">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

