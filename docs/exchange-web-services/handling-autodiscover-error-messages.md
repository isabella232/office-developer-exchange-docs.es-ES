---
title: Administrar los mensajes de error de detección automática
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: Obtenga información sobre los distintos tipos de errores de detección automática y qué hacer con ellos.
localization_priority: Priority
ms.openlocfilehash: 0cba7e54cb251a9775e0971826560e277dcd9d2d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455964"
---
# <a name="handling-autodiscover-error-messages"></a><span data-ttu-id="f245c-103">Administrar los mensajes de error de detección automática</span><span class="sxs-lookup"><span data-stu-id="f245c-103">Handling Autodiscover error messages</span></span>

<span data-ttu-id="f245c-104">Obtenga información sobre los distintos tipos de errores de detección automática y qué hacer con ellos.</span><span class="sxs-lookup"><span data-stu-id="f245c-104">Learn about the different types of Autodiscover errors and what to do with them.</span></span>
  
<span data-ttu-id="f245c-105">La detección automática permite que las aplicaciones recuperen automáticamente la información de configuración y funciona bien.</span><span class="sxs-lookup"><span data-stu-id="f245c-105">Autodiscover enables your applications to retrieve configuration information automatically, and it works great.</span></span> <span data-ttu-id="f245c-106">Sin embargo, las cosas no siempre van según el plan.</span><span class="sxs-lookup"><span data-stu-id="f245c-106">However, things don't always go according to plan.</span></span> <span data-ttu-id="f245c-107">Veamos los errores comunes que pueden producirse y cómo puede controlarlos para minimizar la necesidad de solicitar al usuario que configure el cliente de forma manual.</span><span class="sxs-lookup"><span data-stu-id="f245c-107">Let's look at the common errors that might occur and how you can handle them to minimize the need to prompt your user to manually configure your client.</span></span>
  
## <a name="http-status-errors"></a><span data-ttu-id="f245c-108">Errores de Estado HTTP</span><span class="sxs-lookup"><span data-stu-id="f245c-108">HTTP status errors</span></span>
<span data-ttu-id="f245c-109"><a name="bk_HttpErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="f245c-109"><a name="bk_HttpErrors"> </a></span></span>

<span data-ttu-id="f245c-110">El primer tipo de error que puede encontrarse al enviar solicitudes de detección automática es el estado de HTTP.</span><span class="sxs-lookup"><span data-stu-id="f245c-110">The first type of error you might encounter when sending Autodiscover requests is the HTTP status.</span></span> <span data-ttu-id="f245c-111">Si el Estado HTTP de la respuesta es distinto de 200 (correcto), la carga de respuesta no contiene la respuesta de detección automática que estaba buscando.</span><span class="sxs-lookup"><span data-stu-id="f245c-111">If the HTTP status in your response is anything other than 200 (OK), the response payload doesn't contain the Autodiscover response you were looking for.</span></span> <span data-ttu-id="f245c-112">Para simplificar, podemos agrupar los códigos de estado que no sean 200 en tres categorías.</span><span class="sxs-lookup"><span data-stu-id="f245c-112">For simplicity, we can group non-200 status codes into three categories.</span></span>
  
<span data-ttu-id="f245c-113">**Tabla 1. Códigos de Estado HTTP**</span><span class="sxs-lookup"><span data-stu-id="f245c-113">**Table 1. HTTP status codes**</span></span>

