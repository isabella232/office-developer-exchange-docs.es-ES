---
title: Read
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Read
api_type:
- schema
ms.assetid: b14637e9-1695-4b7e-b078-ae527c2e4303
description: El elemento Read indica si un cliente puede leer una carpeta o un elemento. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: d75285e0ab14c4f53d73cb7f4349196e07c3c521
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468316"
---
# <a name="read"></a><span data-ttu-id="9585f-104">Read</span><span class="sxs-lookup"><span data-stu-id="9585f-104">Read</span></span>

<span data-ttu-id="9585f-105">El elemento **Read** indica si un cliente puede leer una carpeta o un elemento.</span><span class="sxs-lookup"><span data-stu-id="9585f-105">The **Read** element indicates whether a client can read a folder or item.</span></span> <span data-ttu-id="9585f-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9585f-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Read>true or false</Read>
```

 <span data-ttu-id="9585f-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="9585f-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9585f-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9585f-108">Attributes and elements</span></span>

<span data-ttu-id="9585f-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9585f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9585f-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="9585f-110">Attributes</span></span>

<span data-ttu-id="9585f-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9585f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9585f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9585f-112">Child elements</span></span>

<span data-ttu-id="9585f-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9585f-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9585f-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9585f-114">Parent elements</span></span>

|<span data-ttu-id="9585f-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9585f-115">**Element**</span></span>|<span data-ttu-id="9585f-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9585f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9585f-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="9585f-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="9585f-118">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="9585f-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="9585f-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="9585f-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9585f-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9585f-120">Text value</span></span>

<span data-ttu-id="9585f-121">Un valor de texto de **true** indica que un cliente puede leer un elemento de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="9585f-121">A text value of **true** indicates that a client can read an item of folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9585f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9585f-122">Remarks</span></span>

<span data-ttu-id="9585f-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9585f-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9585f-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9585f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9585f-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="9585f-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9585f-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9585f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="9585f-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9585f-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="9585f-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9585f-128">Validation File</span></span>  <br/> |<span data-ttu-id="9585f-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9585f-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9585f-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9585f-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="9585f-131">Falso</span><span class="sxs-lookup"><span data-stu-id="9585f-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9585f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="9585f-132">See also</span></span>



- [<span data-ttu-id="9585f-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9585f-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="9585f-134">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="9585f-134">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

