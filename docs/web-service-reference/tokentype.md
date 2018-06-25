---
title: TokenType en
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83c650eb-7ab8-480c-a7c9-df60072ee042
description: El elemento TokenType en especifica el tipo de símbolo (token).
ms.openlocfilehash: 5c8e880f035ed74776a7c77e4b4e60ca46d66d4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840695"
---
# <a name="tokentype"></a><span data-ttu-id="57ab5-103">TokenType en</span><span class="sxs-lookup"><span data-stu-id="57ab5-103">TokenType</span></span>

<span data-ttu-id="57ab5-104">El elemento **TokenType en** especifica el tipo de símbolo (token).</span><span class="sxs-lookup"><span data-stu-id="57ab5-104">The **TokenType** element specifies the type of token.</span></span> 
  
```XML
<TokenType> CallerIdentity | ExtensionCallback | ScopedToken </TokenType>
```

 <span data-ttu-id="57ab5-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="57ab5-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="57ab5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="57ab5-106">Attributes and elements</span></span>

<span data-ttu-id="57ab5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="57ab5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57ab5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="57ab5-108">Attributes</span></span>

<span data-ttu-id="57ab5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="57ab5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="57ab5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="57ab5-110">Child elements</span></span>

<span data-ttu-id="57ab5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="57ab5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="57ab5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="57ab5-112">Parent elements</span></span>

<span data-ttu-id="57ab5-113">[TokenRequest](tokenrequest.md) | [símbolo (token)](token.md)</span><span class="sxs-lookup"><span data-stu-id="57ab5-113">[TokenRequest](tokenrequest.md) | [Token](token.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="57ab5-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="57ab5-114">Text value</span></span>

<span data-ttu-id="57ab5-115">El valor de texto del elemento **TokenType en** es el tipo de símbolo (token).</span><span class="sxs-lookup"><span data-stu-id="57ab5-115">The text value of the **TokenType** element is the token type.</span></span> <span data-ttu-id="57ab5-116">El valor de texto de **CallerIdentity** indica que el token es un token de identidad del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="57ab5-116">The text value of **CallerIdentity** indicates that the token is a caller identity token.</span></span> <span data-ttu-id="57ab5-117">El valor de texto de **ExtensionCallback** indica que el token es para una devolución de llamada de extensión.</span><span class="sxs-lookup"><span data-stu-id="57ab5-117">The text value of **ExtensionCallback** indicates that the token is for an extension callback.</span></span> <span data-ttu-id="57ab5-118">El valor de texto de **ScopedToken** indica que el token de acceso de cliente es un token de ámbito.</span><span class="sxs-lookup"><span data-stu-id="57ab5-118">The text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="57ab5-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57ab5-119">Remarks</span></span>

<span data-ttu-id="57ab5-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57ab5-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="57ab5-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="57ab5-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57ab5-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="57ab5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57ab5-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="57ab5-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="57ab5-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="57ab5-124">Schema name</span></span>  <br/> |<span data-ttu-id="57ab5-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="57ab5-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="57ab5-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="57ab5-126">Validation file</span></span>  <br/> |<span data-ttu-id="57ab5-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="57ab5-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="57ab5-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="57ab5-128">Can be empty</span></span>  <br/> |<span data-ttu-id="57ab5-129">falso</span><span class="sxs-lookup"><span data-stu-id="57ab5-129">false</span></span>  <br/> |
   

