---
title: Toplu işte Varlık kiralama ödeme planlarını onaylama
description: Bu konuda, birden fazla ödeme planının toplu işte nasıl onaylanacağı açıklanmaktadır.
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
ms.openlocfilehash: 0275fda306a58159a982b342622b9b6a18fa5b71
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225531"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Toplu işte Varlık kiralama ödeme planlarını onaylama

[!include [banner](../includes/banner.md)]

Bu konuda, birden fazla ödeme planının toplu işte nasıl onaylanacağı açıklanmaktadır. Ödeme planları, kiralama bazında veya onay toplu iş işlemi aracılığıyla onaylanır. Bir günlük girişi yalnızca onaylanmış bir ödeme planı olan bir kiralama için deftere nakledilebilir. Ödeme planının onayı, kiralamaya ilişkin mali bilgilerin son onayı görevi görür. Kiralamanın mali bilgilerinde yapılacak olan tüm değişiklikler (ör. ödemeler ve kiralama süresi) kiralama düzeltmesi oluşturur ve bu şekilde işlenmelidir.

Birden fazla ödeme planını onaylamak için, aşağıdaki adımları izleyin.

1. **Varlık kiralama \> Periyodik \> Onay toplu işi** bölümüne gidin.
2. **Onay toplu işi** sayfasında **Onay toplu işi**'ni seçin.
3. Görüntülenen iletişim kutusunda onaylamak istediğiniz defterlere filtre uygulayın.

    - Belirli bir kiralama grubundaki tüm defterleri onaylamak için **Kiralama grubu** alanında grubu seçin.
    - Belirli defterleri onaylamak için **Defter Kimliği** alanında defterleri seçin.
    - Tüm defterleri onaylamak için **Tüm defterler için** parametresini açın.

Yeni onaylanan defterlerle ilgili bilgiler **Onaylanan defterler** sayfasında gösterilir. Ödeme planları onaylandıktan sonra, kiralamalara göre ilk kabul günlüğü girişleri deftere nakledilebilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]