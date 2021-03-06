---
title: Banka mutabakatı eşleştirme kurallarını ayarlama
description: Bu konu, banka mutabakatı sürecini kolaylaştırmak için banka mutabakatı eşleştirme kuralları ve mutabakat eşleştirme kural kümeleri oluşturmayı anlatır. Mutabakat eşleştirme kuralları, mutabakat süreci sırasında banka ekstresi satırlarını ve banka belge satırlarını filtrelemek için kullanılan bir ölçüt kümesidir.
author: panolte
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: roschlom
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c630449b8666593f69d9299ad1c0726369cc030a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834968"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Banka mutabakatı eşleştirme kurallarını ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, banka mutabakatı sürecini kolaylaştırmak için banka mutabakatı eşleştirme kuralları ve mutabakat eşleştirme kural kümeleri oluşturmayı anlatır. Mutabakat eşleştirme kuralları, mutabakat süreci sırasında banka ekstresi satırlarını ve banka belge satırlarını filtrelemek için kullanılan bir ölçüt kümesidir.

Banka mutabakatı sürecini kolaylaştırmak için banka mutabakatı eşleştirme kuralları ve mutabakat eşleştirme kural kümeleri oluşturabilirsiniz. Bir mutabakat eşleştirme kuralı, mutabakat süreci sırasında banka ekstresi satırlarını ve Dynamics 365 Finance banka hareketi satırlarını filtrelemek için kullanılan bir ölçüt kümesidir. Mutabakat eşleştirme kurallarını ayarlamak için **Mutabakat eşleştirme kuralları** sayfasını kullanın. Birden fazla eşleştirme kuralı oluşturabilir ve ardından **Mutabakat eşleştirme kural kümeleri** sayfasında bir mutabakat eşleştirme kural kümesi oluşturabilirsiniz. 

> [!NOTE] 
> Banka mutabakatı eşleştirme kuralları, bir elektronik banka ekstresi için gelişmiş banka mutabakatı kullanarak mutabakat sağladığınızda kullanılır. 

**Mutabakat eşleştirme kuralları** sayfasında, eşleştirme kuralı çalıştırıldığında hangi eylemlerin ve seçimi ölçütlerinin kullanılacağını seçebilirsiniz. **Eylemler** alan grubunda, mutabakat işlemi sırasında eşleştirme kuralı çalıştırıldığı zaman gerçekleştirilecek eylemi seçin.  

Varsayılan olarak, eşleştirme kuralları eşleştirme kural ölçütünü karşılayan ilk banka belgesiyle eşleşecektir. Birden çok banka belgesi kural ölçütlerini karşılıyorsa **Nakit ve banka yönetimi > Ayar > Nakit ve banka yönetimi parametreleri > Banka mutabakatı > Gelişmiş banka mutabakatı eşleştirme kuralları, tutarla eşleşen birden fazla belge bulduğunda el ile eşleştirmeyi gerekli kıl** seçeneğine giderek el ile eşleştirme parametresi açılabilir.

> [!NOTE] 
> Belirttiğiniz seçenek görüntülenen alanları belirler.

| Eylem | Tanım   | Eylem seçildiğinde kullanılabilecek seçim ölçütleri     |
|--------|---------------|----------------------------------------------------------|
| **Banka belgesiyle eşleştir**       | **Banka mutabakatı çalışma sayfası** sayfasından eşleştirme kuralı çalıştırıldığında banka belgelerinin ve banka ekstresi satırlarının nasıl eşleştirileceğini tanımlayan ölçütler oluşturun. Hareket satırları, Hızlı Sekmelerde ayarlanan ek ölçütlere göre seçilir.                                | **1. adım: Eşleştirme kuralını tanımlayın** – Finance banka hareketleriyle hangi banka ekstrelerinin eşleştirilmesi gerektiğini tanımlayan ölçütleri seçin. **Adım 2 (isteğe bağlı): Eşleştirme kurallarının çalıştırılacağı ekstre satırlarını seçin:** Kuralların hangi ekstre satırında çalıştırılacağını belirlemek için bir filtre uygulayın.                                                                                                                                                                                                                                                                                                               |
| **Ters ekstre satırlarını temizle** | Eşleştirme kuralı çalıştırıldığında **Banka mutabakatı çalışma sayfası** sayfasından hangi ters ekstre satırlarının kaldırılacağını tanımlayan ölçütler oluşturun. Bu seçenek, bir banka hatasının, iki banka ekstresi satırının içe aktarılan banka ekstresinde listelenmesine neden olduğunda ve satırlar için mutlaka mutabakat sağlanması gerektiğinde kullanılır. | **1. adım**:**Ters ekstre satırlarını bulun**– Ters banka ekstresi satırlarını seçmek için seçim ölçütlerini ekleyin. Örneğin, yalnızca denetimleri seçmek için, Alan alanında **Banka hareket kodu** öğesini seçin, **İşleç** alanında artı işaretini (+) seçin ve Değer alanına **Denetimleri** girin. **2. Adım: Orijinal ekstre satırlarını bulun** – Banka belgesi satırlarını banka ekstresi satırlarıyla eşleştirmek için seçim ölçütleri ekleyebilirsiniz. **3. Adım: Finance banka hareketlerini bulun**– Finance banka hareketlerini banka ekstresi satırlarıyla eşleştirmek için seçim ölçütleri ekleyebilirsiniz. |
| **Yeni hareketleri işaretle**          | Eşleştirme kuralı çalıştırıldığında **Banka mutabakatı çalışma sayfası** sayfasında yeni hareketlerin nasıl işaretleneceğini tanımlayan ölçütler oluşturun.                                                                                                                                                                 | **1. adım: Ekstre satırlarını bulun**– **Banka mutabakatı çalışma sayfası** sayfasından hangi banka ekstresi satırlarının seçileceğini belirleyen seçim alanlarını ekleyin. **2. Adım: Finance and Operations'ı bulma**: Banka belgesi satırlarını aramak için seçim ölçütleri ekleyebilirsiniz. Hiçbir banka belgesi bulunursa, bir ekstre satırı yeni bir hareket olarak işaretlenecektir.                                                                                                                                                                                                                                             |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]