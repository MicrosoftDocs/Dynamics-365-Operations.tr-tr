---
title: Banka mutabakatı eşleştirme kurallarını ayarlama
description: Bu makalede, banka mutabakatı sürecini kolaylaştırmak için banka mutabakatı eşleştirme kuralları ve mutabakat eşleştirme kural kümeleri oluşturma işlemi açıklanmaktadır. Mutabakat eşleştirme kuralları, mutabakat süreci sırasında banka ekstresi satırlarını ve banka belge satırlarını filtrelemek için kullanılan bir ölçüt kümesidir.
author: angelad116
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac5ab5e2bcb9a63bb52d5a74bd5e4b5db51ba603
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803950"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Banka mutabakatı eşleştirme kurallarını ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, banka mutabakatı sürecini kolaylaştırmak için banka mutabakatı eşleştirme kuralları ve mutabakat eşleştirme kural kümeleri oluşturma işlemi açıklanmaktadır. Mutabakat eşleştirme kuralları, mutabakat süreci sırasında banka ekstresi satırlarını ve banka belge satırlarını filtrelemek için kullanılan bir ölçüt kümesidir.

Banka mutabakatı sürecini kolaylaştırmak için banka mutabakatı eşleştirme kuralları ve mutabakat eşleştirme kural kümeleri oluşturabilirsiniz. Bir mutabakat eşleştirme kuralı, mutabakat süreci sırasında banka ekstresi satırlarını ve Dynamics 365 Finance banka hareketi satırlarını filtrelemek için kullanılan bir ölçüt kümesidir. Mutabakat eşleştirme kurallarını ayarlamak için **Mutabakat eşleştirme kuralları** sayfasını kullanın. Birden fazla eşleştirme kuralı oluşturabilir ve ardından **Mutabakat eşleştirme kural kümeleri** sayfasında bir mutabakat eşleştirme kural kümesi oluşturabilirsiniz. 

> [!NOTE] 
> Banka mutabakatı eşleştirme kuralları, bir elektronik banka ekstresi için gelişmiş banka mutabakatı kullanarak mutabakat sağladığınızda kullanılır. 

**Mutabakat eşleştirme kuralları** sayfasında, eşleştirme kuralı çalıştırıldığında hangi eylemlerin ve seçimi ölçütlerinin kullanılacağını seçebilirsiniz. **Eylemler** alan grubunda, mutabakat işlemi sırasında eşleştirme kuralı çalıştırıldığı zaman gerçekleştirilecek eylemi seçin.  

Varsayılan olarak, eşleştirme kuralları eşleştirme kural ölçütünü karşılayan ilk banka belgesiyle eşleşecektir. Birden çok banka belgesi kural ölçütlerini karşılıyorsa **Nakit ve banka yönetimi > Ayar > Nakit ve banka yönetimi parametreleri > Banka mutabakatı > Gelişmiş banka mutabakatı eşleştirme kuralları, tutarla eşleşen birden fazla belge bulduğunda el ile eşleştirmeyi gerekli kıl** seçeneğine giderek el ile eşleştirme parametresi açılabilir.

> [!NOTE] 
> Belirttiğiniz seçenek görüntülenen alanları belirler.

| Eylem | Tanım   | Eylem seçildiğinde kullanılabilecek seçim ölçütleri     |
|--------|---------------|----------------------------------------------------------|
| **Banka belgesiyle eşleştir**       | **Banka mutabakatı çalışma sayfası** sayfasından eşleştirme kuralı çalıştırıldığında banka belgelerinin ve banka ekstresi satırlarının nasıl eşleştirileceğini tanımlayan ölçütler oluşturun. Hareket satırları, Hızlı Sekmelerde ayarlanan ek ölçütlere göre seçilir. | <ul><li>**1. adım: Eşleştirme kuralını tanımlayın** – Finance banka hareketleriyle hangi banka ekstrelerinin eşleştirilmesi gerektiğini tanımlayan ölçütleri seçin.</li><li> **Adım 2 (isteğe bağlı): Eşleştirme kurallarının çalıştırılacağı ekstre satırlarını seçin:** Kuralların hangi ekstre satırında çalıştırılacağını belirlemek için bir filtre uygulayın.</li></ul>                                       |
| **Ters ekstre satırlarını temizle** | Eşleştirme kuralı çalıştırıldığında **Banka mutabakatı çalışma sayfası** sayfasından hangi ters ekstre satırlarının kaldırılacağını tanımlayan ölçütler oluşturun. Bu seçenek, bir banka hatasının, iki banka ekstresi satırının içe aktarılan banka ekstresinde listelenmesine neden olduğunda ve satırlar için mutlaka mutabakat sağlanması gerektiğinde kullanılır. |<ul><li> **1. adım**:**Ters ekstre satırlarını bulun**– Ters banka ekstresi satırlarını seçmek için seçim ölçütlerini ekleyin. Örneğin, yalnızca denetimleri seçmek için, **Alan** alanında **Banka hareket kodu** öğesini seçin, **İşleç** alanında artı işaretini (+) seçin ve **Değer** alanına **Denetimler** girin. </li><li>**2. Adım: Orijinal ekstre satırlarını bulun** – Banka belgesi satırlarını banka ekstresi satırlarıyla eşleştirmek için seçim ölçütleri ekleyebilirsiniz. </li><li>**3. Adım: Finance banka hareketlerini bulun**– Finance banka hareketlerini banka ekstresi satırlarıyla eşleştirmek için seçim ölçütleri ekleyebilirsiniz.</li></ul>  |
| **Yeni hareketleri işaretle**          | Eşleştirme kuralı çalıştırıldığında **Banka mutabakatı çalışma sayfası** sayfasında yeni hareketlerin nasıl işaretleneceğini tanımlayan ölçütler oluşturun.                                                                                                                                                                 | <ul><li>**1. adım: Ekstre satırlarını bulun**– **Banka mutabakatı çalışma sayfası** sayfasından hangi banka ekstresi satırlarının seçileceğini belirleyen seçim alanlarını ekleyin.</li><li> **2. Adım: Finans ve operasyon uygulamalarını bulun** – Banka belgeleri satırlarını aramak için seçim ölçütleri ekleyebilirsiniz. Hiçbir banka belgesi bulunursa, bir ekstre satırı yeni bir hareket olarak işaretlenecektir. </li></ul>         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

