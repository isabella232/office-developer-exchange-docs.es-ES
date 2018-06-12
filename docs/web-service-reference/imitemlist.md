---
title: ImItemList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 556457d5-a730-4131-853f-1198c27c5942
description: El elemento ImItemList contiene una lista de contactos de mensajería instantánea y de grupos de mensajería instantáneos.
ms.openlocfilehash: 490ac57da0c7ae7bedc75e94b7e21dc30c9da23f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835896"
---
# <a name="imitemlist"></a><span data-ttu-id="34064-103">ImItemList</span><span class="sxs-lookup"><span data-stu-id="34064-103">ImItemList</span></span>

<span data-ttu-id="34064-104">El elemento **ImItemList** contiene una lista de contactos de mensajería instantánea y de grupos de mensajería instantáneos.</span><span class="sxs-lookup"><span data-stu-id="34064-104">The **ImItemList** element contains a list of instant messaging groups and instant messaging contacts.</span></span> 
  
```XML
<ImItemList>
   <Groups/>
   <Personas/>
</ImItemList>
```

 <span data-ttu-id="34064-105">**ImItemListType**</span><span class="sxs-lookup"><span data-stu-id="34064-105">**ImItemListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="34064-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="34064-106">Attributes and elements</span></span>

<span data-ttu-id="34064-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="34064-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34064-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="34064-108">Attributes</span></span>

<span data-ttu-id="34064-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="34064-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34064-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="34064-110">Child elements</span></span>

<span data-ttu-id="34064-111">[Grupos (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [roles](personas-ex15websvcsotherref.md)</span><span class="sxs-lookup"><span data-stu-id="34064-111">[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [Personas](personas-ex15websvcsotherref.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="34064-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="34064-112">Parent elements</span></span>

<span data-ttu-id="34064-113">[GetImItemsResponse](getimitemsresponse.md) | [GetImItemListResponse](getimitemlistresponse.md)</span><span class="sxs-lookup"><span data-stu-id="34064-113">[GetImItemsResponse](getimitemsresponse.md) | [GetImItemListResponse](getimitemlistresponse.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="34064-114">Notas</span><span class="sxs-lookup"><span data-stu-id="34064-114">Remarks</span></span>

<span data-ttu-id="34064-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34064-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="34064-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="34064-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34064-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="34064-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34064-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="34064-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="34064-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="34064-119">Schema name</span></span>  <br/> |<span data-ttu-id="34064-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="34064-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="34064-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="34064-121">Validation file</span></span>  <br/> |<span data-ttu-id="34064-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="34064-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="34064-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="34064-123">Can be empty</span></span>  <br/> ||
   

