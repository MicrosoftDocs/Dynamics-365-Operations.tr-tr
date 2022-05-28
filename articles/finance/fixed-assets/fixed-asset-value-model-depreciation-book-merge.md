---
title: Sabit kıymet değer modeli ve amortisman defteri birleştirme
description: Önceki sürümlerde, sabit kıymetler - değer modelleri ve amortisman defterleri olmak üzere iki değerleme kavramı vardı. Microsoft Dynamics 365 for Operations'ta (1611) sürümünde, değer modeli işlevselliği ve amortisman defteri işlevselliği bir defter olarak bilinen tek bir kavramda birleştirilmiştir.
author: moaamer
ms.date: 10/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e9d937211c049b2ec4ac06ac6eddce7fd9bcb5b0
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720013"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Sabit kıymet değer modeli ve amortisman defteri birleştirme

[!include [banner](../includes/banner.md)]

Bu konu, sabit kıymetlerdeki geçerli defter işlevini açıklamaktadır. Bu özellik, önceki sürümlerde kullanılabilir olan değer modeli işlevselliğini temel alır ancak önceden yalnızca amortisman defterlerinde sunulan tüm işlevsellikleri de içerir.

Defter işlevi, tüm organizasyonunuzun sabit kıymet süreçleri için tek bir sayfa, sorgu ve rapor kümesi kullanmanızı sağlar. Bu konudaki tablolar amortisman defterlerinin ve değer modellerinin daha önceki işlevselliklerini, defterler için geçerli işlevsellikle birlikte açıklar.

## <a name="setup"></a>Kurulum
Varsayılan olarak, defterler genel muhasebe (GL) ve sabit kıymet yardımcı defterine nakleder. Defterler Genel muhasebeye nakletmeyi devre dışı bırakıp yalnızca Sabit kıymet yardımcı defterine nakletmenize izin veren yeni bir **Genel muhasebeye naklet** seçeneğine sahiptir. Bu işlevsellik amortisman defterlerinin önceki nakil davranışını andırır. Günlük adları kurulumu Yok adlı yeni bir deftere nakil katmanına sahiptir. Bu deftere nakil katmanı sabit kıymet hareketleri için özellikle eklenmiştir. Genel muhasebeye nakil yapmayan defterlerin hareketlerini deftere nakletmek için deftere nakil katmanı **Yok** olarak ayarlanmış bir günlük adı kullanmanız gerekir.


| &nbsp;                                           | Amortisman defteri               | Değer modeli                     | Defter (Yeni)                                              |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
| Genel muhasebeye naklet                                   | Hiçbir zaman                           | Her zaman                          | Genel muhasebeye nakletme seçeneği                                |
| Deftere nakil katmanları                                   | Geçerli değil                  | 3: Cari, Operasyonlar ve Vergi | 11: Cari, Operasyonlar, Vergi, 7 özel katman ve Yok |
| Günlük adları                                    | Amortisman defteri günlük adları | Genel muhasebe - Günlük adları              | Genel muhasebe - Günlük adları                                      |
| Türetilen defterler                                    | İzin verilmiyor                     | İzin veriliyor                         | İzin veriliyor                                                 |
| Amortisman profilini kıymet düzeyinde geçersiz kılma | İzin veriliyor                         | İzin verilmiyor                     | İzin veriliyor                                                 |

## <a name="processes"></a>İşlemler
Artık işlemler ortak bir sayfa kullanmaktadır. Bazı işlemlere yalnızca defter ayarındaki **Genel muhasebeye naklet** seçeneği **Hayır** olarak ayarlandıysa izin verilir.

| &nbsp;                                           | Amortisman defteri               | Değer modeli                     | Defter (Yeni)                                              |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
| Hareket girişi              | Amortisman defteri günlüğü | Sabit kıymet günlüğü | Sabit kıymet günlüğü                      |
| Bonus amortisman             | İzin veriliyor                   | İzin Verilmiyor         | İzin veriliyor                                  |
| Geçmiş hareketleri sil | İzin veriliyor                   | İzin Verilmiyor         | Genel muhasebeye nakletmediğiniz sürece izin veriliyor |
| Toplu güncelleştirme                    | İzin veriliyor                   | İzin Verilmiyor         | Genel muhasebeye nakletmediğiniz sürece izin veriliyor |

## <a name="inquiries-and-reports"></a>Sorgular ve raporlar
Sorgular ve raporlar tüm defterleri destekler. Aşağıdaki tabloda yer almayan raporlar önceden amortisman defterlerini ve değer modellerini destekliyordu ve şimdi de tüm defter türlerini desteklemeye devam edecektir. Hareket nakillerini daha kolay tanımlayabilmeniz için **Deftere nakil katmanı** alanı da raporlara eklenmiştir.

| &nbsp;                                           | Amortisman defteri               | Değer modeli                     | Defter (Yeni)                                              |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
| Sorgular                             | Amortisman defteri hareketleri | Sabit kıymet hareketleri | Sabit kıymet hareketleri |
| Sabit kıymet tablosu                 | İzin verilmiyor                    | İzin veriliyor                  | İzin veriliyor                  |
| Sabit kıymet esası                     | İzin veriliyor                        | İzin verilmiyor              | İzin veriliyor                  |
| Çeyrek dönemlik sabit kıymet alım raporu | İzin veriliyor                        | İzin verilmiyor              | İzin veriliyor                  |

## <a name="upgrade"></a>Yükselt
Yükseltme işlemi var olan kurulumunuzu ve var olan tüm hareketlerinizi yeni defter yapısına taşır. Değer modelleri oldukları gibi Genel muhasebeye nakleden defterler olarak kalır. Ancak amortisman defterleri **Genel muhasebeye naklet** seçeneği **Hayır** olarak ayarlanmış bir deftere taşınır. Amortisman defteri günlük adları deftere nakil katmanı **Yok** olarak ayarlanmış bir Genel muhasebe günlük adına taşınır.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