|<span data-ttu-id="f245c-114">**Código de estado**</span><span class="sxs-lookup"><span data-stu-id="f245c-114">**Status code**</span></span>|<span data-ttu-id="f245c-115">**Tipo de error**</span><span class="sxs-lookup"><span data-stu-id="f245c-115">**Type of error**</span></span>|<span data-ttu-id="f245c-116">**Para controlar...**</span><span class="sxs-lookup"><span data-stu-id="f245c-116">**To handle…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f245c-117">301 o 302</span><span class="sxs-lookup"><span data-stu-id="f245c-117">301 or 302</span></span>  <br/> |<span data-ttu-id="f245c-118">Error de redirección</span><span class="sxs-lookup"><span data-stu-id="f245c-118">Redirect error</span></span>  <br/> |<span data-ttu-id="f245c-119">Vuelva a enviar la solicitud al URI contenido en el encabezado de respuesta HTTP "Location".</span><span class="sxs-lookup"><span data-stu-id="f245c-119">Resend your request to the URI contained in the "Location" HTTP response header.</span></span> <span data-ttu-id="f245c-120">Para obtener más información, consulte [Handling Redirect Errors](#bk_HandlingRedirects).</span><span class="sxs-lookup"><span data-stu-id="f245c-120">For details, see [Handling redirect errors](#bk_HandlingRedirects).</span></span>  <br/> |
|<span data-ttu-id="f245c-121">401</span><span class="sxs-lookup"><span data-stu-id="f245c-121">401</span></span>  <br/> |<span data-ttu-id="f245c-122">Error no autorizado</span><span class="sxs-lookup"><span data-stu-id="f245c-122">Unauthorized error</span></span>  <br/> |<span data-ttu-id="f245c-123">Dado que el [proceso de detección automática](autodiscover-for-exchange.md) implica probar varias direcciones URL potenciales, puede obtener esto en una dirección URL solo para que la siguiente acepte sus credenciales.</span><span class="sxs-lookup"><span data-stu-id="f245c-123">Because the [Autodiscover process](autodiscover-for-exchange.md) involves trying multiple potential URLs, you could get this on one URL only to have the next one accept your credentials.</span></span> <span data-ttu-id="f245c-124">Por este motivo, no debe tener en cuenta un solo error 401 para indicar que las credenciales no son válidas.</span><span class="sxs-lookup"><span data-stu-id="f245c-124">For this reason, you shouldn't consider a single 401 error to indicate that the credentials are invalid.</span></span> <span data-ttu-id="f245c-125">Sin embargo, si recibe errores de 401 de varias direcciones URL, es posible que quiera pedir al usuario que vuelva a escribir su contraseña (si es posible).</span><span class="sxs-lookup"><span data-stu-id="f245c-125">However, if you receive 401 errors from multiple URLs, you might want to prompt the user to reenter their password (if possible).</span></span>  <br/> |
|<span data-ttu-id="f245c-126">Cualquier otro Estado que no sea 200</span><span class="sxs-lookup"><span data-stu-id="f245c-126">Any other non-200 status</span></span>  <br/> |<span data-ttu-id="f245c-127">Error de punto de conexión de detección automática no válido</span><span class="sxs-lookup"><span data-stu-id="f245c-127">Invalid Autodiscover endpoint error</span></span>  <br/> |<span data-ttu-id="f245c-128">Considere la dirección URL que devuelve cualquier otro código de estado que no sea 200 no es válido y continúe intentándolo con la siguiente dirección URL de la lista.</span><span class="sxs-lookup"><span data-stu-id="f245c-128">Consider the URL that returns any other non-200 status code to be invalid, and continue trying the next URL in your list.</span></span>  <br/> |
   
## <a name="autodiscover-errors"></a><span data-ttu-id="f245c-129">Errores de detección automática</span><span class="sxs-lookup"><span data-stu-id="f245c-129">Autodiscover errors</span></span>
<span data-ttu-id="f245c-130"><a name="bk_AutodiscoverErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="f245c-130"><a name="bk_AutodiscoverErrors"> </a></span></span>

<span data-ttu-id="f245c-131">Incluso si obtiene un código de estado 200 (correcto) después de enviar una solicitud de detección automática, eso no significa que el servidor haya enviado la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="f245c-131">Even if you get a 200 (OK) status code after sending an Autodiscover request, that doesn't mean that the server sent the information you need.</span></span> <span data-ttu-id="f245c-132">El estado 200 solo significa que tiene una respuesta de detección automática y que la respuesta puede contener un error dentro de la carga.</span><span class="sxs-lookup"><span data-stu-id="f245c-132">The 200 status only means that you have an Autodiscover response, and that response might contain an error within the payload.</span></span> <span data-ttu-id="f245c-133">La ubicación de la información de error varía en función de si el formato es SOAP o POX.</span><span class="sxs-lookup"><span data-stu-id="f245c-133">The location of the error information differs depending on whether the format is SOAP or POX.</span></span>
  
### <a name="soap-autodiscover-errors"></a><span data-ttu-id="f245c-134">Errores de detección automática de SOAP</span><span class="sxs-lookup"><span data-stu-id="f245c-134">SOAP Autodiscover errors</span></span>

