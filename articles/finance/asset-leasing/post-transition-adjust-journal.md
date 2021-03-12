---
title: Varlık kiralamasında geçiş sonrası düzeltme günlük girişleri
description: Bu konu, bir kiralama portföyünü yeni kiralama muhasebesini standartlarına, Muhasabe Standartları Kodlaması Konu 842 (ASC 842) ve Uluslararası Mali Raporlama Standardı 16 (IFRS 16) geçirmenizi sağlayan işlevi açıklamaktadır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51ae41e22507d77f32b8b0f4685cce797fd19cff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969565"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="e6430-103">Varlık kiralamasında geçiş sonrası düzeltme günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="e6430-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6430-104">Bu konu, bir kiralama portföyünü şu yeni kiralama muhasebesi standartlarına geçirmenizi sağlayan işlev açıklanmaktadır: ABD'de Genel Kabul Görmüş Muhasebe İlkeleri'nde (ABD GAAP) standart olan Muhasebe Standartları Kodlaması Konu 842 (ACS 842) ile Uluslararası Mali Raporlama Standardı 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="e6430-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="e6430-105">Yeni standartlara geçiş için bir defter ayarlama hakkında bilgi için bkz. [Kiralama defterleri ayarlama](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="e6430-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="e6430-106">Bir geçiş düzeltme günlüğü girişi oluşturduğunuzda bir günlük girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e6430-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="e6430-107">Bu giriş, belirli bir tarihte kiralamayı yeni standartlar kapsamında kaydetmenin bilançoya etkisini yansıtır.</span><span class="sxs-lookup"><span data-stu-id="e6430-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="e6430-108">İlgili varlık hesabı söz konusu tarihteki defter tutarı için borçlandırılır ve yükümlülük hesabı alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="e6430-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="e6430-109">Fark, dağıtılmamış kazançlara borç veya alacak olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="e6430-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="e6430-110">Bir geçiş düzeltmesini yeni muhasebe standartlarıyla uyumlu olarak deftere nakletmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e6430-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="e6430-111">**Kiralama özeti** sayfasında bir kiralama seçin ve ardından **Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e6430-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="e6430-112">Defterde, **Ödeme planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="e6430-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="e6430-113">**Ödeme planı** iletişim kutusunda **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e6430-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="e6430-114">Ardından iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="e6430-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="e6430-115">**Geçiş düzeltmesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e6430-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6430-116">Geçiş düzeltmesi, yalnızca **Geçiş defteri** alanının kullanılabilir olduğu bir deftere atanan kiralama defterleri için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="e6430-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="e6430-117">**Kiralama başlangıç** alanındaki değer geçiş tarihinden sonra ise, **Geçiş düzeltme** alanındaki değer güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="e6430-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="e6430-118">Günlük girişini görüntülemek için **Varlık kiralama günlükleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e6430-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="e6430-119">Yeni günlüğü seçin ve ardından **Deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e6430-119">Select the new journal, and then select **Post**.</span></span>
