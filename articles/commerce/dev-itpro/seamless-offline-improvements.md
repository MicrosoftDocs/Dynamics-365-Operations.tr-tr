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
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Hediye kartı ve alacak faturası işlemleri için sorunsuz çevrimdışı geçiş

[!include [banner](../includes/banner.md)]

Bir satış noktası (POS) aygıtının, kanal veritabanıyla olan bağlantısını kaybederse, kasiyerin bağlantı kaybı ile ilgili bir uyarı iletisi aldıktan sonra sürmekte olan POS işlemleri ve hareketlerinin çoğu devam edebilir. Ancak, bazı durumlarda, hareketler gerçek zamanlı servise bağlı olan öğelere sahiptir ve POS çevrimdışıyken bu öğeler desteklenmez. Bu konu, bu senaryolarda kaybedilen bağlantının etkisini azaltmaya yardımcı olan bazı işlevleri açıklamaktadır.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>Çevrimdışı modda hediye kartı hareketlerinin sonuçlandırma

Dahili hediye kartları gerçek zamanlı servise bağlıdır, çünkü hediye kartlarının bakiyesi Microsoft Dynamics 365 Commerce Headquarters 'da merkezi olarak tutulmalıdır. Dolandırıcılık veya diğer eşitleme sorunlarını önlemeye yardımcı olmak için, hediye kartları bir hareketle eklendikten hemen sonra kilitlenir. Kilitleme işlevi, bir hediye kartının aynı anda çoklu terminallerde kullanılmamasını sağlar. Hareket tamamlandığında, hediye kartının kilidi güncellenir ve kilidi açılır.

Ancak, POS bir harekette bir hediye kartı eklendikten sonra bağlantıyı kaybederse, hediye kartı kullanılamaz hale gelebilir. Bu durumun engellenmesine yardımcı olmak için Dynamics 365 Commerce, POS çevrimdışıyken hediye kartı satırı içeren hareketlerin tamamlanmasını sağlayan bir parametresi vardır. Bu parametre etkinleştirildiğinde, çevrimdışı olarak zorlanan hediye kartı hareketleri, çevrimdışı hareketlerle birlikte kaydedilir ve çevrimdışı hareketler eşitlendiğinde Commerce Headquarters ile eşitlenir. Eşitleme, başka bir terminalde kullanılabilmesi için hediye kartının kilidini da kaldırır.

Çevrimdışı moda geçtikten sonra hediye kartı hareketlerinin sona erdikten sonra işlevselliğin etkinleştirilmesi için **Commerce parametreleri** sayfasındaki **deftere nakil** sekmesine gidin. Bu sekmede, **hediye kartı** hızlı sekmesini bulun ve **çevrimdışı modda sonuçlan hediye kartı hareketlerini** **Evet** olarak ayarlayın.

![Çevrimdışı hediye kartı ayarı](../media/gift.png)

Commerce parametreleri genellikle önbelleğe alınır. Bu nedenle, bu parametrenin ayarı güncelleştirildikten ve dağıtım zamanlaması, değişikliğin kanalla eşitlenmesi için başlatıldığından, değişikliğin etkili olması 24 saate kadar sürebilir. Değişikliğin hemen etkili olması için, Microsoft Internet Information Services'ı (IIS) sıfırlayın.

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>Çevrimdışı modda alacak faturasıyla hareketlerinin sonuçlandırma

Dahili hediye kartları gibi, iade faturaları da Commerce Headquarters'da merkezi olarak tutulur. Ticaret için POS çevrimdışıyken iade faturası hareketlerinin tamamlanmasını sağlayan bir parametre vardır. Bu parametre, önceki bölümde sözü edilen hediye kartı parametresi gibi çalışır. Parametre açıldığında, çevrimdışı duruma getirilen iade faturası hareketleri, POS çevrimdışıyken gerçekleştirilen diğer hareketlerle birlikte kanal veritabanına geri eşitlenir.

Çevrimdışı moda geçtikten sonra alacak faturasıyla hareketlerinin sona erdikten sonra işlevselliğin etkinleştirilmesi için **Commerce parametreleri** sayfasındaki **deftere nakil** sekmesine gidin. Bu sekmede, **Alacak Faturası** hızlı sekmesini bulun ve **çevrimdışı modda sonuçlan alacak faturası hareketlerini** **Evet** olarak ayarlayın.

![Çevrimdışı iade faturası ayarı](../media/creditmemo.png)

Commerce parametreleri genellikle önbelleğe alınır. Bu nedenle, bu parametrenin ayarı güncelleştirildikten ve dağıtım zamanlaması, değişikliğin kanalla eşitlenmesi için başlatıldığından, değişikliğin etkili olması 24 saate kadar sürebilir. Değişikliğin hemen etkin hale getirmek için IIS'yi sıfırlayın.

## <a name="related-topics"></a>İlgili konular

- [Çevrimdışı satış noktası (POS) işlevleri](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [Çevrimiçi ve çevrimdışı satış noktası (POS) işlemleri](https://docs.microsoft.com/dynamics365/retail/pos-operations)
