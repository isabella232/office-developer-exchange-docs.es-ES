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
ms.openlocfilehash: 2eddb68ecffd8f61a2fbb775d8013433d715db1a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764351"
---
# <a name="emailaddresses"></a><span data-ttu-id="d37de-103">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="d37de-103">EmailAddresses</span></span>

<span data-ttu-id="d37de-104">El elemento **EmailAddresses** representa una colección de direcciones de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="d37de-104">The **EmailAddresses** element represents a collection of e-mail addresses for a contact.</span></span> 
  
```xml
<EmailAddresses>
   <Entry/>
</EmailAddresses>
```

 <span data-ttu-id="d37de-105">**EmailAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="d37de-105">**EmailAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d37de-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d37de-106">Attributes and elements</span></span>

<span data-ttu-id="d37de-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d37de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d37de-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d37de-108">Attributes</span></span>

<span data-ttu-id="d37de-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d37de-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d37de-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d37de-110">Child elements</span></span>

|<span data-ttu-id="d37de-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d37de-111">**Element**</span></span>|<span data-ttu-id="d37de-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d37de-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d37de-113">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="d37de-113">Entry (EmailAddress)</span></span>](entry-emailaddress.md) <br/> |<span data-ttu-id="d37de-114">Representa una dirección de correo electrónico única para un contacto.</span><span class="sxs-lookup"><span data-stu-id="d37de-114">Represents a single e-mail address for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d37de-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d37de-115">Parent elements</span></span>

|<span data-ttu-id="d37de-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d37de-116">**Element**</span></span>|<span data-ttu-id="d37de-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d37de-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d37de-118">Contact</span><span class="sxs-lookup"><span data-stu-id="d37de-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="d37de-119">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d37de-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d37de-120">Notas</span><span class="sxs-lookup"><span data-stu-id="d37de-120">Remarks</span></span>

<span data-ttu-id="d37de-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d37de-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d37de-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d37de-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d37de-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d37de-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d37de-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d37de-124">Schema name</span></span>  <br/> |<span data-ttu-id="d37de-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d37de-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="d37de-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d37de-126">Validation file</span></span>  <br/> |<span data-ttu-id="d37de-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d37de-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d37de-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d37de-128">Can be empty</span></span>  <br/> |<span data-ttu-id="d37de-129">False</span><span class="sxs-lookup"><span data-stu-id="d37de-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d37de-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="d37de-130">See also</span></span>

- [<span data-ttu-id="d37de-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d37de-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="d37de-132">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="d37de-132">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="d37de-133">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="d37de-133">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx) 
- [<span data-ttu-id="d37de-134">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="d37de-134">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

