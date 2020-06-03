---
title: DeleteUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteUserConfiguration
api_type:
- schema
ms.assetid: 91b18b6a-d904-476c-996d-b041e859da1e
description: El elemento DeleteUserConfiguration representa una solicitud para eliminar un objeto de configuración de usuario.
ms.openlocfilehash: 04668ead48e7c321ed7e91cbbeb67c6154c02283
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460760"
---
# <a name="deleteuserconfiguration"></a><span data-ttu-id="d7f09-103">DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7f09-103">DeleteUserConfiguration</span></span>

<span data-ttu-id="d7f09-104">El elemento **DeleteUserConfiguration** representa una solicitud para eliminar un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="d7f09-104">The **DeleteUserConfiguration** element represents a request to delete a user configuration object.</span></span> 
  
```xml
<DeleteUserConfiguration>
   <UserConfigurationName/>
</DeleteUserConfiguration>
```

 <span data-ttu-id="d7f09-105">**DeleteUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="d7f09-105">**DeleteUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7f09-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d7f09-106">Attributes and elements</span></span>

<span data-ttu-id="d7f09-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d7f09-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7f09-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7f09-108">Attributes</span></span>

<span data-ttu-id="d7f09-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d7f09-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7f09-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7f09-110">Child elements</span></span>

|<span data-ttu-id="d7f09-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d7f09-111">**Element**</span></span>|<span data-ttu-id="d7f09-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7f09-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7f09-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d7f09-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="d7f09-114">Representa el nombre del objeto de configuración de usuario que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="d7f09-114">Represents the name of the user configuration object to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d7f09-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d7f09-115">Parent elements</span></span>

<span data-ttu-id="d7f09-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d7f09-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d7f09-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d7f09-117">Text value</span></span>

<span data-ttu-id="d7f09-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d7f09-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7f09-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7f09-119">Remarks</span></span>

<span data-ttu-id="d7f09-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7f09-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7f09-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d7f09-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7f09-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7f09-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d7f09-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d7f09-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d7f09-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d7f09-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d7f09-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d7f09-125">Validation File</span></span>  <br/> |<span data-ttu-id="d7f09-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d7f09-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d7f09-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d7f09-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d7f09-128">Falso</span><span class="sxs-lookup"><span data-stu-id="d7f09-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7f09-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7f09-129">See also</span></span>

- [<span data-ttu-id="d7f09-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d7f09-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

