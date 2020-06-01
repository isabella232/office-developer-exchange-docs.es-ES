---
title: Desagrupo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7b884e-ecf1-4e58-86ec-856b13a95f2b
description: El elemento imgroup representa un grupo de mensajería instantánea.
ms.openlocfilehash: a0ff3fcb82e7f18837af5a6f5daa16e90043034d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460690"
---
# <a name="imgroup"></a><span data-ttu-id="f4b60-103">Desagrupo</span><span class="sxs-lookup"><span data-stu-id="f4b60-103">ImGroup</span></span>

<span data-ttu-id="f4b60-104">El elemento **imgroup** representa un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="f4b60-104">The **ImGroup** element represents an instant messaging group.</span></span> 
  
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

 <span data-ttu-id="f4b60-105">**ImGroupType**</span><span class="sxs-lookup"><span data-stu-id="f4b60-105">**ImGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4b60-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f4b60-106">Attributes and elements</span></span>

<span data-ttu-id="f4b60-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f4b60-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4b60-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4b60-108">Attributes</span></span>

<span data-ttu-id="f4b60-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f4b60-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4b60-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4b60-110">Child elements</span></span>

<span data-ttu-id="f4b60-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)  |  [GroupType](grouptype.md)  |  [ExchangeStoreId](exchangestoreid.md)  |  [MemberCorrelationKey](membercorrelationkey.md)  |  [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)  |  [SmtpAddress](smtpaddress.md)</span><span class="sxs-lookup"><span data-stu-id="f4b60-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupType](grouptype.md) | [ExchangeStoreId](exchangestoreid.md) | [MemberCorrelationKey](membercorrelationkey.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md) | [SmtpAddress](smtpaddress.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f4b60-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f4b60-112">Parent elements</span></span>

<span data-ttu-id="f4b60-113">[Grupos (ArrayOfImGroupType)](groups-arrayofimgrouptype.md)  |  [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md)  |  [AddImGroupResponse](addimgroupresponse.md)</span><span class="sxs-lookup"><span data-stu-id="f4b60-113">[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md) | [AddImGroupResponse](addimgroupresponse.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4b60-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4b60-114">Remarks</span></span>

<span data-ttu-id="f4b60-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f4b60-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f4b60-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4b60-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4b60-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f4b60-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4b60-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4b60-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f4b60-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f4b60-119">Schema name</span></span>  <br/> |<span data-ttu-id="f4b60-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f4b60-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f4b60-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f4b60-121">Validation file</span></span>  <br/> |<span data-ttu-id="f4b60-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f4b60-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f4b60-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f4b60-123">Can be empty</span></span>  <br/> ||
   

