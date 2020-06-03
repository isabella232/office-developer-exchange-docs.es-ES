---
title: TokenType (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: El elemento TokenType identifica el tipo de token de acceso de cliente que se devolverá en la respuesta GetClientAccessToken.
ms.openlocfilehash: 49ba2973967b12396e0c7f56129c89c40ccbcf97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466055"
---
# <a name="tokentype-clientaccesstokentype"></a><span data-ttu-id="0eac1-103">TokenType (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="0eac1-103">TokenType (ClientAccessTokenType)</span></span>

<span data-ttu-id="0eac1-104">El elemento **tokentype** identifica el tipo de token de acceso de cliente que se devolverá en la respuesta **GetClientAccessToken** .</span><span class="sxs-lookup"><span data-stu-id="0eac1-104">The **TokenType** element identifies the type of client access token that will be returned in the **GetClientAccessToken** response.</span></span> 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 <span data-ttu-id="0eac1-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="0eac1-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0eac1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0eac1-106">Attributes and elements</span></span>

<span data-ttu-id="0eac1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0eac1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0eac1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0eac1-108">Attributes</span></span>

<span data-ttu-id="0eac1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0eac1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0eac1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0eac1-110">Child elements</span></span>

<span data-ttu-id="0eac1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0eac1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0eac1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0eac1-112">Parent elements</span></span>

<span data-ttu-id="0eac1-113">[TokenRequest](tokenrequest.md)  |  [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)</span><span class="sxs-lookup"><span data-stu-id="0eac1-113">[TokenRequest](tokenrequest.md) | [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0eac1-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0eac1-114">Text value</span></span>

<span data-ttu-id="0eac1-115">Un valor de texto de **CallerIdentity** significa que se devuelve un token de acceso de cliente de identidad de autor de llamada.</span><span class="sxs-lookup"><span data-stu-id="0eac1-115">A text value of **CallerIdentity** means a caller identity client access token is returned.</span></span> <span data-ttu-id="0eac1-116">Un valor de texto de **ExtensionCallback** indica que se ha devuelto un token de acceso de cliente de devolución de llamada de extensión.</span><span class="sxs-lookup"><span data-stu-id="0eac1-116">A text value of **ExtensionCallback** indicates that an extension callback client access token is returned.</span></span> <span data-ttu-id="0eac1-117">Un valor de texto de **ScopedToken** indica que el token de acceso de cliente es un token con ámbito.</span><span class="sxs-lookup"><span data-stu-id="0eac1-117">A text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0eac1-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0eac1-118">Remarks</span></span>

<span data-ttu-id="0eac1-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0eac1-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0eac1-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0eac1-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0eac1-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0eac1-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0eac1-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="0eac1-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0eac1-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0eac1-123">Schema name</span></span>  <br/> |<span data-ttu-id="0eac1-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0eac1-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="0eac1-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0eac1-125">Validation file</span></span>  <br/> |<span data-ttu-id="0eac1-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0eac1-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0eac1-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0eac1-127">Can be empty</span></span>  <br/> |<span data-ttu-id="0eac1-128">false</span><span class="sxs-lookup"><span data-stu-id="0eac1-128">false</span></span>  <br/> |
   

