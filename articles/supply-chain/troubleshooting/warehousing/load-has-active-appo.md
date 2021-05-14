---
title: Takvimdeki bir sorun nedeniyle sevkiyatı onaylayamıyorsunuz
description: Takvimdeki bir sorun nedeniyle sevkiyatı onaylayamıyorsunuz
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938569"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="5d90b-103">Takvimdeki bir sorun nedeniyle sevkiyatı onaylayamıyorsunuz</span><span class="sxs-lookup"><span data-stu-id="5d90b-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="5d90b-104">Hata kodu: TRX2716</span><span class="sxs-lookup"><span data-stu-id="5d90b-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="5d90b-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="5d90b-105">Symptoms</span></span>

<span data-ttu-id="5d90b-106">Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="5d90b-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="5d90b-107">Takvim türü %1 randevu %2 için giriş ve çıkış yapılmasını gerektiriyor.</span><span class="sxs-lookup"><span data-stu-id="5d90b-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="5d90b-108">Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="5d90b-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="5d90b-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="5d90b-109">Cause</span></span>

<span data-ttu-id="5d90b-110">Yükleme için etkin randevular mevcut.</span><span class="sxs-lookup"><span data-stu-id="5d90b-110">Active appointments for the load exist.</span></span> <span data-ttu-id="5d90b-111">Örneğin, sürücü girişi gerektiren bir kural vardır.</span><span class="sxs-lookup"><span data-stu-id="5d90b-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="5d90b-112">Bu nedenle, yükleme işlemi şu anda sevkiyat onayının başarısız olduğu bir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="5d90b-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="5d90b-113">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="5d90b-113">Resolution</span></span>

<span data-ttu-id="5d90b-114">Yükleme ile bağlantılı etkin randevularla ilgili tüm sorunları araştırmanız ve düzeltmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5d90b-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="5d90b-115">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="5d90b-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5d90b-116">Sevkiyatın onaylanamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="5d90b-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="5d90b-117">Eylem Bölmesinde **Taşıma** sekmesinde **Randevular** grubunda **Randevu zamanlama** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5d90b-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="5d90b-118">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="5d90b-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="5d90b-119">Randevu için sürücünün giriş/çıkış işlemlerinin tamamlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="5d90b-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="5d90b-120">Randevuyu tamamlayın veya iptal edin.</span><span class="sxs-lookup"><span data-stu-id="5d90b-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="5d90b-121">İlgili randevu kuralı için **Sürücü girişi gerekli** seçeneğini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="5d90b-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
