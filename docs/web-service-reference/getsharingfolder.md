---
title: GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: ed5bb61f-89c7-4baa-83ee-30f06a49ff9b
description: El elemento GetSharingFolder define una solicitud para obtener el identificador de la carpeta local de una carpeta compartida especificada. Éste es el elemento base para la operación GetSharingFolder.
ms.openlocfilehash: 7c2f31aa27c1cbde6cdad2b41a341916b4bed2ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835669"
---
# <a name="getsharingfolder"></a><span data-ttu-id="1bb56-104">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="1bb56-104">GetSharingFolder</span></span>

<span data-ttu-id="1bb56-105">El elemento **GetSharingFolder** define una solicitud para obtener el identificador de la carpeta local de una carpeta compartida especificada.</span><span class="sxs-lookup"><span data-stu-id="1bb56-105">The **GetSharingFolder** element defines a request to get the local folder identifier of a specified shared folder.</span></span> <span data-ttu-id="1bb56-106">Éste es el elemento base para la [operación de GetSharingFolder](getsharingfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="1bb56-106">It is the base element for the [GetSharingFolder operation](getsharingfolder-operation.md).</span></span>
  
```xml
<GetSharingFolder>   <SmtpAddress/>   <DataType/>   <SharedFolderId/></GetSharingFolder>
```

 <span data-ttu-id="1bb56-107">**GetSharingFolderType**</span><span class="sxs-lookup"><span data-stu-id="1bb56-107">**GetSharingFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1bb56-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1bb56-108">Attributes and elements</span></span>

<span data-ttu-id="1bb56-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1bb56-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1bb56-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="1bb56-110">Attributes</span></span>

<span data-ttu-id="1bb56-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1bb56-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1bb56-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1bb56-112">Child elements</span></span>

|<span data-ttu-id="1bb56-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1bb56-113">**Element**</span></span>|<span data-ttu-id="1bb56-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1bb56-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1bb56-115">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="1bb56-115">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="1bb56-116">Representa la dirección de correo electrónico SMTP de la otra parte en la relación de uso compartida.</span><span class="sxs-lookup"><span data-stu-id="1bb56-116">Represents the SMTP e-mail address of the other party in the sharing relationship.</span></span> <span data-ttu-id="1bb56-117">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="1bb56-117">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="1bb56-118">DataType</span><span class="sxs-lookup"><span data-stu-id="1bb56-118">DataType</span></span>](datatype.md) <br/> |<span data-ttu-id="1bb56-119">Describe el tipo de datos que se comparten por una carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="1bb56-119">Describes the type of data that is shared by a shared folder.</span></span> <span data-ttu-id="1bb56-120">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="1bb56-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1bb56-121">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="1bb56-121">SharedFolderId</span></span>](sharedfolderid.md) <br/> |<span data-ttu-id="1bb56-122">Representa el identificador de la carpeta compartida que se debe devolver cuyo identificador de la carpeta local.</span><span class="sxs-lookup"><span data-stu-id="1bb56-122">Represents the identifier of the shared folder whose local folder identifier should be returned.</span></span> <span data-ttu-id="1bb56-123">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="1bb56-123">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1bb56-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1bb56-124">Parent elements</span></span>

<span data-ttu-id="1bb56-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1bb56-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1bb56-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1bb56-126">Remarks</span></span>

<span data-ttu-id="1bb56-127">Un elemento GetSharingFolder debe contener un elemento [SmtpAddress](smtpaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="1bb56-127">A GetSharingFolder element must contain an [SmtpAddress](smtpaddress.md) element.</span></span> <span data-ttu-id="1bb56-128">Un elemento GetSharingFolder también debe contener un elemento de [tipo de datos](datatype.md) o un elemento [SharedFolderId](sharedfolderid.md) , pero no puede contener ambas.</span><span class="sxs-lookup"><span data-stu-id="1bb56-128">A GetSharingFolder element must also contain either a [DataType](datatype.md) element or a [SharedFolderId](sharedfolderid.md) element, but cannot contain both.</span></span> 
  
<span data-ttu-id="1bb56-129">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1bb56-129">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1bb56-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1bb56-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bb56-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1bb56-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1bb56-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1bb56-132">Schema Name</span></span>  <br/> |<span data-ttu-id="1bb56-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1bb56-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1bb56-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1bb56-134">Validation File</span></span>  <br/> |<span data-ttu-id="1bb56-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1bb56-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1bb56-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1bb56-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="1bb56-137">False</span><span class="sxs-lookup"><span data-stu-id="1bb56-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1bb56-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="1bb56-138">See also</span></span>



[<span data-ttu-id="1bb56-139">Operación GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="1bb56-139">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="1bb56-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="1bb56-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

