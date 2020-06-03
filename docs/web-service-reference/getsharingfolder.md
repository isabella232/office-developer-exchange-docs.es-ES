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
description: El elemento GetSharingFolder define una solicitud para obtener el identificador de la carpeta local de una carpeta compartida especificada. Es el elemento base para la operación GetSharingFolder.
ms.openlocfilehash: cb76c534d9b30d0a9d1b267396551eb2871e638a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460508"
---
# <a name="getsharingfolder"></a><span data-ttu-id="fbe36-104">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="fbe36-104">GetSharingFolder</span></span>

<span data-ttu-id="fbe36-105">El elemento **GetSharingFolder** define una solicitud para obtener el identificador de la carpeta local de una carpeta compartida especificada.</span><span class="sxs-lookup"><span data-stu-id="fbe36-105">The **GetSharingFolder** element defines a request to get the local folder identifier of a specified shared folder.</span></span> <span data-ttu-id="fbe36-106">Es el elemento base para la [operación GetSharingFolder](getsharingfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="fbe36-106">It is the base element for the [GetSharingFolder operation](getsharingfolder-operation.md).</span></span>
  
```xml
<GetSharingFolder>   <SmtpAddress/>   <DataType/>   <SharedFolderId/></GetSharingFolder>
```

 <span data-ttu-id="fbe36-107">**GetSharingFolderType**</span><span class="sxs-lookup"><span data-stu-id="fbe36-107">**GetSharingFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fbe36-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fbe36-108">Attributes and elements</span></span>

<span data-ttu-id="fbe36-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fbe36-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbe36-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbe36-110">Attributes</span></span>

<span data-ttu-id="fbe36-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fbe36-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fbe36-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fbe36-112">Child elements</span></span>

|<span data-ttu-id="fbe36-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbe36-113">**Element**</span></span>|<span data-ttu-id="fbe36-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbe36-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbe36-115">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="fbe36-115">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="fbe36-116">Representa la dirección de correo electrónico SMTP de la otra parte en la relación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="fbe36-116">Represents the SMTP e-mail address of the other party in the sharing relationship.</span></span> <span data-ttu-id="fbe36-117">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="fbe36-117">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="fbe36-118">DataType</span><span class="sxs-lookup"><span data-stu-id="fbe36-118">DataType</span></span>](datatype.md) <br/> |<span data-ttu-id="fbe36-119">Describe el tipo de datos que comparte una carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="fbe36-119">Describes the type of data that is shared by a shared folder.</span></span> <span data-ttu-id="fbe36-120">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="fbe36-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="fbe36-121">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="fbe36-121">SharedFolderId</span></span>](sharedfolderid.md) <br/> |<span data-ttu-id="fbe36-122">Representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe devolverse.</span><span class="sxs-lookup"><span data-stu-id="fbe36-122">Represents the identifier of the shared folder whose local folder identifier should be returned.</span></span> <span data-ttu-id="fbe36-123">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="fbe36-123">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fbe36-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fbe36-124">Parent elements</span></span>

<span data-ttu-id="fbe36-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fbe36-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fbe36-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fbe36-126">Remarks</span></span>

<span data-ttu-id="fbe36-127">Un elemento GetSharingFolder debe contener un elemento [SmtpAddress](smtpaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="fbe36-127">A GetSharingFolder element must contain an [SmtpAddress](smtpaddress.md) element.</span></span> <span data-ttu-id="fbe36-128">Un elemento GetSharingFolder también debe contener un elemento [DataType](datatype.md) o un elemento [SharedFolderId](sharedfolderid.md) , pero no puede contener ambos.</span><span class="sxs-lookup"><span data-stu-id="fbe36-128">A GetSharingFolder element must also contain either a [DataType](datatype.md) element or a [SharedFolderId](sharedfolderid.md) element, but cannot contain both.</span></span> 
  
<span data-ttu-id="fbe36-129">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="fbe36-129">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbe36-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fbe36-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbe36-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbe36-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fbe36-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fbe36-132">Schema Name</span></span>  <br/> |<span data-ttu-id="fbe36-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="fbe36-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fbe36-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fbe36-134">Validation File</span></span>  <br/> |<span data-ttu-id="fbe36-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fbe36-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fbe36-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fbe36-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="fbe36-137">Falso</span><span class="sxs-lookup"><span data-stu-id="fbe36-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbe36-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbe36-138">See also</span></span>



[<span data-ttu-id="fbe36-139">Operación GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="fbe36-139">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="fbe36-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fbe36-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

