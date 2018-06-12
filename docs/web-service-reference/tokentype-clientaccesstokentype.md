---
title: TokenType en (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: El elemento TokenType en identifica el tipo de token de acceso de cliente que se devuelve en la respuesta de GetClientAccessToken.
ms.openlocfilehash: c9adb60acf76fefebd58e2fd3bc899332a63dbee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840701"
---
# <a name="tokentype-clientaccesstokentype"></a><span data-ttu-id="a1ccf-103">TokenType en (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="a1ccf-103">TokenType (ClientAccessTokenType)</span></span>

<span data-ttu-id="a1ccf-104">El elemento **TokenType en** identifica el tipo de token de acceso de cliente que se devuelve en la respuesta de **GetClientAccessToken** .</span><span class="sxs-lookup"><span data-stu-id="a1ccf-104">The **TokenType** element identifies the type of client access token that will be returned in the **GetClientAccessToken** response.</span></span> 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 <span data-ttu-id="a1ccf-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="a1ccf-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a1ccf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a1ccf-106">Attributes and elements</span></span>

<span data-ttu-id="a1ccf-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a1ccf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1ccf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a1ccf-108">Attributes</span></span>

<span data-ttu-id="a1ccf-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a1ccf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a1ccf-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a1ccf-110">Child elements</span></span>

<span data-ttu-id="a1ccf-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a1ccf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a1ccf-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a1ccf-112">Parent elements</span></span>

<span data-ttu-id="a1ccf-113">[TokenRequest](tokenrequest.md) | [(ClientAccessTokenType) de Token](token-clientaccesstokentype.md)</span><span class="sxs-lookup"><span data-stu-id="a1ccf-113">[TokenRequest](tokenrequest.md) | [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a1ccf-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a1ccf-114">Text value</span></span>

<span data-ttu-id="a1ccf-115">Un valor de texto de **CallerIdentity** significa que se devuelve un token de acceso de cliente de identidad de autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a1ccf-115">A text value of **CallerIdentity** means a caller identity client access token is returned.</span></span> <span data-ttu-id="a1ccf-116">Un valor de texto de **ExtensionCallback** indica que se devuelve un token de acceso de cliente de devolución de llamada de extensión.</span><span class="sxs-lookup"><span data-stu-id="a1ccf-116">A text value of **ExtensionCallback** indicates that an extension callback client access token is returned.</span></span> <span data-ttu-id="a1ccf-117">Un valor de texto de **ScopedToken** indica que el token de acceso de cliente es un token de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a1ccf-117">A text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a1ccf-118">Notas</span><span class="sxs-lookup"><span data-stu-id="a1ccf-118">Remarks</span></span>

<span data-ttu-id="a1ccf-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a1ccf-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a1ccf-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a1ccf-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1ccf-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a1ccf-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1ccf-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a1ccf-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a1ccf-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a1ccf-123">Schema name</span></span>  <br/> |<span data-ttu-id="a1ccf-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a1ccf-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="a1ccf-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a1ccf-125">Validation file</span></span>  <br/> |<span data-ttu-id="a1ccf-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a1ccf-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a1ccf-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a1ccf-127">Can be empty</span></span>  <br/> |<span data-ttu-id="a1ccf-128">falso</span><span class="sxs-lookup"><span data-stu-id="a1ccf-128">false</span></span>  <br/> |
   

