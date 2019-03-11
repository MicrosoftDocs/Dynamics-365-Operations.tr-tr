---
title: Kısmi konum döngü sayımı
description: Döngü sayımı planları, gerçek sayım işlemlerine yol gösterir. Bir konumdaki tüm eldeki stokun sayılması yerine yalnızca belirli ürünlerin ve ürün çeşitlerinin sayılmasını talep edebilirsiniz.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd7cb8b35023ed63af191545d01c60c2c7cc8ef5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "320662"
---
# <a name="partial-location-cycle-counting"></a>Kısmi konum döngü sayımı

[!include [banner](../includes/banner.md)]

Döngü sayımı planları, gerçek sayım işlemlerine yol gösterir. Bir konumdaki tüm eldeki stokun sayılması yerine yalnızca belirli ürünlerin ve ürün çeşitlerinin sayılmasını talep edebilirsiniz.

Döngü sayımı planlarını sayım işi oluşturmak için kullanarak, gerçek sayım işlemlerine yol gösterebilirsiniz. Bir konumdaki tüm eldeki stokun sayılması yerine yalnızca belirli ürünlerin ve ürün çeşitlerinin sayılmasını talep edebilirsiniz. Belirli ürünleri filtreleyerek, ambar yöneticisi inceleme yükünü azaltabilir, konsolidasyon hatalarının önüne geçebilir ve zaman tasarruf edebilir.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Kısmi konum döngü sayımının yapılandırılması
Sayım işlemleri için ambar iş işlemini kullanıyorsanız, her bir konum için bir iş başlığı oluşturulur. Döngü sayım planı tanımlarsanız, **Konumları seç** sorgusunu, oluşturulan döngü sayımı işini sınırlamak için kullanabilirsiniz. Döngü sayım planı için ürünler seçtiğinizde, nelerin sayıldığını belirlemek için hem ürün hem de ürün çeşidi sorgularını seçebilirsiniz. 

Bir **iş şablonunu**, döngü sayım planının nasıl oluşturulacağını tanımlamak için bir döngü sayım planı ile ilişkilendirebilirsiniz. Sayım işlemleri için iş şablonu, doğrudan döngü sayım planından referans alınır. 

İş şablonu ayrıntılarını tanımladığınızda, **İş satırı bölmeleri** seçeneğini, sayım iş satırlarının madde numarası mı yoksa ürün çeşidi numarasına mı göre gruplanacağını belirtmek için kullanabilirsiniz. Bu ayar, bir konumdaki yalnızca belirli ürünler için eldeki stoku saymak istiyorsanız gereklidir. Oluşturulan döngü sayımı iş satırları, burada tanımladığınız bilgi düzeyine sahip olacaktır ve yönlendirmeli sayım işlemi, bu düzeye bağlı olacak ele alınacaktır. 

Döngü sayım planlarını, iş şablonları ile **İş satır sonu** seçeneğini kullanarak ilişkilendirirseniz, **Kısmi döngü sayım** alanı, oluşturulan döngü sayımı işi seçilir ve çoklu döngü sayım iş satırları, iş şablonundaki tanıma dayalı olarak oluşturulur. 

Kısmi döngü sayım işi işleme alınmadan önce, döngü sayım kurulumunun parçası olarak mobil cihaz menü öğesi için en azından **Madde numarasını görüntüle** seçeneğini işaretlemelisiniz. Ambar operatörü, yalnızca sayım satırları (madde numaraları ve ürün boyutları) ile ilgili sayım bilgisini kaydetmek üzere yönlendirilecektir. Eldeki diğer tüm stoklar bu sayım işlemi için yok sayılacaktır. 

Kısmi döngü sayım işlemi için **Son döngü sayımı** tarihi/saati, konum için güncelleştirilmeyecektir.

## <a name="example"></a>Örnek
Bu örnekte, ambar 61'de yalnızca ürün numarası A0001 sayılacaktır.

1.  Döngü sayımı için yeni bir iş şablonu oluşturulur. **Döngü satır sonları** seçeneği, sayım iş satırlarını madde numarasına göre gruplamak için kullanılır. Bu nedenle, oluşturulan döngü sayım işi, madde numarasına göre satırlara sahip olacaktır. Satırları ayrıca ürün çeşit numarasına göre de gruplayabilirsiniz.
2.  Yeni oluşturulan iş şablonuna referans gösteren bir döngü sayım planı oluşturulur. Döngü sayım planı, ambar 61'deki (**Konum seç** sorgusu) madde numarası A0001 bulunduran tüm konumları kapsar. Belirli ürünlerin seçimi **Döngü sayımı ürün seçimi** bölümünde tanımlanır.
3.  **Boş yerleşimler** alanını **Boşu hariç tut** olarak ayarlayarak döngü sayımı planları için ürünler seçebilirsiniz. Döngü sayımı planı işlendiğinde, A0001 madde numarası için kısmi döngü sayımı işi oluşturulur. Gerçek sayım işlemi, yönlendirmeli döngü sayımı için bir taşınabilir aygıt menü öğesi kullanılarak gerçekleştirilebilir.



<a name="additional-resources"></a>Ek kaynaklar
--------

[Döngü sayımı](cycle-counting.md)

