---
title: Kiralama günlüğü adlarını ayarlama
description: Bu konu, kiralama günlüğü adlarının nasıl tanımlanacağını açıklamaktadır. Kiralama günlüğü adları, Varlık kiralamada girişlerin nakledildiği günlükleri belirtir.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1ea35ec40ddd459e1a9e7641557147e23fe45d3e
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343226"
---
# <a name="set-up-lease-journal-names"></a>Kiralama günlüğü adlarını ayarlama

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Kiralama günlüğü adları, Varlık kiralama hareketlerinin nakledildiği günlükleri belirtir. Yalnızca **Varlık kiralama** günlük türüne atanmış günlük adları, **Varlık kiralama parametreleri** sayfasında **İlk Kabul** ve **Aylık Günlük Adı** alanlarında gösterilir. Yalnızca **satıcı faturası kaydı** günlük türü **Satıcı günlüğü adı** alanına atanabilir.

Sistem, hareketler ve zamanlamalar arasındaki farkları önlemek için belirli mali alanların düzenlenmesini kilitler. Kilitlenen bazı alanlar şunlardır: **Hesap**, **Tutarlar**, **Mali boyutlar**, **Para birimi** ve **Hareket türü**. Ayrıca zamanlamalar ve hareketler arasında farklara neden olabileceğinden Varlık kiralama yevmiye defteri girişlerine yevmiye defteri girişi satırları ekleyemez veya bunları silemezsiniz.


Kiralama günlüğü adlarını yapılandırmak için aşağıdaki adımları izleyin.

1. **Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**'ne gidin.
2. **Genel** sekmesindeki **İlk kabul günlük adı** alanında bir günlük seçin. Tüm ilk kabul günlüğü girişleri bu günlük adına nakledilecek.
3. **Fatura günlük adı** alanında, bir günlük seçin. Kiralama defteri için **Satıcıya öde** seçeneği **Evet** olarak ayarlanmışsa kiralama ve gider ödeme faturaları bu günlük adına nakledilir.
4. **Kiralama günlüğü adı** alanında, bir günlük seçin. Tüm amortisman, faiz ve kısa süreli yeniden sınıflama girişleri bu günlük adına nakledilecek. Kiralama defteri için **Satıcıya öde** seçeneği **Hayır** olarak ayarlanmışsa kira ödemeleri ve gider ödeme girişleri de bu günlük adına nakledilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
