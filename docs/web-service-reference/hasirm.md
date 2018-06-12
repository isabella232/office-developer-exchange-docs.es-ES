---
title: HasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fedc04e0-cfd2-4652-a2a8-51de859ae847
description: El elemento HasIrm especifica si al menos un mensaje en la conversación y la carpeta actual es un mensaje protegido de IRM.
ms.openlocfilehash: c129370d7920da7cf1f9f32eed2f075e6c21cf8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835803"
---
# <a name="hasirm"></a><span data-ttu-id="43fa6-103">HasIrm</span><span class="sxs-lookup"><span data-stu-id="43fa6-103">HasIrm</span></span>

<span data-ttu-id="43fa6-104">El elemento **HasIrm** especifica si al menos un mensaje en la conversación y la carpeta actual es un mensaje protegido de IRM.</span><span class="sxs-lookup"><span data-stu-id="43fa6-104">The **HasIrm** element specifies whether at least one message in the conversation and the current folder is an IRM protected message.</span></span> 
  
```XML
<HasIrm> true | false </HasIrm>
```

 <span data-ttu-id="43fa6-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="43fa6-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43fa6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="43fa6-106">Attributes and elements</span></span>

<span data-ttu-id="43fa6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="43fa6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43fa6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="43fa6-108">Attributes</span></span>

<span data-ttu-id="43fa6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="43fa6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43fa6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="43fa6-110">Child elements</span></span>

<span data-ttu-id="43fa6-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="43fa6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43fa6-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="43fa6-112">Parent elements</span></span>

[<span data-ttu-id="43fa6-113">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="43fa6-113">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
## <a name="text-value"></a><span data-ttu-id="43fa6-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="43fa6-114">Text value</span></span>

<span data-ttu-id="43fa6-115">El valor de texto del elemento **HasIrm** es **true** si al menos un mensaje en la conversación y la carpeta actual tiene IRM.</span><span class="sxs-lookup"><span data-stu-id="43fa6-115">The text value of the **HasIrm** element is **true** if at least one message in the conversation and the current folder has IRM.</span></span> <span data-ttu-id="43fa6-116">De lo contrario, el valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="43fa6-116">Otherwise, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43fa6-117">Notas</span><span class="sxs-lookup"><span data-stu-id="43fa6-117">Remarks</span></span>

<span data-ttu-id="43fa6-118">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="43fa6-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="43fa6-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="43fa6-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43fa6-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="43fa6-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43fa6-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="43fa6-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43fa6-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="43fa6-122">Schema Name</span></span>  <br/> |<span data-ttu-id="43fa6-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="43fa6-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="43fa6-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="43fa6-124">Validation File</span></span>  <br/> |<span data-ttu-id="43fa6-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="43fa6-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43fa6-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="43fa6-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="43fa6-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="43fa6-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43fa6-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="43fa6-128">See also</span></span>



[<span data-ttu-id="43fa6-129">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="43fa6-129">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)


- [<span data-ttu-id="43fa6-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="43fa6-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

