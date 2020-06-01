---
title: EmailAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EmailAddresses
api_type:
- schema
ms.assetid: fd4d773c-f7dc-4a04-9025-e772d7a45fdf
description: El elemento EmailAddresses representa una colección de direcciones de correo electrónico de un contacto.
ms.openlocfilehash: 9d247f6159d621124ecdd9968ee468ed2b4fe84b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456181"
---
# <a name="emailaddresses"></a><span data-ttu-id="af512-103">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="af512-103">EmailAddresses</span></span>

<span data-ttu-id="af512-104">El elemento **EmailAddresses** representa una colección de direcciones de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="af512-104">The **EmailAddresses** element represents a collection of e-mail addresses for a contact.</span></span> 
  
```xml
<EmailAddresses>
   <Entry/>
</EmailAddresses>
```

 <span data-ttu-id="af512-105">**EmailAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="af512-105">**EmailAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af512-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="af512-106">Attributes and elements</span></span>

<span data-ttu-id="af512-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="af512-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af512-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="af512-108">Attributes</span></span>

<span data-ttu-id="af512-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="af512-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af512-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="af512-110">Child elements</span></span>

|<span data-ttu-id="af512-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="af512-111">**Element**</span></span>|<span data-ttu-id="af512-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af512-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af512-113">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="af512-113">Entry (EmailAddress)</span></span>](entry-emailaddress.md) <br/> |<span data-ttu-id="af512-114">Representa una sola dirección de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="af512-114">Represents a single e-mail address for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af512-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="af512-115">Parent elements</span></span>

|<span data-ttu-id="af512-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="af512-116">**Element**</span></span>|<span data-ttu-id="af512-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af512-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af512-118">Contacto</span><span class="sxs-lookup"><span data-stu-id="af512-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="af512-119">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="af512-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af512-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af512-120">Remarks</span></span>

<span data-ttu-id="af512-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="af512-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af512-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="af512-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af512-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="af512-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af512-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="af512-124">Schema name</span></span>  <br/> |<span data-ttu-id="af512-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="af512-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="af512-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="af512-126">Validation file</span></span>  <br/> |<span data-ttu-id="af512-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="af512-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af512-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="af512-128">Can be empty</span></span>  <br/> |<span data-ttu-id="af512-129">Falso</span><span class="sxs-lookup"><span data-stu-id="af512-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af512-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="af512-130">See also</span></span>

- [<span data-ttu-id="af512-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="af512-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="af512-132">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="af512-132">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="af512-133">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="af512-133">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx) 
- [<span data-ttu-id="af512-134">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="af512-134">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

