---
title: FolderNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderNames
api_type:
- schema
ms.assetid: 6cbe4083-5705-4695-a54e-8dab3e472662
description: El elemento FolderNames contiene una matriz de carpetas administradas con nombre para agregar a un buzón de correo.
ms.openlocfilehash: 00cb1a81f420469033ccbc745313d2719b155aff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530989"
---
# <a name="foldernames"></a><span data-ttu-id="97aa7-103">FolderNames</span><span class="sxs-lookup"><span data-stu-id="97aa7-103">FolderNames</span></span>

<span data-ttu-id="97aa7-104">El elemento **FolderNames** contiene una matriz de carpetas administradas con nombre para agregar a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="97aa7-104">The **FolderNames** element contains an array of named managed folders to add to a mailbox.</span></span> 
  
[<span data-ttu-id="97aa7-105">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="97aa7-105">CreateManagedFolder</span></span>](createmanagedfolder.md)
  
[<span data-ttu-id="97aa7-106">FolderNames</span><span class="sxs-lookup"><span data-stu-id="97aa7-106">FolderNames</span></span>](foldernames.md)
  
```xml
<FolderNames>
   <FolderName/>
</FolderNames>
```

 <span data-ttu-id="97aa7-107">**NonEmptyArrayOfFolderNamesType**</span><span class="sxs-lookup"><span data-stu-id="97aa7-107">**NonEmptyArrayOfFolderNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="97aa7-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="97aa7-108">Attributes and elements</span></span>

<span data-ttu-id="97aa7-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="97aa7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97aa7-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="97aa7-110">Attributes</span></span>

<span data-ttu-id="97aa7-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="97aa7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="97aa7-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="97aa7-112">Child elements</span></span>

|<span data-ttu-id="97aa7-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="97aa7-113">**Element**</span></span>|<span data-ttu-id="97aa7-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="97aa7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97aa7-115">FolderName</span><span class="sxs-lookup"><span data-stu-id="97aa7-115">FolderName</span></span>](foldername.md) <br/> |<span data-ttu-id="97aa7-116">Identifica una única carpeta administrada para agregar al buzón.</span><span class="sxs-lookup"><span data-stu-id="97aa7-116">Identifies a single managed folder to add to mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="97aa7-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="97aa7-117">Parent elements</span></span>

|<span data-ttu-id="97aa7-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="97aa7-118">**Element**</span></span>|<span data-ttu-id="97aa7-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="97aa7-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97aa7-120">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="97aa7-120">CreateManagedFolder</span></span>](createmanagedfolder.md) <br/> |<span data-ttu-id="97aa7-121">El elemento raíz de una solicitud para agregar una carpeta administrada a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="97aa7-121">The root element in a request to add a managed folder to a mailbox.</span></span>  <br/> <span data-ttu-id="97aa7-122">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="97aa7-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateManagedFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97aa7-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97aa7-123">Remarks</span></span>

<span data-ttu-id="97aa7-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="97aa7-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="97aa7-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="97aa7-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97aa7-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="97aa7-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="97aa7-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="97aa7-127">Schema Name</span></span>  <br/> |<span data-ttu-id="97aa7-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="97aa7-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="97aa7-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="97aa7-129">Validation File</span></span>  <br/> |<span data-ttu-id="97aa7-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="97aa7-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="97aa7-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="97aa7-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="97aa7-132">Falso</span><span class="sxs-lookup"><span data-stu-id="97aa7-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="97aa7-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="97aa7-133">See also</span></span>



[<span data-ttu-id="97aa7-134">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="97aa7-134">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="97aa7-135">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="97aa7-135">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="97aa7-136">Adición de carpetas administradas</span><span class="sxs-lookup"><span data-stu-id="97aa7-136">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

