---
title: MustDisplayComment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MustDisplayComment
api_type:
- schema
ms.assetid: 11d4d3c3-4652-4ed4-9b29-a0b5f85b82b7
description: El elemento MustDisplayComment indica si se debe mostrar el comentario de la carpeta administrada.
ms.openlocfilehash: e86b0c6e2c1d7c3cc00561c17c82b3be82d81242
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463212"
---
# <a name="mustdisplaycomment"></a><span data-ttu-id="cc285-103">MustDisplayComment</span><span class="sxs-lookup"><span data-stu-id="cc285-103">MustDisplayComment</span></span>

<span data-ttu-id="cc285-104">El elemento **MustDisplayComment** indica si se debe mostrar el comentario de la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="cc285-104">The **MustDisplayComment** element indicates whether the managed folder comment must be displayed.</span></span> 
  
```xml
<MustDisplayComment/>
```

 <span data-ttu-id="cc285-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cc285-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cc285-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cc285-106">Attributes and elements</span></span>

<span data-ttu-id="cc285-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cc285-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc285-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc285-108">Attributes</span></span>

<span data-ttu-id="cc285-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cc285-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc285-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc285-110">Child elements</span></span>

<span data-ttu-id="cc285-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cc285-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cc285-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cc285-112">Parent elements</span></span>

|<span data-ttu-id="cc285-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc285-113">**Element**</span></span>|<span data-ttu-id="cc285-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc285-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc285-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="cc285-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="cc285-116">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="cc285-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cc285-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cc285-117">Text value</span></span>

<span data-ttu-id="cc285-118">El valor de texto representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="cc285-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="cc285-119">Un valor de **true** indica que se debe mostrar el comentario; un valor de **false** indica que no es necesario mostrar el comentario.</span><span class="sxs-lookup"><span data-stu-id="cc285-119">A value of **true** indicates that the comment must be displayed; a value of **false** indicates that the comment does not have to be displayed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cc285-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc285-120">Remarks</span></span>

<span data-ttu-id="cc285-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="cc285-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc285-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cc285-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc285-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc285-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cc285-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cc285-124">Schema name</span></span>  <br/> |<span data-ttu-id="cc285-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cc285-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="cc285-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cc285-126">Validation file</span></span>  <br/> |<span data-ttu-id="cc285-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cc285-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cc285-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cc285-128">Can be empty</span></span>  <br/> |<span data-ttu-id="cc285-129">Falso</span><span class="sxs-lookup"><span data-stu-id="cc285-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc285-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc285-130">See also</span></span>



[<span data-ttu-id="cc285-131">Operación CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="cc285-131">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="cc285-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cc285-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

