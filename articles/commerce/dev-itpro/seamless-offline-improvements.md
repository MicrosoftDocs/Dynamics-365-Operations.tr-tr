---
title: Hediye kartı ve alacak faturası işlemleri için sorunsuz çevrimdışı geçiş
description: Bu konu, belirli ödeme tipleri için kesintisiz bir çevrimdışı anahtar sağlayan gelişmelere genel bakış sağlar.
author: rubendel
manager: AnnBe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 3c2a644fd7096668fcefc73c67068fccde6894b0
ms.sourcegitcommit: 472f8bfc02acf80b07caf7c53bbb397411e946cc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/11/2020
ms.locfileid: "3040245"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="57282-103">Hediye kartı ve alacak faturası işlemleri için sorunsuz çevrimdışı geçiş</span><span class="sxs-lookup"><span data-stu-id="57282-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57282-104">Bir satış noktası (POS) aygıtının, kanal veritabanıyla olan bağlantısını kaybederse, kasiyerin bağlantı kaybı ile ilgili bir uyarı iletisi aldıktan sonra sürmekte olan POS işlemleri ve hareketlerinin çoğu devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="57282-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="57282-105">Ancak, bazı durumlarda, hareketler gerçek zamanlı servise bağlı olan öğelere sahiptir ve POS çevrimdışıyken bu öğeler desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="57282-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="57282-106">Bu konu, bu senaryolarda kaybedilen bağlantının etkisini azaltmaya yardımcı olan bazı işlevleri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="57282-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="57282-107">Çevrimdışı modda hediye kartı hareketlerinin sonuçlandırma</span><span class="sxs-lookup"><span data-stu-id="57282-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="57282-108">Dahili hediye kartları gerçek zamanlı servise bağlıdır, çünkü hediye kartlarının bakiyesi Microsoft Dynamics 365 Commerce Headquarters 'da merkezi olarak tutulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="57282-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="57282-109">Dolandırıcılık veya diğer eşitleme sorunlarını önlemeye yardımcı olmak için, hediye kartları bir hareketle eklendikten hemen sonra kilitlenir.</span><span class="sxs-lookup"><span data-stu-id="57282-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="57282-110">Kilitleme işlevi, bir hediye kartının aynı anda çoklu terminallerde kullanılmamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="57282-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="57282-111">Hareket tamamlandığında, hediye kartının kilidi güncellenir ve kilidi açılır.</span><span class="sxs-lookup"><span data-stu-id="57282-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="57282-112">Ancak, POS bir harekette bir hediye kartı eklendikten sonra bağlantıyı kaybederse, hediye kartı kullanılamaz hale gelebilir.</span><span class="sxs-lookup"><span data-stu-id="57282-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="57282-113">Bu durumun engellenmesine yardımcı olmak için Dynamics 365 Commerce, POS çevrimdışıyken hediye kartı satırı içeren hareketlerin tamamlanmasını sağlayan bir parametresi vardır.</span><span class="sxs-lookup"><span data-stu-id="57282-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="57282-114">Bu parametre etkinleştirildiğinde, çevrimdışı olarak zorlanan hediye kartı hareketleri, çevrimdışı hareketlerle birlikte kaydedilir ve çevrimdışı hareketler eşitlendiğinde Commerce Headquarters ile eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="57282-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="57282-115">Eşitleme, başka bir terminalde kullanılabilmesi için hediye kartının kilidini da kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57282-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="57282-116">Çevrimdışı moda geçtikten sonra hediye kartı hareketlerinin sona erdikten sonra işlevselliğin etkinleştirilmesi için **Commerce parametreleri** sayfasındaki **deftere nakil** sekmesine gidin.</span><span class="sxs-lookup"><span data-stu-id="57282-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="57282-117">Bu sekmede, **hediye kartı** hızlı sekmesini bulun ve **çevrimdışı modda sonuçlan hediye kartı hareketlerini** **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="57282-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![Çevrimdışı hediye kartı ayarı](../media/gift.png)

<span data-ttu-id="57282-119">Commerce parametreleri genellikle önbelleğe alınır.</span><span class="sxs-lookup"><span data-stu-id="57282-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="57282-120">Bu nedenle, bu parametrenin ayarı güncelleştirildikten ve dağıtım zamanlaması, değişikliğin kanalla eşitlenmesi için başlatıldığından, değişikliğin etkili olması 24 saate kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="57282-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="57282-121">Değişikliğin hemen etkili olması için, Microsoft Internet Information Services'ı (IIS) sıfırlayın.</span><span class="sxs-lookup"><span data-stu-id="57282-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="57282-122">Çevrimdışı modda alacak faturasıyla hareketlerinin sonuçlandırma</span><span class="sxs-lookup"><span data-stu-id="57282-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="57282-123">Dahili hediye kartları gibi, iade faturaları da Commerce Headquarters'da merkezi olarak tutulur.</span><span class="sxs-lookup"><span data-stu-id="57282-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="57282-124">Ticaret için POS çevrimdışıyken iade faturası hareketlerinin tamamlanmasını sağlayan bir parametre vardır.</span><span class="sxs-lookup"><span data-stu-id="57282-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="57282-125">Bu parametre, önceki bölümde sözü edilen hediye kartı parametresi gibi çalışır.</span><span class="sxs-lookup"><span data-stu-id="57282-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="57282-126">Parametre açıldığında, çevrimdışı duruma getirilen iade faturası hareketleri, POS çevrimdışıyken gerçekleştirilen diğer hareketlerle birlikte kanal veritabanına geri eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="57282-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="57282-127">Çevrimdışı moda geçtikten sonra alacak faturasıyla hareketlerinin sona erdikten sonra işlevselliğin etkinleştirilmesi için **Commerce parametreleri** sayfasındaki **deftere nakil** sekmesine gidin.</span><span class="sxs-lookup"><span data-stu-id="57282-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="57282-128">Bu sekmede, **Alacak Faturası** hızlı sekmesini bulun ve **çevrimdışı modda sonuçlan alacak faturası hareketlerini** **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="57282-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![Çevrimdışı iade faturası ayarı](../media/creditmemo.png)

<span data-ttu-id="57282-130">Commerce parametreleri genellikle önbelleğe alınır.</span><span class="sxs-lookup"><span data-stu-id="57282-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="57282-131">Bu nedenle, bu parametrenin ayarı güncelleştirildikten ve dağıtım zamanlaması, değişikliğin kanalla eşitlenmesi için başlatıldığından, değişikliğin etkili olması 24 saate kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="57282-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="57282-132">Değişikliğin hemen etkin hale getirmek için IIS'yi sıfırlayın.</span><span class="sxs-lookup"><span data-stu-id="57282-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57282-133">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="57282-133">Related topics</span></span>

- [<span data-ttu-id="57282-134">Çevrimdışı satış noktası (POS) işlevleri</span><span class="sxs-lookup"><span data-stu-id="57282-134">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [<span data-ttu-id="57282-135">Çevrimiçi ve çevrimdışı satış noktası (POS) işlemleri</span><span class="sxs-lookup"><span data-stu-id="57282-135">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-operations)
