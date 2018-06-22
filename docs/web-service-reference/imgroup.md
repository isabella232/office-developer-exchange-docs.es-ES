---
title: ImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7b884e-ecf1-4e58-86ec-856b13a95f2b
description: El elemento ImGroup representa un grupo de mensajería instantáneo.
ms.openlocfilehash: 2a444158dbc6a73b1aee7b306cc251d33d005c43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835890"
---
# <a name="imgroup"></a><span data-ttu-id="9e4c2-103">ImGroup</span><span class="sxs-lookup"><span data-stu-id="9e4c2-103">ImGroup</span></span>

<span data-ttu-id="9e4c2-104">El elemento **ImGroup** representa un grupo de mensajería instantáneo.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-104">The **ImGroup** element represents an instant messaging group.</span></span> 
  
```XML
<ImGroup>
   <DisplayName/>
   <GroupType/>
   <ExchangeStoreId/>
   <MemberCorrelationKey/>
   <ExtendedProperties/>
   <SmtpAddress/>
</ImGroup>
```

 <span data-ttu-id="9e4c2-105">**ImGroupType**</span><span class="sxs-lookup"><span data-stu-id="9e4c2-105">**ImGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9e4c2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9e4c2-106">Attributes and elements</span></span>

<span data-ttu-id="9e4c2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e4c2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9e4c2-108">Attributes</span></span>

<span data-ttu-id="9e4c2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9e4c2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9e4c2-110">Child elements</span></span>

<span data-ttu-id="9e4c2-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupType](grouptype.md) | [ExchangeStoreId](exchangestoreid.md) | [MemberCorrelationKey](membercorrelationkey.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)  |  [ SmtpAddress](smtpaddress.md)</span><span class="sxs-lookup"><span data-stu-id="9e4c2-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupType](grouptype.md) | [ExchangeStoreId](exchangestoreid.md) | [MemberCorrelationKey](membercorrelationkey.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md) | [SmtpAddress](smtpaddress.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9e4c2-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9e4c2-112">Parent elements</span></span>

<span data-ttu-id="9e4c2-113">[Grupos (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md) | [AddImGroupResponse](addimgroupresponse.md)</span><span class="sxs-lookup"><span data-stu-id="9e4c2-113">[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md) | [AddImGroupResponse](addimgroupresponse.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e4c2-114">Notas</span><span class="sxs-lookup"><span data-stu-id="9e4c2-114">Remarks</span></span>

<span data-ttu-id="9e4c2-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9e4c2-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e4c2-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9e4c2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e4c2-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9e4c2-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9e4c2-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9e4c2-119">Schema name</span></span>  <br/> |<span data-ttu-id="9e4c2-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9e4c2-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9e4c2-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9e4c2-121">Validation file</span></span>  <br/> |<span data-ttu-id="9e4c2-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9e4c2-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9e4c2-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9e4c2-123">Can be empty</span></span>  <br/> ||
   