<span data-ttu-id="f245c-135">Para la detección automática de SOAP, la respuesta puede contener uno o más elementos [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) , en lugares diferentes.</span><span class="sxs-lookup"><span data-stu-id="f245c-135">For SOAP Autodiscover, the response can contain one or more [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) elements, in different places.</span></span> <span data-ttu-id="f245c-136">Normalmente, se puede esperar que haya un elemento secundario del elemento [Response (SOAP)](https://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) y otro como elemento secundario de cada elemento [UserResponse (SOAP)](https://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f245c-136">Typically you can expect one as a child element of the [Response (SOAP)](https://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) element, and one as a child of each [UserResponse (SOAP)](https://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) element in the response.</span></span> <span data-ttu-id="f245c-137">También es posible que encuentre uno como elemento secundario de un elemento [UserSettingError (SOAP)](https://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) , si hay alguno presente.</span><span class="sxs-lookup"><span data-stu-id="f245c-137">You might also encounter one as a child of a [UserSettingError (SOAP)](https://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) element, if one is present.</span></span> <span data-ttu-id="f245c-138">El contexto del error depende de dónde se encuentre el elemento **ErrorCode** , como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f245c-138">The context of the error depends on where the **ErrorCode** element is located, as follows:</span></span> 
  
- <span data-ttu-id="f245c-139">Como elemento secundario del elemento **Response** , el elemento **ErrorCode** representa un error que se aplica a toda la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f245c-139">As a child element of the **Response** element, the **ErrorCode** element represents an error that applies to the entire request.</span></span> 
    
- <span data-ttu-id="f245c-140">Como elemento secundario del elemento **UserResponse** , representa un error que se aplica solo a ese usuario específico.</span><span class="sxs-lookup"><span data-stu-id="f245c-140">As a child of the **UserResponse** element, it represents an error that applies just to that specific user.</span></span> 
    
- <span data-ttu-id="f245c-141">Como elemento secundario de un elemento **UserSettingError** , representa un error que se aplica a una configuración específica que se solicitó.</span><span class="sxs-lookup"><span data-stu-id="f245c-141">As a child of a **UserSettingError** element, it represents an error that applies to a specific setting that was requested.</span></span> 
    
<span data-ttu-id="f245c-142">Echemos un vistazo a un ejemplo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f245c-142">Let's take a look at an example of a response.</span></span> <span data-ttu-id="f245c-143">En este ejemplo, el elemento **ErrorCode** del elemento **Response** tiene un valor de "NoError", que indica el éxito general.</span><span class="sxs-lookup"><span data-stu-id="f245c-143">In this example, the **ErrorCode** element under the **Response** element has a value of "NoError", which indicates overall success.</span></span> <span data-ttu-id="f245c-144">Sin embargo, el elemento **ErrorCode** del elemento **UserResponse** tiene un valor de "RedirectAddress", que indica que se ha producido un error para ese usuario en particular.</span><span class="sxs-lookup"><span data-stu-id="f245c-144">However, the **ErrorCode** element under the **UserResponse** element has a value of "RedirectAddress", which indicates that an error occurred for that particular user.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>elvin@mail.contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="f245c-145">El artículo [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) contiene una lista completa de los posibles errores.</span><span class="sxs-lookup"><span data-stu-id="f245c-145">The [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) article contains a full list of possible errors.</span></span> <span data-ttu-id="f245c-146">La mayoría de estos errores indican un error irrecuperable, pero algunos de ellos justifican un tratamiento especial.</span><span class="sxs-lookup"><span data-stu-id="f245c-146">Most of these indicate an unrecoverable error, but a few warrant special handling.</span></span> 
  
<span data-ttu-id="f245c-147">**Tabla 2. Valores del ErrorCode de Autodisover SOAP**</span><span class="sxs-lookup"><span data-stu-id="f245c-147">**Table 2. SOAP Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="f245c-148">**Valor ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f245c-148">**ErrorCode value**</span></span>|<span data-ttu-id="f245c-149">**Para controlar...**</span><span class="sxs-lookup"><span data-stu-id="f245c-149">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f245c-150">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="f245c-150">RedirectAddress</span></span>  <br/> |<span data-ttu-id="f245c-151">[Reiniciar la detección automática con una dirección de correo electrónico nueva](#bk_RestartAutodiscover) con la dirección de correo electrónico en el elemento [RedirectTarget (SOAP)](https://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f245c-151">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectTarget (SOAP)](https://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="f245c-152">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="f245c-152">RedirectUrl</span></span>  <br/> |<span data-ttu-id="f245c-153">[Reenviar la solicitud a una nueva dirección URL](#bk_ResendRequest) en la dirección URL del elemento **RedirectTarget** .</span><span class="sxs-lookup"><span data-stu-id="f245c-153">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the **RedirectTarget** element.</span></span>  <br/> |
|<span data-ttu-id="f245c-154">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="f245c-154">ServerBusy</span></span>  <br/> |<span data-ttu-id="f245c-155">Vuelva a intentar esta dirección URL tras un pequeño retraso.</span><span class="sxs-lookup"><span data-stu-id="f245c-155">Retry this URL after a small delay.</span></span> <span data-ttu-id="f245c-156">Puede esperar un período de tiempo determinado o simplemente mover esta dirección URL al final de la lista de direcciones URL para probar.</span><span class="sxs-lookup"><span data-stu-id="f245c-156">You might wait a set amount of time or simply move this URL to the end of your list of URLs to try.</span></span> <span data-ttu-id="f245c-157">Si recibe este error varias veces desde una dirección URL, debe tener en cuenta que la dirección URL no es válida.</span><span class="sxs-lookup"><span data-stu-id="f245c-157">If you receive this error multiple times from a URL, you should consider the URL to be invalid.</span></span>  <br/> |
   
### <a name="pox-autodiscover-errors"></a><span data-ttu-id="f245c-158">Errores de detección automática de POX</span><span class="sxs-lookup"><span data-stu-id="f245c-158">POX Autodiscover errors</span></span>

<span data-ttu-id="f245c-159">El servicio Detección automática de POX informa de los errores de una forma ligeramente distinta.</span><span class="sxs-lookup"><span data-stu-id="f245c-159">The POX Autodiscover service reports errors a little differently.</span></span> <span data-ttu-id="f245c-160">Los errores no recuperables se encuentran en el elemento [error (POX)](https://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f245c-160">Non-recoverable errors are contained in the [Error (POX)](https://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="f245c-161">El artículo código de error [(POX)](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) contiene una lista completa de los códigos de error posibles.</span><span class="sxs-lookup"><span data-stu-id="f245c-161">The [ErrorCode (POX)](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) article contains a full list of possible error codes.</span></span> 
  
<span data-ttu-id="f245c-162">Los errores de redirección se incluyen en el elemento [Action (POX)](https://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f245c-162">Redirect errors are contained in the [Action (POX)](https://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="f245c-163">Cualquier valor del elemento **Action** distinto de "Settings" indica un error de redirección.</span><span class="sxs-lookup"><span data-stu-id="f245c-163">Any value of the **Action** element other than "settings" indicates a redirect error.</span></span> 
  
<span data-ttu-id="f245c-164">**Tabla 3. Valores del ErrorCode Autodisover de POX**</span><span class="sxs-lookup"><span data-stu-id="f245c-164">**Table 3. POX Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="f245c-165">**Valor de la acción**</span><span class="sxs-lookup"><span data-stu-id="f245c-165">**Action value**</span></span>|<span data-ttu-id="f245c-166">**Para controlar...**</span><span class="sxs-lookup"><span data-stu-id="f245c-166">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f245c-167">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="f245c-167">redirectAddr</span></span>  <br/> |<span data-ttu-id="f245c-168">[Reiniciando detección automática con una dirección de correo electrónico nueva](#bk_RestartAutodiscover) con la dirección de correo electrónico en el elemento [RedirectAddr (POX)](https://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f245c-168">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectAddr (POX)](https://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="f245c-169">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="f245c-169">redirectUrl</span></span>  <br/> |<span data-ttu-id="f245c-170">[Reenviar la solicitud a una nueva dirección URL](#bk_ResendRequest) a la dirección URL en el elemento [RedirectURL (POX)](https://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f245c-170">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the [RedirectUrl (POX)](https://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) element.</span></span>  <br/> |
   
<span data-ttu-id="f245c-171">En este ejemplo, el elemento **Action** tiene un valor de "redirectAddr", que indica que se debe enviar una nueva solicitud con la nueva dirección de correo electrónico contenida en el elemento **redirectAddr** .</span><span class="sxs-lookup"><span data-stu-id="f245c-171">In this example, the **Action** element has a value of "redirectAddr", which indicates that a new request should be sent with the new email address contained in the **RedirectAddr** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="handling-redirect-errors"></a><span data-ttu-id="f245c-172">Control de errores de redirección</span><span class="sxs-lookup"><span data-stu-id="f245c-172">Handling redirect errors</span></span>
<span data-ttu-id="f245c-173"><a name="bk_HandlingRedirects"> </a></span><span class="sxs-lookup"><span data-stu-id="f245c-173"><a name="bk_HandlingRedirects"> </a></span></span>

<span data-ttu-id="f245c-174">Puede controlar los escenarios de error de redirección de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="f245c-174">You can handle redirect error scenarios in two ways:</span></span>
  
- <span data-ttu-id="f245c-175">Reiniciando la detección automática con una nueva dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f245c-175">By restarting Autodiscover with a new email address.</span></span>
    
- <span data-ttu-id="f245c-176">Reenviando la solicitud a una nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f245c-176">By resending your request to a new URL.</span></span>
    
<span data-ttu-id="f245c-177">Ambos escenarios requieren una validación antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="f245c-177">Both scenarios require some validation before proceeding.</span></span>
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a><span data-ttu-id="f245c-178">Reinicio de detección automática con una nueva dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="f245c-178">Restarting Autodiscover with a new email address</span></span>
<span data-ttu-id="f245c-179"><a name="bk_RestartAutodiscover"> </a></span><span class="sxs-lookup"><span data-stu-id="f245c-179"><a name="bk_RestartAutodiscover"> </a></span></span>

<span data-ttu-id="f245c-180">Cuando obtenga una nueva dirección de correo electrónico en una respuesta de redireccionamiento de detección automática, compruebe primero que la nueva dirección de correo electrónico que se proporcionó en la respuesta de error de redireccionamiento no es la misma dirección que envió en la solicitud que resultó en el error.</span><span class="sxs-lookup"><span data-stu-id="f245c-180">When you get a new email address in an Autodiscover redirect response, first verify that the new email address that was provided in the redirect error response is not the same address that you sent in the request that resulted in the error.</span></span> <span data-ttu-id="f245c-181">Si es así, no debe reiniciar la detección automática y considere, en su lugar, que la dirección URL que generó la respuesta no sea válida.</span><span class="sxs-lookup"><span data-stu-id="f245c-181">If it is, you should not restart Autodiscover and instead consider the URL that generated the response to be invalid.</span></span>
  
<span data-ttu-id="f245c-182">Si la nueva dirección de correo electrónico es diferente, descarte la lista existente de direcciones URL potenciales del punto de conexión de detección automática y genere una nueva lista basada en la nueva dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f245c-182">If the new email address is different, discard your existing list of potential Autodiscover endpoint URLs and generate a new list based on the new email address.</span></span>
  
### <a name="resending-your-request-to-a-new-url"></a><span data-ttu-id="f245c-183">Reenviar la solicitud a una nueva dirección URL</span><span class="sxs-lookup"><span data-stu-id="f245c-183">Resending your request to a new URL</span></span>
<span data-ttu-id="f245c-184"><a name="bk_ResendRequest"> </a></span><span class="sxs-lookup"><span data-stu-id="f245c-184"><a name="bk_ResendRequest"> </a></span></span>

<span data-ttu-id="f245c-185">Cuando obtenga una nueva dirección URL en una respuesta de redireccionamiento de detección automática, primero debe validar la dirección URL de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f245c-185">When you get a new URL in an Autodiscover redirect response, you should first validate the URL as follows:</span></span>
  
- <span data-ttu-id="f245c-186">Compruebe que la dirección URL es una dirección URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f245c-186">Verify that the URL is an HTTPS URL.</span></span>
    
- <span data-ttu-id="f245c-187">Compruebe que no ha recibido un error de esta dirección URL con la dirección de correo electrónico actual anterior.</span><span class="sxs-lookup"><span data-stu-id="f245c-187">Verify that you have not received an error from this URL with the current email address before.</span></span>
    
- <span data-ttu-id="f245c-188">Si es aplicable a la aplicación, informe al usuario de la redirección y obtenga su permiso para seguir el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="f245c-188">If applicable to your application, inform the user of the redirection and get their permission to follow the redirect.</span></span>
    
- <span data-ttu-id="f245c-189">Envíe una solicitud a la dirección URL y [Compruebe que el certificado SSL presentado por el servidor es válido](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="f245c-189">Send a request to the URL and [verify that the SSL certificate presented by the server is valid](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span>
    
<span data-ttu-id="f245c-190">Si la dirección URL pasa la validación, vuelva a enviar la solicitud a esta nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f245c-190">If the URL passes validation, resend the request to this new URL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f245c-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="f245c-191">See also</span></span>


- [<span data-ttu-id="f245c-192">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="f245c-192">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="f245c-193">Buscar Autodisover extremos mediante el uso de búsqueda de SCP en Exchange</span><span class="sxs-lookup"><span data-stu-id="f245c-193">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [<span data-ttu-id="f245c-194">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f245c-194">ErrorCode (SOAP)</span></span>](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [<span data-ttu-id="f245c-195">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="f245c-195">ErrorCode (POX)</span></span>](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

