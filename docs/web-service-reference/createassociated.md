---
title: CreateAssociated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAssociated
api_type:
- schema
ms.assetid: 742a6136-6015-4924-bae4-f3868127e966
description: El elemento CreateAssociated indica si un cliente puede crear una tabla de contenido asociada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: e88d7670fd9ef848221dab8cc145395bcb11e5bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460795"
---
# <a name="createassociated"></a><span data-ttu-id="63221-104">CreateAssociated</span><span class="sxs-lookup"><span data-stu-id="63221-104">CreateAssociated</span></span>

<span data-ttu-id="63221-105">El elemento **CreateAssociated** indica si un cliente puede crear una tabla de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="63221-105">The **CreateAssociated** element indicates whether a client can create an associated contents table.</span></span> <span data-ttu-id="63221-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="63221-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CreateAssociated>true or false</CreateAssociated>
```

 <span data-ttu-id="63221-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="63221-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63221-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="63221-108">Attributes and elements</span></span>

<span data-ttu-id="63221-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="63221-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63221-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="63221-110">Attributes</span></span>

<span data-ttu-id="63221-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="63221-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63221-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="63221-112">Child elements</span></span>

<span data-ttu-id="63221-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="63221-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="63221-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="63221-114">Parent elements</span></span>

|<span data-ttu-id="63221-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="63221-115">**Element**</span></span>|<span data-ttu-id="63221-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63221-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63221-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="63221-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="63221-118">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="63221-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="63221-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="63221-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="63221-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="63221-120">Text value</span></span>

<span data-ttu-id="63221-121">Un valor de texto de **true** indica que un cliente puede crear una tabla de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="63221-121">A text value of **true** indicates that a client can create an associated contents table.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="63221-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63221-122">Remarks</span></span>

<span data-ttu-id="63221-123">Esta propiedad solo se usa en objetos Folder.</span><span class="sxs-lookup"><span data-stu-id="63221-123">This property is only used on folder objects.</span></span>
  
<span data-ttu-id="63221-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="63221-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63221-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="63221-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63221-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="63221-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="63221-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="63221-127">Schema Name</span></span>  <br/> |<span data-ttu-id="63221-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="63221-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="63221-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="63221-129">Validation File</span></span>  <br/> |<span data-ttu-id="63221-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="63221-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="63221-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="63221-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="63221-132">Falso</span><span class="sxs-lookup"><span data-stu-id="63221-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63221-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="63221-133">See also</span></span>



- [<span data-ttu-id="63221-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="63221-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="63221-135">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="63221-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

