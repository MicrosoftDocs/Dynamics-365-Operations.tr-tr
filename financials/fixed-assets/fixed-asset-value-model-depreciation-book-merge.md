---
title: "Sabit kıymet değer modeli ve amortisman defteri birleştirme"
description: "Önceki sürümlerde, sabit kıymetler - değer modelleri ve amortisman defterleri olmak üzere iki değerleme kavramı vardı. Microsoft Dynamics 365 for Operations dağıtımı 1611 ile, değer modeli işlevselliği ve amortisman defteri işlevselliği bir defter olarak bilinen tek bir kavramda birleştirilmiştir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 602515e9ea5681fd0bbe74525365b6628fee62d3
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Sabit kıymet değer modeli ve amortisman defteri birleştirme

[!include[banner](../includes/banner.md)]


Önceki sürümlerde, sabit kıymetler - değer modelleri ve amortisman defterleri olmak üzere iki değerleme kavramı vardı. Microsoft Dynamics 365 for Operations dağıtımı 1611 ile, değer modeli işlevselliği ve amortisman defteri işlevselliği bir defter olarak bilinen tek bir kavramda birleştirilmiştir.

Yeni defter işlevselliği eski değer modeli işlevselliğini temel alır ancak önceden yalnızca amortisman defterlerinde sunulan tüm işlevsellikleri de içerir. [![Bir değer modeli ve amortisman defteri işlevinin birleştirmesi olarak kaydet](./media/fixed-assets.png)](./media/fixed-assets.png) Bu birleştirme sayesinde tüm sabit kıymet işlemleriniz için tek bir sayfa seti, sorgular ve raporlar kullanabilirsiniz. Bu konudaki tablolar amortisman defterlerinin ve değer modellerinin daha önceki işlevselliklerini, defterler için yeni işlevsellikle birlikte açıklar.

## <a name="setup"></a>Kurulum
Varsayılan olarak, defterler genel muhasebe (GL) ve sabit kıymet yardımcı defterine nakleder. Defterler genel muhasebeye nakletmeyi devre dışı bırakıp yalnızca sabit kıymet yardımcı defterine nakletmenize izin veren yeni bir **Genel muhasebeye naklet** seçeneğine sahiptir. Bu işlevsellik amortisman defterlerinin önceki nakil davranışını andırır. Günlük adları kurulumu Yok adlı yeni bir deftere nakil katmanına sahiptir. Bu deftere nakil katmanı sabit kıymet hareketleri için özellikle eklenmiştir. Genel muhasebeye nakil yapmayan defterlerin hareketlerini deftere nakletmek için deftere nakil katmanı **Yok** olarak ayarlanmış bir günlük adı kullanmanız gerekir.

|                                                  |                                 |                                 |                                                         |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
|                                                  | Amortisman defteri               | Değer modeli                     | Defter (Yeni)                                              |
| Genel muhasebeye nakletme                                   | Hiçbir Zaman                           | Her zaman                          | Genel muhasebeye nakletme seçeneği                                |
| Deftere nakil katmanları                                   | Uygulanamaz                  | 3: Cari, Operasyonlar ve Vergi | 11: Cari, Operasyonlar, Vergi, 7 özel katman ve Yok |
| Günlük adları                                    | Amortisman defteri günlük adları | Genel Muhasebe - Günlük adları              | Genel Muhasebe - Günlük adları                                      |
| Türetilen defterler                                    | İzin verilmiyor                     | İzin veriliyor                         | İzin veriliyor                                                 |
| Amortisman profilini kıymet düzeyinde geçersiz kılma | İzin veriliyor                         | İzin verilmiyor                     | İzin veriliyor                                                 |

## <a name="processes"></a>İşlemler
Artık işlemler ortak bir sayfa kullanmaktadır. Bazı işlemlere yalnızca defter ayarındaki **Genel muhasebeye naklet** seçeneği **Hayır** olarak ayarlandıysa izin verilir.

|                                |                           |                     |                                          |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
|                                | Amortisman defteri         | Değer modeli         | Defter (Yeni)                               |
| Hareket girişi              | Amortisman defteri günlüğü | Sabit kıymet günlüğü | Sabit kıymet günlüğü                      |
| Bonus amortisman             | İzin veriliyor                   | İzin Verilmiyor         | İzin veriliyor                                  |
| Geçmiş hareketleri sil | İzin veriliyor                   | İzin Verilmiyor         | Genel muhasebeye nakletmediğiniz sürece izin veriliyor |
| Toplu güncelleştirme                    | İzin veriliyor                   | İzin Verilmiyor         | Genel muhasebeye nakletmediğiniz sürece izin veriliyor |

## <a name="inquiries-and-reports"></a>Sorgular ve raporlar
Sorgular ve raporlar tüm defterleri destekler. Aşağıdaki tabloda yer almayan raporlar önceden amortisman defterlerini ve değer modellerini destekliyordu ve şimdi de tüm defter türlerini desteklemeye devam edecektir. Hareket nakillerini daha kolay tanımlayabilmeniz için **Deftere nakil katmanı** alanı da raporlara eklenmiştir.

|                                       |                                |                          |                          |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
|                                       | Amortisman defteri              | Değer modeli              | Defter (Yeni)               |
| Sorgular                             | Amortisman defteri hareketleri | Sabit kıymet hareketleri | Sabit kıymet hareketleri |
| Sabit kıymet tablosu                 | İzin verilmiyor                    | İzin veriliyor                  | İzin veriliyor                  |
| Sabit kıymet esası                     | İzin veriliyor                        | İzin verilmiyor              | İzin veriliyor                  |
| Çeyrek dönemlik sabit kıymet alım raporu | İzin veriliyor                        | İzin verilmiyor              | İzin veriliyor                  |

## <a name="upgrade"></a>Yükselt
Yükseltme işlemi var olan kurulumunuzu ve var olan tüm hareketlerinizi yeni defter yapısına taşır. Değer modelleri oldukları gibi genel muhasebeye nakleden defterler olarak kalır. Ancak amortisman defterleri **Genel muhasebeye naklet** seçeneği **Hayır** olarak ayarlanmış bir deftere taşınır. Amortisman defteri günlük adları deftere nakil katmanı **Yok** olarak ayarlanmış bir genel muhasebe günlük adına taşınır.



