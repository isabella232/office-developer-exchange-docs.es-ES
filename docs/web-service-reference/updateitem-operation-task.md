---
title: Operación UpdateItem (tarea)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: La operación UpdateItem se utiliza para actualizar las propiedades del elemento de tarea en el almacén de Exchange.
ms.openlocfilehash: d6f966fa663300b476383a136d30cf611d6bfb9b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840840"
---
# <a name="updateitem-operation-task"></a><span data-ttu-id="eb2b3-103">Operación UpdateItem (tarea)</span><span class="sxs-lookup"><span data-stu-id="eb2b3-103">UpdateItem operation (task)</span></span>

<span data-ttu-id="eb2b3-104">La operación UpdateItem se utiliza para actualizar las propiedades del elemento de tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-104">The UpdateItem operation is used to update task item properties in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb2b3-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb2b3-105">Remarks</span></span>

<span data-ttu-id="eb2b3-106">No puede usar servicios Web de Exchange para enviar solicitudes de tareas.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-106">You cannot use Exchange Web Services to send task requests.</span></span> <span data-ttu-id="eb2b3-107">Servicios Web de Exchange puede devolver las solicitudes de tarea que se crean de forma MicrosoftOfficeOutlook.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-107">Exchange Web Services can return task requests that are created by MicrosoftOfficeOutlook.</span></span> <span data-ttu-id="eb2b3-108">Si ya se ha enviado una solicitud de tarea, una solicitud para actualizar la tarea devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-108">If a task request has already been sent, a request to update the task will return an error.</span></span>
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a><span data-ttu-id="eb2b3-109">Actualizar la aparición actual de una tarea periódica</span><span class="sxs-lookup"><span data-stu-id="eb2b3-109">Updating the Current Occurrence of a Recurring Task</span></span>

<span data-ttu-id="eb2b3-110">El resultado de una operación UpdateItem en tareas repetitivas difiere el resultado de la operación UpdateItem en una sola tarea no periódica.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-110">The result of an UpdateItem operation on recurring tasks differs from the result of the UpdateItem operation on a single, nonrecurring task.</span></span> <span data-ttu-id="eb2b3-111">Los cambios realizados en una ocurrencia de una tarea periódica que constituye tareas se generan cuando se realizan las siguientes actualizaciones:</span><span class="sxs-lookup"><span data-stu-id="eb2b3-111">Changes to an occurrence of a recurring task cause one-off tasks to be generated when the following updates are made:</span></span>
  
1. <span data-ttu-id="eb2b3-112">La propiedad de estado de una tarea periódica regenerada o nonregenerating se establece como **completada**.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-112">The status property of a regenerating or nonregenerating recurrent task is set to **Completed**.</span></span>
    
2. <span data-ttu-id="eb2b3-113">Se cambia la fecha de comienzo o fecha de finalización de una tarea periódica nonregenerating.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-113">The start date or end date of a nonregenerating recurrent task is changed.</span></span>
    
<span data-ttu-id="eb2b3-114">Por ejemplo, si una solicitud **UpdateItem** establece el valor de completado de una tarea periódica en **true**, la **UpdateItemResponse** incluirá un nuevo identificador y ChangeKey que representan una tarea de uso único recién creada.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-114">For example, if an **UpdateItem** request sets the Completed value of a recurring task to **true**, the **UpdateItemResponse** will include a new Id and ChangeKey that represent a newly created one-off task.</span></span> <span data-ttu-id="eb2b3-115">El identificador que se ha incluido en la solicitud todavía es válido y se ha actualizado la tarea periódica que está representada por el Id para representar la siguiente aparición.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-115">The Id that was included in the request is still valid and the recurring task that is represented by that Id has been updated to represent the next occurrence.</span></span> <span data-ttu-id="eb2b3-116">El ChangeKey que se ha incluido en la solicitud ya no es válido porque se ha actualizado la tarea repetitiva.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-116">The ChangeKey that was included in the request is no longer valid because the recurring task has been updated.</span></span> 
  
<span data-ttu-id="eb2b3-117">Puede usar la [operación GetItem](getitem-operation.md) para obtener la más reciente **ChangeKey** para la tarea repetitiva.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-117">You can use the [GetItem operation](getitem-operation.md) to get the latest **ChangeKey** for the recurring task.</span></span> 
  
<span data-ttu-id="eb2b3-118">Para las tareas no periódicas o la última aparición de una tarea periódica, la respuesta UpdateItem devuelve el mismo **identificador** que se pasó a ella y devuelve que el asociado actualizó **ChangeKey**.</span><span class="sxs-lookup"><span data-stu-id="eb2b3-118">For nonrecurring tasks or for the last occurrence of a recurring task, the UpdateItem response returns the same **Id** that was passed to it and returns the associated updated **ChangeKey**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb2b3-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb2b3-119">See also</span></span>



[<span data-ttu-id="eb2b3-120">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="eb2b3-120">UpdateItem operation</span></span>](updateitem-operation.md)

