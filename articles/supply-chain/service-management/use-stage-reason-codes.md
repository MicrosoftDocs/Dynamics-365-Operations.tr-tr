---
title: "Aşama neden kodlarını kullanma"
description: "Bir servis düzeyi sözleşmesinin (SLA) neden iptal edildiğini veya bir servis siparişinin SLA'da tanımlanan süre limitini neden aştığını belirtmek için bir neden kodu kullanırsınız."
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 33fa7e5f08f09fe109d0507d686315d01e043928
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---


# <a name="use-stage-reason-codes"></a><span data-ttu-id="b301a-103">Aşama neden kodlarını kullanma</span><span class="sxs-lookup"><span data-stu-id="b301a-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b301a-104">Bir servis düzeyi sözleşmesinin (SLA) neden iptal edildiğini veya bir servis siparişinin SLA'da tanımlanan süre limitini neden aştığını belirtmek için bir neden kodu kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="b301a-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="b301a-105">Ayrıca SLA iptal edildiğinde veya süre limiti servis siparişi için SLA'da belirtilen süreyi aştığında bir neden kodunun gerekli olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b301a-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="b301a-106">Neden kodunun gerekli olduğunu belirttiyseniz, aşağıdaki durumlarda bir neden kodu girmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="b301a-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="b301a-107">Servis siparişi, servis siparişine yönelik SLA'ya karşı zaman kaydını durduran bir aşamaya geldiğinde.</span><span class="sxs-lookup"><span data-stu-id="b301a-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="b301a-108">Servis siparişi imzalandığında.</span><span class="sxs-lookup"><span data-stu-id="b301a-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="b301a-109">Zaman kaydı el ile durdurulduğunda.</span><span class="sxs-lookup"><span data-stu-id="b301a-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="b301a-110">Neden kodlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="b301a-110">Set up reason codes</span></span>

1.  <span data-ttu-id="b301a-111">**Servis yönetimi** \> **Kurulum** \> **Servis siparişleri** \> **Aşama neden kodları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b301a-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="b301a-112">**Aşama neden kodları** formunda, **Yeni**'ye tıklayarak yeni bir neden kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b301a-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="b301a-113">**Aşama neden kodu** alanına, benzersiz bir aşama neden kodu girin.</span><span class="sxs-lookup"><span data-stu-id="b301a-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="b301a-114">**Açıklama** alanına, aşama neden kodu açıklaması girin.</span><span class="sxs-lookup"><span data-stu-id="b301a-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="b301a-115">Değişikliklerinizi kaydetmek için formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="b301a-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="b301a-116">Bir servis düzeyi anlaşması iptal edildiğinde neden kodu gerektirme</span><span class="sxs-lookup"><span data-stu-id="b301a-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="b301a-117">**Servis yönetimi** \> **Kurulum** \> **Servis yönetimi parametreleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b301a-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="b301a-118">**Servis yönetimi parametreleri** formunda, **Genel** bağlantısına tıklayın ve sonra **İptal durumunda neden kodu** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b301a-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="b301a-119">Servis siparişi, servis düzeyi sözleşmesi tarafından ayarlanan süre limitini aştığından neden kodu gerektir</span><span class="sxs-lookup"><span data-stu-id="b301a-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="b301a-120">**Servis yönetimi** \> **Kurulum** \> **Servis yönetimi parametreleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b301a-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="b301a-121">**Servis yönetimi parametreleri** formunda, **Genel** bağlantısına tıklayın ve sonra **Süre aşımında neden kodu** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b301a-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="b301a-122">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b301a-122">See also</span></span>

[<span data-ttu-id="b301a-123">Servis siparişinde zaman kaydını başlatma ve durdurma</span><span class="sxs-lookup"><span data-stu-id="b301a-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  



