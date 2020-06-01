---
title: ProgrammaticAccessAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a1fc7dff-a303-4809-b7f4-9672f86c183c
description: El elemento ProgrammaticAccessAllowed especifica si el acceso mediante programación está habilitado para los datos con derechos administrados.
ms.openlocfilehash: 8a5cf4e57a97807e5940a0402768d7123b9912d2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465642"
---
# <a name="programmaticaccessallowed"></a><span data-ttu-id="1c4df-103">ProgrammaticAccessAllowed</span><span class="sxs-lookup"><span data-stu-id="1c4df-103">ProgrammaticAccessAllowed</span></span>

<span data-ttu-id="1c4df-104">El elemento **ProgrammaticAccessAllowed** especifica si el acceso mediante programación está habilitado para los datos con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="1c4df-104">The **ProgrammaticAccessAllowed** element specifies whether programmatic access is enabled for rights managed data.</span></span> 
  
```XML
<ProgrammaticAccessAllowed> true | false </ProgrammaticAccessAllowed>
```

 <span data-ttu-id="1c4df-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1c4df-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c4df-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1c4df-106">Attributes and elements</span></span>

<span data-ttu-id="1c4df-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1c4df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c4df-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1c4df-108">Attributes</span></span>

<span data-ttu-id="1c4df-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1c4df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c4df-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1c4df-110">Child elements</span></span>

<span data-ttu-id="1c4df-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1c4df-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1c4df-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1c4df-112">Parent elements</span></span>

[<span data-ttu-id="1c4df-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="1c4df-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="1c4df-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1c4df-114">Text value</span></span>

<span data-ttu-id="1c4df-115">Un valor de texto de **true** para el elemento **ProgrammaticAccessAllowed** indica que se puede obtener acceso A los datos mediante programación.</span><span class="sxs-lookup"><span data-stu-id="1c4df-115">A text value of **true** for the **ProgrammaticAccessAllowed** element indicates that the data is programmatically accessible.</span></span> <span data-ttu-id="1c4df-116">Un valor de **false** indica que no se puede tener acceso A los datos mediante programación.</span><span class="sxs-lookup"><span data-stu-id="1c4df-116">A value of **false** indicates that the data is not programmatically accessible.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1c4df-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c4df-117">Remarks</span></span>

<span data-ttu-id="1c4df-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1c4df-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1c4df-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1c4df-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c4df-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1c4df-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c4df-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c4df-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1c4df-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1c4df-122">Schema name</span></span>  <br/> |<span data-ttu-id="1c4df-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1c4df-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="1c4df-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1c4df-124">Validation file</span></span>  <br/> |<span data-ttu-id="1c4df-125">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1c4df-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1c4df-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1c4df-126">Can be empty</span></span>  <br/> |<span data-ttu-id="1c4df-127">false</span><span class="sxs-lookup"><span data-stu-id="1c4df-127">false</span></span>  <br/> |
   

