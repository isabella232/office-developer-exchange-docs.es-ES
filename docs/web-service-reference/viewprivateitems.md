---
title: ViewPrivateItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ViewPrivateItems
api_type:
- schema
ms.assetid: 80b949ac-440c-4a01-b428-ebafb5b1b802
description: El elemento ViewPrivateItems indica si un usuario delegado o una aplicación cliente tiene permiso para ver elementos privados en el buzón de la entidad de la identidad.
ms.openlocfilehash: 4e1375f7c4a3c660cc5de885deff8d094250ca7b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44525972"
---
# <a name="viewprivateitems"></a><span data-ttu-id="6e41b-103">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="6e41b-103">ViewPrivateItems</span></span>

<span data-ttu-id="6e41b-104">El elemento **ViewPrivateItems** indica si un usuario delegado o una aplicación cliente tiene permiso para ver elementos privados en el buzón de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="6e41b-104">The **ViewPrivateItems** element indicates whether a delegate user or client application has permission to view private items in the principal's mailbox.</span></span> 
  
```XML
<ViewPrivateItems>true | false</ViewPrivateItems>
```

 <span data-ttu-id="6e41b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6e41b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6e41b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6e41b-106">Attributes and elements</span></span>

<span data-ttu-id="6e41b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6e41b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e41b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6e41b-108">Attributes</span></span>

<span data-ttu-id="6e41b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6e41b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e41b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6e41b-110">Child elements</span></span>

<span data-ttu-id="6e41b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6e41b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6e41b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6e41b-112">Parent elements</span></span>

|<span data-ttu-id="6e41b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6e41b-113">**Element**</span></span>|<span data-ttu-id="6e41b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e41b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e41b-115">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="6e41b-115">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="6e41b-116">Identifica un único delegado para agregar o actualizar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="6e41b-116">Identifies a single delegate to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6e41b-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="6e41b-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="6e41b-118">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="6e41b-118">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="6e41b-119">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="6e41b-119">This element is read-only.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6e41b-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6e41b-120">Text value</span></span>

<span data-ttu-id="6e41b-121">Un valor de **true** indica que el delegado o el cliente puede ver los elementos privados en el buzón de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="6e41b-121">A value of **true** indicates that the delegate or client can view private items in the principal's mailbox.</span></span> <span data-ttu-id="6e41b-122">Un valor de **false** indica que los elementos privados no son visibles para un delegado o un cliente.</span><span class="sxs-lookup"><span data-stu-id="6e41b-122">A value of **false** indicates that private items are not visible to a delegate or client.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6e41b-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e41b-123">Remarks</span></span>

<span data-ttu-id="6e41b-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6e41b-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e41b-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6e41b-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e41b-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e41b-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6e41b-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6e41b-127">Schema Name</span></span>  <br/> |<span data-ttu-id="6e41b-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6e41b-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="6e41b-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6e41b-129">Validation File</span></span>  <br/> |<span data-ttu-id="6e41b-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6e41b-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6e41b-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6e41b-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="6e41b-132">Falso</span><span class="sxs-lookup"><span data-stu-id="6e41b-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e41b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e41b-133">See also</span></span>



[<span data-ttu-id="6e41b-134">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="6e41b-134">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="6e41b-135">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="6e41b-135">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="6e41b-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6e41b-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6e41b-137">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="6e41b-137">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

