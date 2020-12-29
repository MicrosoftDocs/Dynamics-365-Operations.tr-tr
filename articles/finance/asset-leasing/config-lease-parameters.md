---
title: Kiralama parametrelerini yapılandırma (Önizleme)
description: Bu konuda, Varlık kiralamayla ilgili yapılandırma ayarları (ör. güvenlik bilgileri ve muhasebe ayarları) açıklanmaktadır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449015"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="eb048-103">Kiralama parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="eb048-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb048-104">Birçok yapılandırma ayarı, Varlık kiralamanın davranışını etkiler.</span><span class="sxs-lookup"><span data-stu-id="eb048-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="eb048-105">Bu ayarlar günlük adlarını, genel parametreleri ve deftere nakil profili ayarlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="eb048-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="eb048-106">**Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="eb048-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="eb048-107">**Kiralamalar** sekmesinde, **Genel** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="eb048-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="eb048-108">**El ile sınıflandırmayı geçersiz kılmaya izin ver** parametresi, ödeme planı onaylanmadan önce kiralama sınıflandırmasının geçersiz kılınıp kılınamayacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="eb048-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="eb048-109">**Tüzel kişilikler arası toplu iş** parametresi, geçerli tüzel kişilikten diğer tüzel kişiliklerin defterine nakil yapıp yapamayacağınızı belirler.</span><span class="sxs-lookup"><span data-stu-id="eb048-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="eb048-110">Bu parametre açıksa erişiminiz olan tüzel kişilikler için günlük girişleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb048-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="eb048-111">Ödeme planları onaylanan kiralamaların silinmesine izin vermek için **Onaylanan kiralamaların silinmesine izin ver** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb048-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="eb048-112">Bu seçeneğin ayarı ne olursa olsun, kiralamalar ile deftere nakledilen veya nakledilmeyen hareketler ilişkilendirilmişse kiralamalar silinemez.</span><span class="sxs-lookup"><span data-stu-id="eb048-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="eb048-113">Bir kiralama kaydını silindikten sonra geri alamazsınız.</span><span class="sxs-lookup"><span data-stu-id="eb048-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="eb048-114">Silinen bir kiralama için el ile veya veri kaynakları üzerinden kayıt yüklerseniz, yüklenen bilgiler mevcut bir kiralamanın güncelleştirilmesi olarak değil yeni bir kiralama olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="eb048-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="eb048-115">Bu seçeneği **Evet** olarak ayarlarsanız ve defterin hareket türü **Kümülatif Yakalama Seçeneği A veya B** ise sistem, **Alternatif borçlanma oranı** alanını **Defter kurulumu** sayfasındaki **Geçişte alternatif borçlanma oranı** değerine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="eb048-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="eb048-116">Bu seçenek **Hayır** olarak ayarlanırsa, defterin geçiş türüne bakılmaksızın, üst kiralamadaki oran **Defter ayrıntıları** sayfasındaki **Alternatif borçlanma oranı** alanının değerine ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="eb048-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="eb048-117">Amortisman gider hareketlerinin tersine çevrilmesine izin vermek için **Kapalı defter sürümünde amortisman ters işlemlerine izin ver** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb048-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="eb048-118">Defter sürümü kapalı olsa bile gider hareketleri tersine çevrilebilir.</span><span class="sxs-lookup"><span data-stu-id="eb048-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eb048-119">Bu seçeneği **Hayır** olarak tutmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="eb048-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="eb048-120">Bu seçeneğin ayarı, kapatılmış bir defter sürümüne yanlışlıkla amortisman uygulanmasını önlemek için doğrulama ve denetim amaçlı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="eb048-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="eb048-121">Seçenek **Hayır** olarak kaldığında, net defter değerinin ve gelecekteki amortisman hesaplamalarının doğru olmasına yardımcı olursunuz.</span><span class="sxs-lookup"><span data-stu-id="eb048-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>
