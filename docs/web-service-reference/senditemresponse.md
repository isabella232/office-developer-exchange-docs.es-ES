---
title: SendItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItemResponse
api_type:
- schema
ms.assetid: 26ac41c7-57d9-473e-ab7a-bae93e1d2aba
description: El elemento SendItemResponse define una respuesta a una solicitud SendItem.
ms.openlocfilehash: dd90510547c3db8c3531663c23d05055bd774fab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462132"
---
# <a name="senditemresponse"></a><span data-ttu-id="09236-103">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="09236-103">SendItemResponse</span></span>

<span data-ttu-id="09236-104">El elemento **SendItemResponse** define una respuesta a una solicitud SendItem.</span><span class="sxs-lookup"><span data-stu-id="09236-104">The **SendItemResponse** element defines a response to a SendItem request.</span></span> 
  
```xml
<SendItemResponse>
   <ResponseMessages/>
</SendItemResponse>
```

 <span data-ttu-id="09236-105">**SendItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="09236-105">**SendItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09236-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="09236-106">Attributes and elements</span></span>

<span data-ttu-id="09236-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="09236-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09236-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="09236-108">Attributes</span></span>

<span data-ttu-id="09236-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="09236-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09236-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="09236-110">Child elements</span></span>

|<span data-ttu-id="09236-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="09236-111">**Element**</span></span>|<span data-ttu-id="09236-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="09236-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09236-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="09236-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="09236-114">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="09236-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="09236-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="09236-115">Parent elements</span></span>

<span data-ttu-id="09236-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="09236-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09236-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09236-117">Remarks</span></span>

<span data-ttu-id="09236-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="09236-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09236-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="09236-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09236-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="09236-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="09236-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="09236-121">Schema name</span></span>  <br/> |<span data-ttu-id="09236-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="09236-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="09236-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="09236-123">Validation file</span></span>  <br/> |<span data-ttu-id="09236-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="09236-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="09236-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="09236-125">Can be empty</span></span>  <br/> |<span data-ttu-id="09236-126">Falso</span><span class="sxs-lookup"><span data-stu-id="09236-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09236-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="09236-127">See also</span></span>



[<span data-ttu-id="09236-128">Operación SendItem</span><span class="sxs-lookup"><span data-stu-id="09236-128">SendItem operation</span></span>](senditem-operation.md)
  
[<span data-ttu-id="09236-129">SendItem</span><span class="sxs-lookup"><span data-stu-id="09236-129">SendItem</span></span>](senditem.md)


- [<span data-ttu-id="09236-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="09236-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

