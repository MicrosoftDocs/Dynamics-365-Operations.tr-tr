---
title: Periyodik alacak yönetimi görevleri
description: Bu konu, müşteriler için kredi limitlerini yönetme sürecinin gerekli bir parçası olan periyodik görevleri açıklamaktadır.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5e5d1ad7b0b151d67bd96513e9ce0c82c172a601
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835304"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="e1ad7-103">Periyodik alacak yönetimi görevleri</span><span class="sxs-lookup"><span data-stu-id="e1ad7-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1ad7-104">Bu konu, müşteriler için kredi limitlerini yönetme sürecinin gerekli bir parçası olan periyodik görevleri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="e1ad7-105">Risk puanlarını güncelleştir</span><span class="sxs-lookup"><span data-stu-id="e1ad7-105">Update risk scores</span></span>

<span data-ttu-id="e1ad7-106">İşler gelişip koşullar değişince, belirli bir müşteriyle ilgili kredi riskleri de değişebilir.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="e1ad7-107">Müşterileriniz için uygun kredi limitlerini korumaya yardımcı olmak amacıyla, her risk puanı için ölçütleri düzenli olarak gözden geçirmeniz ve her müşteri için puanları güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="e1ad7-108">Aşağıdaki puanları **Risk puanlarını güncelleştir** sayfasını (**Alacak ve tahsilatlar \> Periyodik görevler \> Kredi yönetimi \> Riski puanlarını güncelleştir**) kullanarak güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="e1ad7-109">Ayrıca tüm kullanıcı tanımlı hesaplamalar da işlenir.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="e1ad7-110">**Ortalama ödeme gün sayısı** – Bu puan, bir müşterinin ödeme için beklettiği ortalama gün sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="e1ad7-111">**Müşterilik başlangıç tarihi** – Bu puan, bir müşterinin kuruluşunuzun müşterisi olduğu yıl sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="e1ad7-112">**Sektöre giriş tarihi** Bu puan, müşterinin sektörde bulunduğu yıl sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="e1ad7-113">Bu puan, **Müşteriler** sayfasındaki **İş başlangıcı** alanının değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="e1ad7-114">**Bekleyen satış gün sayısı** – Bu puan, önceki 12 aylık dönemdeki alacak hesapları bakiyesine, satış gelirine ve gün sayısına dayanır.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="e1ad7-115">**Ortalama bakiye** – Bu puan, önceki 12 aylık dönem için alacak hesapları bakiyesine dayanır.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="e1ad7-116">**Kredi yönetimi grubu**, **Hesap durumu** ve **Ülke** – Bu puanlar, müşteriden gelen bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="e1ad7-117">Müşteri bakiye istatistiklerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e1ad7-117">Update customer balance statistics</span></span>

<span data-ttu-id="e1ad7-118">**Bakiye istatistikleri sorgusu** sayfasında gösterilen bakiye istatistiklerinin hesaplamasını güncelleştirmek için **Müşteri bakiyesi istatistiklerini güncelleştir** işlemini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="e1ad7-119">Bu bilgiler, risk puanlarını ve **Müşteri** sayfasındaki kredi istatistikleri bilgi kutularında gösterilen değerleri hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="e1ad7-120">İşlemi çalıştırdığınızda, tek bir müşteriyle ilgili müşteri bakiyesi istatistiklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="e1ad7-121">İşlemi birden fazla müşteri için yapmak üzere bir toplu iş ayarlamak için, **Bakiye istatistiklerini hesapla** sayfasını (**Kredi yönetimi \> Periyodik görevler \> Bakiye istatistiklerini hesapla**) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]