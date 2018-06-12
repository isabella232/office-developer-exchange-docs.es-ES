---
title: AddNewTelUriContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cff8ef19-3e19-4107-9b35-c8a2b87a41bc
description: El elemento AddNewTelUriContactToGroup especifica los datos de entrada para la operación WSDL AddNewTelUriContactToGroup.
ms.openlocfilehash: d99d557530397aa9edd2c23b595bdcb348783dd4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763408"
---
# <a name="addnewteluricontacttogroup"></a><span data-ttu-id="aa362-103">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="aa362-103">AddNewTelUriContactToGroup</span></span>

<span data-ttu-id="aa362-104">El elemento **AddNewTelUriContactToGroup** especifica los datos de entrada para la operación de WSDL **AddNewTelUriContactToGroup** .</span><span class="sxs-lookup"><span data-stu-id="aa362-104">The **AddNewTelUriContactToGroup** element specifies the input data for the **AddNewTelUriContactToGroup** WSDL operation.</span></span> 
  
```XML
<AddNewTelUriContactToGroup>
   <TelUriAddress/>
   <ImContactSipUriAddress/>
   <ImTelephoneNumber/>
   <GroupId/>
</AddNewTelUriContactToGroup>
```

 <span data-ttu-id="aa362-105">**AddNewTelUriContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="aa362-105">**AddNewTelUriContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa362-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aa362-106">Attributes and elements</span></span>

<span data-ttu-id="aa362-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aa362-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa362-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aa362-108">Attributes</span></span>

<span data-ttu-id="aa362-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aa362-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa362-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aa362-110">Child elements</span></span>

<span data-ttu-id="aa362-111">[TelUriAddress](teluriaddress.md) | [ImContactSipUriAddress](imcontactsipuriaddress.md) | [ImTelephoneNumber](imtelephonenumber.md) | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="aa362-111">[TelUriAddress](teluriaddress.md) | [ImContactSipUriAddress](imcontactsipuriaddress.md) | [ImTelephoneNumber](imtelephonenumber.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aa362-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aa362-112">Parent elements</span></span>

<span data-ttu-id="aa362-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aa362-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa362-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa362-114">Remarks</span></span>

<span data-ttu-id="aa362-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aa362-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="aa362-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa362-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa362-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aa362-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa362-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aa362-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aa362-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aa362-119">Schema name</span></span>  <br/> |<span data-ttu-id="aa362-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="aa362-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="aa362-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aa362-121">Validation file</span></span>  <br/> |<span data-ttu-id="aa362-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="aa362-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aa362-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aa362-123">Can be empty</span></span>  <br/> |<span data-ttu-id="aa362-124">False</span><span class="sxs-lookup"><span data-stu-id="aa362-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa362-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="aa362-125">See also</span></span>

- [<span data-ttu-id="aa362-126">Operación AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="aa362-126">AddNewTelUriContactToGroup operation</span></span>](addnewteluricontacttogroup-operation.md)
- [<span data-ttu-id="aa362-127">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="aa362-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

