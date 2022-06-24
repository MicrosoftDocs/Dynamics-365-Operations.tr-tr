---
title: Toplu işte Varlık kiralama ödeme planlarını onaylama
description: Bu makalede, birden fazla ödeme planının toplu işte nasıl onaylanacağı açıklanmaktadır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd75e22f6407d6bc25a78c1dfeacf70022238e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895065"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Toplu işte Varlık kiralama ödeme planlarını onaylama

[!include [banner](../includes/banner.md)]

Bu makalede, birden fazla ödeme planının toplu işte nasıl onaylanacağı açıklanmaktadır. Ödeme planları, kiralama bazında veya onay toplu iş işlemi aracılığıyla onaylanır. Bir günlük girişi yalnızca onaylanmış bir ödeme planı olan bir kiralama için deftere nakledilebilir. Ödeme planının onayı, kiralamaya ilişkin mali bilgilerin son onayı görevi görür. Kiralamanın mali bilgilerinde yapılacak olan tüm değişiklikler (ör. ödemeler ve kiralama süresi) kiralama düzeltmesi oluşturur ve bu şekilde işlenmelidir.

Birden fazla ödeme planını onaylamak için, aşağıdaki adımları izleyin.

1. **Varlık kiralama \> Periyodik \> Onay toplu işi** bölümüne gidin.
2. **Onay toplu işi** sayfasında **Onay toplu işi**'ni seçin.
3. Görüntülenen iletişim kutusunda onaylamak istediğiniz defterlere filtre uygulayın.

    - Belirli bir kiralama grubundaki tüm defterleri onaylamak için **Kiralama grubu** alanında grubu seçin.
    - Belirli defterleri onaylamak için **Defter Kimliği** alanında defterleri seçin.
    - Tüm defterleri onaylamak için **Tüm defterler için** parametresini açın.

Yeni onaylanan defterlerle ilgili bilgiler **Onaylanan defterler** sayfasında gösterilir. Ödeme planları onaylandıktan sonra, kiralamalara göre ilk kabul günlüğü girişleri deftere nakledilebilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
