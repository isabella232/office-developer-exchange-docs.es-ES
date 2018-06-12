---
title: DistinguishedUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedUser
api_type:
- schema
ms.assetid: 9362699d-666a-4acf-8fa1-c6669f0a2ae5
description: El elemento DistinguishedUser identifica las cuentas de usuario anónimo y predeterminado para el acceso de delegado. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: b14be22bfe5316b9ab254e63cdfa0757596b8b92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764247"
---
# <a name="distinguisheduser"></a><span data-ttu-id="7c04c-104">DistinguishedUser</span><span class="sxs-lookup"><span data-stu-id="7c04c-104">DistinguishedUser</span></span>

<span data-ttu-id="7c04c-105">El elemento **DistinguishedUser** identifica las cuentas de usuario anónimo y predeterminado para el acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="7c04c-105">The **DistinguishedUser** element identifies Anonymous and Default user accounts for delegate access.</span></span> <span data-ttu-id="7c04c-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7c04c-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DistinguishedUser>Default or Anonymous</DistinguishedUser>
```

 <span data-ttu-id="7c04c-107">**DistinguishedUserType**</span><span class="sxs-lookup"><span data-stu-id="7c04c-107">**DistinguishedUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7c04c-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7c04c-108">Attributes and elements</span></span>

<span data-ttu-id="7c04c-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7c04c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c04c-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="7c04c-110">Attributes</span></span>

<span data-ttu-id="7c04c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7c04c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c04c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7c04c-112">Child elements</span></span>

<span data-ttu-id="7c04c-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7c04c-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7c04c-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7c04c-114">Parent elements</span></span>

|<span data-ttu-id="7c04c-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c04c-115">**Element**</span></span>|<span data-ttu-id="7c04c-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c04c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c04c-117">UserId</span><span class="sxs-lookup"><span data-stu-id="7c04c-117">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="7c04c-118">Identifica un usuario delegado o un usuario que tiene permisos de acceso de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7c04c-118">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="7c04c-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="7c04c-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7c04c-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7c04c-120">Text value</span></span>

<span data-ttu-id="7c04c-121">Un valor de texto de **forma predeterminada** , describe la configuración predeterminada para los usuarios de delegado que se agregan al buzón de correo de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7c04c-121">A text value of **Default** describes the default setting for delegate users who are added to the principal's mailbox.</span></span> <span data-ttu-id="7c04c-122">Un valor de texto de **anónimo** describe la configuración de acceso de delegado que tienen los usuarios anónimos en el buzón de correo de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7c04c-122">A text value of **Anonymous** describes the delegate access settings that anonymous users have on the principal's mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7c04c-123">Notas</span><span class="sxs-lookup"><span data-stu-id="7c04c-123">Remarks</span></span>

<span data-ttu-id="7c04c-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7c04c-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c04c-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7c04c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c04c-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7c04c-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7c04c-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7c04c-127">Schema Name</span></span>  <br/> |<span data-ttu-id="7c04c-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7c04c-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="7c04c-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7c04c-129">Validation File</span></span>  <br/> |<span data-ttu-id="7c04c-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7c04c-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7c04c-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7c04c-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="7c04c-132">False</span><span class="sxs-lookup"><span data-stu-id="7c04c-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c04c-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="7c04c-133">See also</span></span>

- [<span data-ttu-id="7c04c-134">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="7c04c-134">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="7c04c-135">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="7c04c-135">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="7c04c-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7c04c-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="7c04c-137">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="7c04c-137">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

