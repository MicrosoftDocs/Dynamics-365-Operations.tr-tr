---
title: Varlık ölçüleri
description: Bu konuda Kıymet Yönetimi'nde varlık ölçüsü oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: adadb1df7b41488fad496f937ecbc24e0761e42d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439406"
---
# <a name="counters"></a>Sayaçlar

[!include [banner](../../includes/banner.md)]

Bu konuda Varlık Yönetimi'nde sayaç türleri oluşturma işlemi açıklanmaktadır. Sayaç türleri, varlıklar üzerinde üretim saatleri sayısı veya varlık üzerinde üretilen miktar gibi sayaç kayıtları yapmak için kullanılır. Sayaç türleri varlık ölçü birimi türleriyle ilişkilidir. Bu, sayacın bir varlık üzerinde yalnızca varlık üzerinde kullanılan varlık türünde sayaç ayarlanmış olması durumunda kullanılabileceği anlamına gelir.

Varlıklar üzerinde sayaç kayıtları yapmadan önce, **Sayaçlar**'da kullanmak istediğiniz sayaç türlerini oluşturun. Ardından, **Sayaçlar**'dan varlıklar üzerinde sayaç kayıtları oluşturabilirsiniz. 

Sayaçlar bakım planlarında kullanılabilir. Bir bakım planı satırı, örneğin üretim saatlerinin veya üretilen miktarın sayısıyla ilgili olarak "Sayaç" türünde olabilir. 

Bir sayaç kaydı el ile veya üretim saatlerine veya üretilen miktara göre otomatik olarak güncellenebilir. Sayaç, üç güncelleştirme yönteminden birini kullanacak şekilde ayarlanabilir (**Sayaçlar**'ın **Güncelleştir** alanında seçilir):
  
- El ile: Sayaç değerlerini el ile kaydetmeniz gerekir.  
- Üretim saatleri: Sayaç, üretim saatlerinin sayısına göre otomatik olarak güncelleştirilir.  
- Üretim miktarı: Sayaç, üretilen miktarın sayısına göre otomatik olarak güncelleştirilir.  

>[!NOTE]
>Üretilen miktar kullanılırsa, sağlam miktar ve hatalı miktar dahil *tüm* kayıtlı maddeler sayaç kaydına eklenir. Gerekirse, el ile varlık sayaç kayıtları yapmak her zaman mümkündür.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Varlık sayacı kayıtları için sayaç türleri oluşturma

1. **Varlık yönetimi** > **Kurulum** > **Varlık türleri** > **Sayaçlar**'ı seçin.
2. Yeni bir sayaç türü oluşturmak için **Yeni**'yi seçin.
3. **Sayaç** alanına bir kimlik ve **Ad** alanına bir sayaç adı ekleyin.
4. **Genel** hızlı sekmesinde, **Birim** alanından bir sayaç birimi seçin.
5. **Güncelleştirme** alanında, sayaç için kullanılacak güncelleştirme yöntemini seçin.
6. Bir varlık yapısındaki alt varlıkların otomatik olarak üst varlıkta yapılan sayaç kayıtlarını devralması gerekiyorsa **Sayaç verilerini devral** düğmesini "Evet"e getirin.
7. **Toplama toplamı** alanında, bu sayaç türünü kullanan bir sayaç için kullanılacak toplama yöntemini seçin. "Toplam", toplam değere kayıtlı değerleri sürekli olarak eklemek için kullanılan standart seçimdir. Bir sayaç, örneğin varlıktaki sıcaklık, titreşim veya aşınmayla ilgili olarak bir eşik izlemek için ayarlanmışsa, "Ortalama" kullanılabilir. 
8. **Yukarı yönlü sapma** alanına, el ile yapılan sayaç kayıtlarının beklenen aralıkta olduğunu doğrulamak için üst düzey yüzde değeri ekleyin. Doğrulama, varolan sayaç kayıtlarındaki doğrusal artışı temel alır.
9. **Aşağı yönlü sapma** alanına, el ile yapılan sayaç kayıtlarının beklenen aralıkta olduğunu doğrulamak için alt düzey yüzde değeri ekleyin. Doğrulama, varolan sayaç kayıtlarındaki doğrusal azalışı temel alır.
10. **Tür** alanında, el ile sayaç kayıtları yaptığınızda tanımlanan aralığın dışındaki sapmalar oluşursa gösterilecek ileti türünü (bilgi, uyarı, hata) seçin.
11. **Varlık türleri** hızlı sekmesinden sayacı kullanabilmesi gereken varlık türlerini ekleyin.
12. **İlgili varlık sayaçları** hızlı sekmesinde, bu sayaç güncelleştirildiğinde otomatik olarak güncelleştirilmesini istediğiniz sayacı ekleyin.


>[!NOTE]
>İlgili sayaç, yalnızca ilgili varlık ölçüsü, sayaç kurulumunda ilişkili olduğu varlık türüne sahipse, ilgili sayaç otomatik olarak güncelleştirilir. Örneğin: "Üretim saatleri" için bir sayaç ayarlayın ve "Kamyon Motoru" varlık türünü ekleyin. Bu sayaç güncelleştirildiğinde, ilgili bir sayaç olan "Petrol" aynı sayaç değerleri ile güncelleştirilir. **Sayaçlar**'daki kurulum "Saat" kurulumunu içerir. Ayrıca, "Petrol" sayacında, "Kamyon Motoru" varlık türü sayaç ilişkisini sağlamak amacıyla **Varlık türleri** hızlı sekmesine eklenmelidir. Saat ve Petrol sayaçları kurulumu örneği için aşağıdaki ekran görüntülerine bakın.

Varlık türleri **Sayaçlar**'daki bir sayaç türüne eklendiğinde bu sayaç otomatik olarak  [Varlık türleri](../setup-for-objects/object-types.md)'ndeki **Sayaçlar** hızlı sekmesinde bulunan varlık türlerine eklenir.

![Şekil 1](media/071-setup-for-objects.png)

