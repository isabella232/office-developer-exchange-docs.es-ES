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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460690"
---
# <a name="imgroup"></a><span data-ttu-id="1df52-103">Desagrupo</span><span class="sxs-lookup"><span data-stu-id="1df52-103">ImGroup</span></span>

<span data-ttu-id="1df52-104">El elemento **imgroup** representa un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="1df52-104">The **ImGroup** element represents an instant messaging group.</span></span> 
  
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

 <span data-ttu-id="1df52-105">**ImGroupType**</span><span class="sxs-lookup"><span data-stu-id="1df52-105">**ImGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1df52-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1df52-106">Attributes and elements</span></span>

<span data-ttu-id="1df52-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1df52-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1df52-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1df52-108">Attributes</span></span>

<span data-ttu-id="1df52-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1df52-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1df52-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1df52-110">Child elements</span></span>

<span data-ttu-id="1df52-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)  |  [GroupType](grouptype.md)  |  [ExchangeStoreId](exchangestoreid.md)  |  [MemberCorrelationKey](membercorrelationkey.md)  |  [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)  |  [SmtpAddress](smtpaddress.md)</span><span class="sxs-lookup"><span data-stu-id="1df52-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupType](grouptype.md) | [ExchangeStoreId](exchangestoreid.md) | [MemberCorrelationKey](membercorrelationkey.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md) | [SmtpAddress](smtpaddress.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1df52-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1df52-112">Parent elements</span></span>

<span data-ttu-id="1df52-113">[Grupos (ArrayOfImGroupType)](groups-arrayofimgrouptype.md)  |  [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md)  |  [AddImGroupResponse](addimgroupresponse.md)</span><span class="sxs-lookup"><span data-stu-id="1df52-113">[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md) | [AddImGroupResponse](addimgroupresponse.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1df52-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1df52-114">Remarks</span></span>

<span data-ttu-id="1df52-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1df52-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1df52-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1df52-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1df52-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1df52-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1df52-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="1df52-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1df52-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1df52-119">Schema name</span></span>  <br/> |<span data-ttu-id="1df52-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1df52-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1df52-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1df52-121">Validation file</span></span>  <br/> |<span data-ttu-id="1df52-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1df52-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1df52-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1df52-123">Can be empty</span></span>  <br/> ||
   

