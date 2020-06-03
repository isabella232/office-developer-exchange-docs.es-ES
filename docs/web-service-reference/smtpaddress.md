---
title: SmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SmtpAddress
api_type:
- schema
ms.assetid: 779305a6-ad1e-424e-8a69-4e3bef61d787
description: El elemento SmtpAddress representa la dirección del Protocolo simple de transferencia de correo (SMTP) de una cuenta que se va a usar para la suplantación o la dirección del destinatario del Protocolo simple de transferencia de correo (SMTP) de una solicitud de uso compartido de contactos o calendario.
ms.openlocfilehash: 915ff328cc384c1f2884e9fbea8c10c1ebc79288
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466692"
---
# <a name="smtpaddress"></a><span data-ttu-id="c9905-103">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="c9905-103">SmtpAddress</span></span>

<span data-ttu-id="c9905-104">El elemento **SmtpAddress** representa la dirección del Protocolo simple de transferencia de correo (SMTP) de una cuenta que se va a usar para la suplantación o la dirección del destinatario del Protocolo simple de transferencia de correo (SMTP) de una solicitud de uso compartido de contactos o calendario.</span><span class="sxs-lookup"><span data-stu-id="c9905-104">The **SmtpAddress** element represents the Simple Mail Transfer Protocol (SMTP) address of an account to be used for impersonation or a Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span> 
  
```xml
<SmtpAddress/>
```

<span data-ttu-id="c9905-105">**SmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="c9905-105">**SmtpAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c9905-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c9905-106">Attributes and elements</span></span>

<span data-ttu-id="c9905-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c9905-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9905-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c9905-108">Attributes</span></span>

<span data-ttu-id="c9905-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c9905-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9905-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c9905-110">Child elements</span></span>

<span data-ttu-id="c9905-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c9905-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c9905-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c9905-112">Parent elements</span></span>

|<span data-ttu-id="c9905-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c9905-113">**Element**</span></span>|<span data-ttu-id="c9905-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9905-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9905-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="c9905-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="c9905-116">Representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="c9905-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="c9905-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="c9905-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="c9905-118">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="c9905-118">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="c9905-119">Representa un destinatario no válido para un mensaje de uso compartido de calendarios o contactos.</span><span class="sxs-lookup"><span data-stu-id="c9905-119">Represents an invalid recipient for a calendar sharing or contact sharing message.</span></span>  <br/> |
|[<span data-ttu-id="c9905-120">Recipients (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="c9905-120">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="c9905-121">Representa una colección de destinatarios a los que se concederá acceso a la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="c9905-121">Represents a collection of recipients that will be granted access to the shared folder.</span></span>  <br/> |
|[<span data-ttu-id="c9905-122">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="c9905-122">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="c9905-123">Define una solicitud para obtener el identificador de carpeta local de una carpeta compartida especificada.</span><span class="sxs-lookup"><span data-stu-id="c9905-123">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c9905-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c9905-124">Text value</span></span>

<span data-ttu-id="c9905-125">Se necesita un valor de texto que represente una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="c9905-125">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c9905-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9905-126">Remarks</span></span>

<span data-ttu-id="c9905-127">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c9905-127">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9905-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c9905-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9905-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9905-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c9905-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c9905-130">Schema Name</span></span>  <br/> |<span data-ttu-id="c9905-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c9905-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="c9905-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c9905-132">Validation File</span></span>  <br/> |<span data-ttu-id="c9905-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c9905-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c9905-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c9905-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="c9905-135">Falso</span><span class="sxs-lookup"><span data-stu-id="c9905-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9905-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9905-136">See also</span></span>

- [<span data-ttu-id="c9905-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c9905-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

