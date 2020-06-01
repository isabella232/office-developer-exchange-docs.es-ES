---
title: Representante
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agent
api_type:
- schema
ms.assetid: 0bf744a5-9d79-4c82-8ea7-45fdb3f55300
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: a810bb229015054e0f244773760235114655a982
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455684"
---
# <a name="agent"></a><span data-ttu-id="bb72a-103">Representante</span><span class="sxs-lookup"><span data-stu-id="bb72a-103">agent</span></span>
  
<span data-ttu-id="bb72a-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb72a-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="bb72a-105">El elemento **Agent** contiene información de configuración sobre un agente instalado.</span><span class="sxs-lookup"><span data-stu-id="bb72a-105">The **agent** element contains configuration information about an installed agent.</span></span> 
  
- [<span data-ttu-id="bb72a-106">configuración</span><span class="sxs-lookup"><span data-stu-id="bb72a-106">configuration</span></span>](configuration.md) 
- [<span data-ttu-id="bb72a-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="bb72a-107">mexRuntime</span></span>](mexruntime.md)
- [<span data-ttu-id="bb72a-108">agentList</span><span class="sxs-lookup"><span data-stu-id="bb72a-108">agentList</span></span>](agentlist.md)
- [<span data-ttu-id="bb72a-109">Representante</span><span class="sxs-lookup"><span data-stu-id="bb72a-109">agent</span></span>](agent.md)
  
```XML
<agent
        name=""
        baseType=""
        classFactory=""
        assemblyPath=""
        enabled="" />
</agent>
```

<span data-ttu-id="bb72a-110">**agentType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="bb72a-110">**agentType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bb72a-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bb72a-111">Attributes and elements</span></span>

<span data-ttu-id="bb72a-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bb72a-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb72a-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb72a-113">Attributes</span></span>

|<span data-ttu-id="bb72a-114">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bb72a-114">**Attribute**</span></span>|<span data-ttu-id="bb72a-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb72a-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb72a-116">**nombre**</span><span class="sxs-lookup"><span data-stu-id="bb72a-116">**name**</span></span> <br/> |<span data-ttu-id="bb72a-117">El nombre que se especificó cuando se instaló el agente.</span><span class="sxs-lookup"><span data-stu-id="bb72a-117">The name that was specified when the agent was installed.</span></span> <span data-ttu-id="bb72a-118">Este atributo requiere un valor de cadena no vacío que contenga un máximo de 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bb72a-118">This attribute requires a nonempty string value that contains a maximum of 64 characters.</span></span>  <br/> |
|<span data-ttu-id="bb72a-119">**baseType**</span><span class="sxs-lookup"><span data-stu-id="bb72a-119">**baseType**</span></span> <br/> |<span data-ttu-id="bb72a-120">Nombre completo, incluido el espacio de nombres, de la clase de la que se deriva el agente.</span><span class="sxs-lookup"><span data-stu-id="bb72a-120">The full name, including the namespace, of the class from which the agent derives.</span></span> <span data-ttu-id="bb72a-121">Este atributo requiere un valor de cadena no vacío que contenga al menos un carácter.</span><span class="sxs-lookup"><span data-stu-id="bb72a-121">This attribute requires a nonempty string value that contains at least one character.</span></span>  <br/> |
|<span data-ttu-id="bb72a-122">**classFactory**</span><span class="sxs-lookup"><span data-stu-id="bb72a-122">**classFactory**</span></span> <br/> |<span data-ttu-id="bb72a-123">El nombre completo, incluido el espacio de nombres, de la clase que implementa el generador del agente que crea instancias del agente.</span><span class="sxs-lookup"><span data-stu-id="bb72a-123">The full name, including the namespace, of the class that implements the agent factory that creates instances of the agent.</span></span> <span data-ttu-id="bb72a-124">Este atributo debe contener el nombre completo de la clase que implementa el generador del agente que crea instancias del agente.</span><span class="sxs-lookup"><span data-stu-id="bb72a-124">This attribute must contain the fully qualified name of the class that implements the agent factory that creates instances of the agent.</span></span> <span data-ttu-id="bb72a-125">Esta clase debe derivarse de la clase [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) o [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bb72a-125">This class must derive from either the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) or [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class.</span></span>  <br/> |
|<span data-ttu-id="bb72a-126">**assemblyPath**</span><span class="sxs-lookup"><span data-stu-id="bb72a-126">**assemblyPath**</span></span> <br/> |<span data-ttu-id="bb72a-127">La ruta de acceso completa, incluido el nombre de archivo, del ensamblado que contiene el código para el agente.</span><span class="sxs-lookup"><span data-stu-id="bb72a-127">The fully qualified path, including the file name, of the assembly that contains the code for the agent.</span></span> <span data-ttu-id="bb72a-128">Este atributo requiere un valor de cadena no vacío que contenga al menos un carácter.</span><span class="sxs-lookup"><span data-stu-id="bb72a-128">This attribute requires a nonempty string value that contains at least one character.</span></span>  <br/> |
|<span data-ttu-id="bb72a-129">**enabled**</span><span class="sxs-lookup"><span data-stu-id="bb72a-129">**enabled**</span></span> <br/> |<span data-ttu-id="bb72a-130">Un valor booleano que indica si está habilitado el agente.</span><span class="sxs-lookup"><span data-stu-id="bb72a-130">A Boolean value that indicates whether the agent is enabled.</span></span> <span data-ttu-id="bb72a-131">El valor es **true** si el agente está habilitado; de lo contrario, el valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="bb72a-131">The value is **true** if the agent is enabled; otherwise, the value is **false**.</span></span> <span data-ttu-id="bb72a-132">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bb72a-132">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bb72a-133">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bb72a-133">Child elements</span></span>

<span data-ttu-id="bb72a-134">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bb72a-134">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bb72a-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bb72a-135">Parent elements</span></span>

|<span data-ttu-id="bb72a-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bb72a-136">**Element**</span></span>|<span data-ttu-id="bb72a-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb72a-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb72a-138">agentList</span><span class="sxs-lookup"><span data-stu-id="bb72a-138">agentList</span></span>](agentlist.md) <br/> |<span data-ttu-id="bb72a-139">Contiene un elemento **Agent** para cada agente instalado.</span><span class="sxs-lookup"><span data-stu-id="bb72a-139">Contains an **agent** element for each installed agent.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="bb72a-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bb72a-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb72a-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb72a-141">Namespace</span></span>  <br/> |<span data-ttu-id="bb72a-142">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="bb72a-142">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="bb72a-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bb72a-143">Schema Name</span></span>  <br/> |<span data-ttu-id="bb72a-144">No disponible.</span><span class="sxs-lookup"><span data-stu-id="bb72a-144">Not available.</span></span>  <br/> |
|<span data-ttu-id="bb72a-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bb72a-145">Validation File</span></span>  <br/> |<span data-ttu-id="bb72a-146">No disponible.</span><span class="sxs-lookup"><span data-stu-id="bb72a-146">Not available.</span></span>  <br/> |
|<span data-ttu-id="bb72a-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bb72a-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb72a-148">Falso.</span><span class="sxs-lookup"><span data-stu-id="bb72a-148">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb72a-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb72a-149">See also</span></span>

- [<span data-ttu-id="bb72a-150">Elementos del archivo de configuración de agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="bb72a-150">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

