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
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Varlık kiralamasında geçiş sonrası düzeltme günlük girişleri

[!include [banner](../includes/banner.md)]

Bu konu, bir kiralama portföyünü şu yeni kiralama muhasebesi standartlarına geçirmenizi sağlayan işlev açıklanmaktadır: ABD'de Genel Kabul Görmüş Muhasebe İlkeleri'nde (ABD GAAP) standart olan Muhasebe Standartları Kodlaması Konu 842 (ACS 842) ile Uluslararası Mali Raporlama Standardı 16 (IFRS 16).

Yeni standartlara geçiş için bir defter ayarlama hakkında bilgi için bkz. [Kiralama defterleri ayarlama](set-up-lease-books.md).

Bir geçiş düzeltme günlüğü girişi oluşturduğunuzda bir günlük girişi oluşturulur. Bu giriş, belirli bir tarihte kiralamayı yeni standartlar kapsamında kaydetmenin bilançoya etkisini yansıtır. İlgili varlık hesabı söz konusu tarihteki defter tutarı için borçlandırılır ve yükümlülük hesabı alacaklandırılır. Fark, dağıtılmamış kazançlara borç veya alacak olarak kaydedilir.

Bir geçiş düzeltmesini yeni muhasebe standartlarıyla uyumlu olarak deftere nakletmek için aşağıdaki adımları izleyin.

1. **Kiralama özeti** sayfasında bir kiralama seçin ve ardından **Defterler**'i seçin.
2. Defterde, **Ödeme planı**'nı seçin.
3. **Ödeme planı** iletişim kutusunda **Onayla**'yı seçin. Ardından iletişim kutusunu kapatın.
4. **Geçiş düzeltmesi**'ni seçin.

    > [!NOTE]
    > Geçiş düzeltmesi, yalnızca **Geçiş defteri** alanının kullanılabilir olduğu bir deftere atanan kiralama defterleri için oluşturulabilir. **Kiralama başlangıç** alanındaki değer geçiş tarihinden sonra ise, **Geçiş düzeltme** alanındaki değer güncelleştirilmez.

5. Günlük girişini görüntülemek için **Varlık kiralama günlükleri**'ni seçin.
6. Yeni günlüğü seçin ve ardından **Deftere naklet**'i seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]