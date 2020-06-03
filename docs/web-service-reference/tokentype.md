---
title: TokenType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83c650eb-7ab8-480c-a7c9-df60072ee042
description: El elemento TokenType especifica el tipo de token.
ms.openlocfilehash: a42849dce9ed0253c3c5d4d4e899367b8e105594
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459885"
---
# <a name="tokentype"></a><span data-ttu-id="ac3b0-103">TokenType</span><span class="sxs-lookup"><span data-stu-id="ac3b0-103">TokenType</span></span>

<span data-ttu-id="ac3b0-104">El elemento **tokentype** especifica el tipo de token.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-104">The **TokenType** element specifies the type of token.</span></span> 
  
```XML
<TokenType> CallerIdentity | ExtensionCallback | ScopedToken </TokenType>
```

 <span data-ttu-id="ac3b0-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="ac3b0-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac3b0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ac3b0-106">Attributes and elements</span></span>

<span data-ttu-id="ac3b0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac3b0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac3b0-108">Attributes</span></span>

<span data-ttu-id="ac3b0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac3b0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ac3b0-110">Child elements</span></span>

<span data-ttu-id="ac3b0-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ac3b0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ac3b0-112">Parent elements</span></span>

<span data-ttu-id="ac3b0-113">[TokenRequest](tokenrequest.md)  |  [Token](token.md)</span><span class="sxs-lookup"><span data-stu-id="ac3b0-113">[TokenRequest](tokenrequest.md) | [Token](token.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ac3b0-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ac3b0-114">Text value</span></span>

<span data-ttu-id="ac3b0-115">El valor de texto del elemento **tokentype** es el tipo de token.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-115">The text value of the **TokenType** element is the token type.</span></span> <span data-ttu-id="ac3b0-116">El valor de texto de **CallerIdentity** indica que el token es un token de identidad de llamada.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-116">The text value of **CallerIdentity** indicates that the token is a caller identity token.</span></span> <span data-ttu-id="ac3b0-117">El valor de texto de **ExtensionCallback** indica que el token es para una devolución de llamada de extensión.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-117">The text value of **ExtensionCallback** indicates that the token is for an extension callback.</span></span> <span data-ttu-id="ac3b0-118">El valor de texto de **ScopedToken** indica que el token de acceso de cliente es un token con ámbito.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-118">The text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ac3b0-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac3b0-119">Remarks</span></span>

<span data-ttu-id="ac3b0-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ac3b0-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac3b0-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ac3b0-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac3b0-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac3b0-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ac3b0-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ac3b0-124">Schema name</span></span>  <br/> |<span data-ttu-id="ac3b0-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ac3b0-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="ac3b0-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ac3b0-126">Validation file</span></span>  <br/> |<span data-ttu-id="ac3b0-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ac3b0-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ac3b0-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ac3b0-128">Can be empty</span></span>  <br/> |<span data-ttu-id="ac3b0-129">false</span><span class="sxs-lookup"><span data-stu-id="ac3b0-129">false</span></span>  <br/> |
   

