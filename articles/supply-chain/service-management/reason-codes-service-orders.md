---
title: Servis siparişleri için neden kodları
description: Bir servis siparişinin aşaması güncelleştirildiğinde servis siparişinin durumunu açıklamaya yardımcı olması için neden kodlarını kullanın.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b059ad5b2ea9cd577624355cf17925cfb9b4867b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258530"
---
# <a name="reason-codes-for-service-orders"></a><span data-ttu-id="e3290-103">Servis siparişleri için neden kodları</span><span class="sxs-lookup"><span data-stu-id="e3290-103">Reason codes for service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e3290-104">Bir servis siparişinin aşaması güncelleştirildiğinde servis siparişinin durumunu açıklamaya yardımcı olması için neden kodlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3290-104">You can use reason codes to help explain the status of a service order when the stage of a service order is updated.</span></span> <span data-ttu-id="e3290-105">Örneğin, bir servis siparişini iptal ederseniz iptal için bir neden kodu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3290-105">For example, if you cancel a service order, you can select a reason code for the cancellation.</span></span>

<span data-ttu-id="e3290-106">Servis siparişinin ilerlemesiyle izlemek için kullanılan neden kodları hakkındaki bilgileri görüntülemek için, Servis siparişi ilerlemesi raporunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="e3290-106">To view information about reason codes that are used to track the progress of service orders, run the Service order progress report.</span></span> <span data-ttu-id="e3290-107">Bu raporda, aşamalarına bakılmaksızın tüm servis siparişleri ve bir servis siparişi aşaması güncelleştirildiğinde belirtilen neden kodları listelenir.</span><span class="sxs-lookup"><span data-stu-id="e3290-107">This report lists all service orders, regardless of their stage, and the reason codes that are specified when a service order stage is updated.</span></span>

## <a name="turn-reason-codes-on-or-off"></a><span data-ttu-id="e3290-108">Neden kodlarını açma veya kapatma</span><span class="sxs-lookup"><span data-stu-id="e3290-108">Turn reason codes on or off</span></span>

<span data-ttu-id="e3290-109">Neden kodları isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e3290-109">Reason codes are optional.</span></span> <span data-ttu-id="e3290-110">Servis siparişini belirli bir servis aşamasına güncelleştirdiğinizde bir neden kodunun gerekli olup olmayacağına karar verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3290-110">You can decide whether to require a reason code when you update a service order to a specific service stage.</span></span>

1.  <span data-ttu-id="e3290-111">**Servis yönetimi** \> **Kurulum** \> **Servis siparişleri** \> **Servis aşamaları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3290-111">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="e3290-112">**Servis aşamaları** formunda bir servis aşaması seçin ve sonra servis aşaması için **Neden** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e3290-112">In the **Service stages** form, select a service stage, and then select the **Reason** check box for the service stage.</span></span>

3.  <span data-ttu-id="e3290-113">Değişikliklerinizi kaydetmek için formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="e3290-113">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3290-114">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="e3290-114">See also</span></span>

[<span data-ttu-id="e3290-115">Servis siparişi aşamalarını ayarla</span><span class="sxs-lookup"><span data-stu-id="e3290-115">Set up service order stages</span></span>](set-up-service-order-stages.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]