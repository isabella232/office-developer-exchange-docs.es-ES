---
title: IdOfFolderToShare
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IdOfFolderToShare
api_type:
- schema
ms.assetid: 199d1839-f061-4070-a977-874b0c08e5be
description: El elemento IdOfFolderToShare representa el identificador de la carpeta en el servidor que se va a compartir.
ms.openlocfilehash: 93a4740d9adefbb35aae071f0a6bfcb4b2021b4d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457630"
---
# <a name="idoffoldertoshare"></a><span data-ttu-id="37911-103">IdOfFolderToShare</span><span class="sxs-lookup"><span data-stu-id="37911-103">IdOfFolderToShare</span></span>

<span data-ttu-id="37911-104">El elemento **IdOfFolderToShare** representa el identificador de la carpeta en el servidor que se va a compartir.</span><span class="sxs-lookup"><span data-stu-id="37911-104">The **IdOfFolderToShare** element represents the identifier of the folder on the server that will be shared.</span></span> 
  
```
<IdOfFolderToShare Id="" ChangeKey="" />
```

 <span data-ttu-id="37911-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="37911-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37911-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="37911-106">Attributes and elements</span></span>

<span data-ttu-id="37911-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="37911-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37911-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="37911-108">Attributes</span></span>

|<span data-ttu-id="37911-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="37911-109">**Attribute**</span></span>|<span data-ttu-id="37911-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37911-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37911-111">Id</span><span class="sxs-lookup"><span data-stu-id="37911-111">Id</span></span>  <br/> |<span data-ttu-id="37911-112">Contiene una cadena que identifica una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="37911-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="37911-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="37911-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="37911-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="37911-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="37911-115">Contiene una cadena que identifica una versión de una carpeta identificada por el atributo id.</span><span class="sxs-lookup"><span data-stu-id="37911-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="37911-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="37911-116">This attribute is optional.</span></span> <span data-ttu-id="37911-117">Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="37911-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="37911-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37911-118">Child elements</span></span>

<span data-ttu-id="37911-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="37911-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="37911-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="37911-120">Parent elements</span></span>

|<span data-ttu-id="37911-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="37911-121">**Element**</span></span>|<span data-ttu-id="37911-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37911-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37911-123">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="37911-123">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="37911-124">Define una solicitud para obtener un token de autenticación opaco que identifique la invitación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="37911-124">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37911-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37911-125">Remarks</span></span>

<span data-ttu-id="37911-126">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="37911-126">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37911-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="37911-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37911-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="37911-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="37911-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="37911-129">Schema Name</span></span>  <br/> |<span data-ttu-id="37911-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="37911-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="37911-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="37911-131">Validation File</span></span>  <br/> |<span data-ttu-id="37911-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="37911-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="37911-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="37911-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="37911-134">Falso</span><span class="sxs-lookup"><span data-stu-id="37911-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37911-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="37911-135">See also</span></span>



[<span data-ttu-id="37911-136">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="37911-136">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="37911-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="37911-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

