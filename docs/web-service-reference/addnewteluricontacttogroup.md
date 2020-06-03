---
title: AddNewTelUriContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cff8ef19-3e19-4107-9b35-c8a2b87a41bc
description: El elemento AddNewTelUriContactToGroup especifica los datos de entrada para la operación WSDL de AddNewTelUriContactToGroup.
ms.openlocfilehash: 151c5b1dab7a3ffc9630fb4e4192b90bd1d4ae38
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464934"
---
# <a name="addnewteluricontacttogroup"></a><span data-ttu-id="a570e-103">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="a570e-103">AddNewTelUriContactToGroup</span></span>

<span data-ttu-id="a570e-104">El elemento **AddNewTelUriContactToGroup** especifica los datos de entrada para la operación WSDL de **AddNewTelUriContactToGroup** .</span><span class="sxs-lookup"><span data-stu-id="a570e-104">The **AddNewTelUriContactToGroup** element specifies the input data for the **AddNewTelUriContactToGroup** WSDL operation.</span></span> 
  
```XML
<AddNewTelUriContactToGroup>
   <TelUriAddress/>
   <ImContactSipUriAddress/>
   <ImTelephoneNumber/>
   <GroupId/>
</AddNewTelUriContactToGroup>
```

 <span data-ttu-id="a570e-105">**AddNewTelUriContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="a570e-105">**AddNewTelUriContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a570e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a570e-106">Attributes and elements</span></span>

<span data-ttu-id="a570e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a570e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a570e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a570e-108">Attributes</span></span>

<span data-ttu-id="a570e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a570e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a570e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a570e-110">Child elements</span></span>

<span data-ttu-id="a570e-111">[TelUriAddress](teluriaddress.md)  |  [ImContactSipUriAddress](imcontactsipuriaddress.md)  |  [ImTelephoneNumber](imtelephonenumber.md)  |  [GROUPID](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="a570e-111">[TelUriAddress](teluriaddress.md) | [ImContactSipUriAddress](imcontactsipuriaddress.md) | [ImTelephoneNumber](imtelephonenumber.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a570e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a570e-112">Parent elements</span></span>

<span data-ttu-id="a570e-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a570e-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a570e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a570e-114">Remarks</span></span>

<span data-ttu-id="a570e-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a570e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a570e-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a570e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a570e-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a570e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a570e-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a570e-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a570e-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a570e-119">Schema name</span></span>  <br/> |<span data-ttu-id="a570e-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a570e-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a570e-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a570e-121">Validation file</span></span>  <br/> |<span data-ttu-id="a570e-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a570e-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a570e-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a570e-123">Can be empty</span></span>  <br/> |<span data-ttu-id="a570e-124">Falso</span><span class="sxs-lookup"><span data-stu-id="a570e-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a570e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a570e-125">See also</span></span>

- [<span data-ttu-id="a570e-126">Operación AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="a570e-126">AddNewTelUriContactToGroup operation</span></span>](addnewteluricontacttogroup-operation.md)
- [<span data-ttu-id="a570e-127">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a570e-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

