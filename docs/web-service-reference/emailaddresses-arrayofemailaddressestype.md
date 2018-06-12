---
title: EmailAddresses (ArrayOfEmailAddressesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95084659-aa5a-4bac-8977-00db3b87883e
description: El elemento EmailAddresses especifica una matriz de todas las direcciones de correo electrónico de la persona asociada.
ms.openlocfilehash: 292d4c3f12b01f25fd094b2ab6d9c2d484d37694
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764350"
---
# <a name="emailaddresses-arrayofemailaddressestype"></a><span data-ttu-id="fa407-103">EmailAddresses (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="fa407-103">EmailAddresses (ArrayOfEmailAddressesType)</span></span>

<span data-ttu-id="fa407-104">El elemento **EmailAddresses** especifica una matriz de todas las direcciones de correo electrónico de la persona asociada.</span><span class="sxs-lookup"><span data-stu-id="fa407-104">The **EmailAddresses** element specifies an array of all email addresses of the associated persona.</span></span> 
  
```XML
<EmailAddresses>
    <Address></Address>
</EmailAddresses>
```

 <span data-ttu-id="fa407-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="fa407-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa407-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa407-106">Attributes and elements</span></span>

<span data-ttu-id="fa407-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa407-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa407-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa407-108">Attributes</span></span>

<span data-ttu-id="fa407-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa407-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa407-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa407-110">Child elements</span></span>

|<span data-ttu-id="fa407-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa407-111">**Element**</span></span>|<span data-ttu-id="fa407-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa407-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa407-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="fa407-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="fa407-114">Representa una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="fa407-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa407-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa407-115">Parent elements</span></span>

|<span data-ttu-id="fa407-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa407-116">**Element**</span></span>|<span data-ttu-id="fa407-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa407-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa407-118">Rol</span><span class="sxs-lookup"><span data-stu-id="fa407-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="fa407-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="fa407-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa407-120">Notas</span><span class="sxs-lookup"><span data-stu-id="fa407-120">Remarks</span></span>

<span data-ttu-id="fa407-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fa407-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa407-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa407-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa407-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa407-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa407-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fa407-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa407-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa407-125">Schema Name</span></span>  <br/> |<span data-ttu-id="fa407-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="fa407-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="fa407-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa407-127">Validation File</span></span>  <br/> |<span data-ttu-id="fa407-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa407-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa407-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa407-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fa407-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="fa407-130">See also</span></span>



- [<span data-ttu-id="fa407-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fa407-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

