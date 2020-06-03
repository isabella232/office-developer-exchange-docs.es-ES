---
title: Modificación
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Modify
api_type:
- schema
ms.assetid: 7a51e9e1-addb-4343-8a22-78f23763c0a8
description: El elemento Modify indica si un cliente puede modificar una carpeta o un elemento. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: e7712644ac9c32afab06be49b438ad83bbb31058
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530418"
---
# <a name="modify"></a><span data-ttu-id="a523e-104">Modificación</span><span class="sxs-lookup"><span data-stu-id="a523e-104">Modify</span></span>

<span data-ttu-id="a523e-105">El elemento **Modify** indica si un cliente puede modificar una carpeta o un elemento.</span><span class="sxs-lookup"><span data-stu-id="a523e-105">The **Modify** element indicates whether a client can modify a folder or item.</span></span> <span data-ttu-id="a523e-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a523e-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Modify>true or false</Modify>
```

 <span data-ttu-id="a523e-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="a523e-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a523e-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a523e-108">Attributes and elements</span></span>

<span data-ttu-id="a523e-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a523e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a523e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="a523e-110">Attributes</span></span>

<span data-ttu-id="a523e-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a523e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a523e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a523e-112">Child elements</span></span>

<span data-ttu-id="a523e-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a523e-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a523e-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a523e-114">Parent elements</span></span>

|<span data-ttu-id="a523e-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a523e-115">**Element**</span></span>|<span data-ttu-id="a523e-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a523e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a523e-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="a523e-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="a523e-118">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="a523e-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="a523e-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="a523e-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a523e-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a523e-120">Text value</span></span>

<span data-ttu-id="a523e-121">Un valor de texto de **true** indica que un cliente puede modificar un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a523e-121">A text value of **true** indicates that a client can modify an item or folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a523e-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a523e-122">Remarks</span></span>

<span data-ttu-id="a523e-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a523e-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a523e-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a523e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a523e-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="a523e-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a523e-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a523e-126">Schema Name</span></span>  <br/> |<span data-ttu-id="a523e-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a523e-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="a523e-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a523e-128">Validation File</span></span>  <br/> |<span data-ttu-id="a523e-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a523e-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a523e-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a523e-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="a523e-131">Falso</span><span class="sxs-lookup"><span data-stu-id="a523e-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a523e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a523e-132">See also</span></span>



- [<span data-ttu-id="a523e-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a523e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="a523e-134">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="a523e-134">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

