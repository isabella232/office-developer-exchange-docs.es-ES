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
description: El elemento DistinguishedUser identifica cuentas de usuario anónimas y predeterminadas para el acceso delegado. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 922c36251290d7090cdafbed9e570144593ca97e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530736"
---
# <a name="distinguisheduser"></a><span data-ttu-id="599e3-104">DistinguishedUser</span><span class="sxs-lookup"><span data-stu-id="599e3-104">DistinguishedUser</span></span>

<span data-ttu-id="599e3-105">El elemento **DistinguishedUser** identifica cuentas de usuario anónimas y predeterminadas para el acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="599e3-105">The **DistinguishedUser** element identifies Anonymous and Default user accounts for delegate access.</span></span> <span data-ttu-id="599e3-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="599e3-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DistinguishedUser>Default or Anonymous</DistinguishedUser>
```

 <span data-ttu-id="599e3-107">**DistinguishedUserType**</span><span class="sxs-lookup"><span data-stu-id="599e3-107">**DistinguishedUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="599e3-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="599e3-108">Attributes and elements</span></span>

<span data-ttu-id="599e3-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="599e3-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="599e3-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="599e3-110">Attributes</span></span>

<span data-ttu-id="599e3-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="599e3-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="599e3-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="599e3-112">Child elements</span></span>

<span data-ttu-id="599e3-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="599e3-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="599e3-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="599e3-114">Parent elements</span></span>

|<span data-ttu-id="599e3-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="599e3-115">**Element**</span></span>|<span data-ttu-id="599e3-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="599e3-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="599e3-117">UserId</span><span class="sxs-lookup"><span data-stu-id="599e3-117">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="599e3-118">Identifica un usuario delegado o un usuario que tiene permisos de acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="599e3-118">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="599e3-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="599e3-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="599e3-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="599e3-120">Text value</span></span>

<span data-ttu-id="599e3-121">Un valor de texto **predeterminado** describe la configuración predeterminada para los usuarios delegados que se agregan al buzón de la entidad de identidad.</span><span class="sxs-lookup"><span data-stu-id="599e3-121">A text value of **Default** describes the default setting for delegate users who are added to the principal's mailbox.</span></span> <span data-ttu-id="599e3-122">Un valor de texto de **anónimo** describe la configuración de acceso delegado que los usuarios anónimos tienen en el buzón de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="599e3-122">A text value of **Anonymous** describes the delegate access settings that anonymous users have on the principal's mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="599e3-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="599e3-123">Remarks</span></span>

<span data-ttu-id="599e3-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="599e3-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="599e3-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="599e3-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="599e3-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="599e3-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="599e3-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="599e3-127">Schema Name</span></span>  <br/> |<span data-ttu-id="599e3-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="599e3-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="599e3-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="599e3-129">Validation File</span></span>  <br/> |<span data-ttu-id="599e3-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="599e3-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="599e3-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="599e3-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="599e3-132">Falso</span><span class="sxs-lookup"><span data-stu-id="599e3-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="599e3-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="599e3-133">See also</span></span>

- [<span data-ttu-id="599e3-134">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="599e3-134">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="599e3-135">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="599e3-135">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="599e3-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="599e3-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="599e3-137">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="599e3-137">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

