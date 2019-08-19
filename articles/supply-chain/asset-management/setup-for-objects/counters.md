---
title: Varlık ölçüleri
description: Bu konuda Kıymet Yönetimi'nde varlık ölçüsü oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783665"
---
# <a name="asset-measures"></a>Varlık ölçüleri

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Bu konuda Kıymet Yönetimi'nde varlık ölçüsü oluşturma işlemi açıklanmaktadır. Varlık ölçü birimi türleri, varlıklar üzerinde üretim saatleri sayısı veya varlık üzerinde üretilen miktar gibi ölçüm kayıtları yapmak için kullanılır. Varlık türleri varlık ölçü birimi türleriyle ilişkilidir. Bu, varlık ölçümünün bir varlık üzerinde yalnızca varlık üzerinde kullanılan kıymet türünde varlık ölçüsü ayarlanmış olması durumunda kullanılabileceği anlamına gelir.

Varlıklar üzerinde ölçüm kayıtları yapmadan önce, **Sayaçlar**'da kullanmak istediğiniz varlık ölçüsü türlerini oluşturun. Ardından, **Varlık ölçüleri**'nden varlıklar üzerinde ölçüm kayıtları oluşturabilirsiniz. 

Varlık ölçüleri bakım planlarında kullanılabilir. Bir bakım planı satırı, örneğin üretim saatlerinin veya üretilen miktarın sayısıyla ilgili olarak "Sayaç" türünde olabilir. 

Bir varlık ölçüm kaydı el ile veya üretim saatlerine veya üretilen miktara göre otomatik olarak güncellenebilir. Varlık ölçüsü, üç güncelleştirme yönteminden birini kullanacak şekilde ayarlanabilir (**Sayaçlar**'ın **Güncelleştir** alanında seçilir):
  
- El ile: Varlık ölçüm değerlerini el ile kaydetmeniz gerekir.  
- Üretim saatleri: Sayaç, üretim saatlerinin sayısına göre otomatik olarak güncelleştirilir.  
- Üretim miktarı: Sayaç, üretilen miktarın sayısına göre otomatik olarak güncelleştirilir.  

>[!NOTE]
>Üretilen miktar kullanılırsa, sağlam miktar ve hatalı miktar dahil *tüm* kayıtlı maddeler ölçüm kaydına eklenir. Gerekirse, el ile varlık ölçüm kayıtları yapmak her zaman mümkündür.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Varlık sayacı kayıtları için sayaç türleri oluşturma

1. **Varlık yönetimi** > **Kurulum** > **Varlık türleri** > **Sayaçlar**'ı seçin.
2. Yeni bir varlık ölçüsü türü oluşturmak için **Yeni**'yi seçin.
3. **Sayaç** alanına bir kimlik ve **Ad** alanına bir sayaç adı ekleyin.
4. **Genel** hızlı sekmesinde, **Birim** alanından bir ölçüm birimi seçin.
5. **Güncelleştirme** alanında, varlık ölçüsü için kullanılacak güncelleştirme yöntemini seçin.
6. Bir varlık yapısındaki alt varlıkların otomatik olarak üst varlıkta yapılan varlık ölçüsü kayıtlarını devralması gerekiyorsa **Sayaç verilerini devral** düğmesini "Evet"e getirin.
7. **Toplama toplamı** alanında, bu varlık ölçü birimi türünü kullanan bir varlık ölçüsü için kullanılacak toplama yöntemini seçin. "Toplam", toplam değere kayıtlı değerleri sürekli olarak eklemek için kullanılan standart seçimdir. Bir varlık ölçüsü, örneğin varlıktaki sıcaklık, titreşim veya aşınmayla ilgili olarak bir eşik izlemek için ayarlanmışsa, "Ortalama" kullanılabilir. 
8. **Yukarı yönlü sapma** alanına, el ile yapılan varlık ölçü kayıtlarının beklenen aralıkta olduğunu doğrulamak için üst düzey yüzde değeri ekleyin. Doğrulama, varolan varlık ölçü birimi kayıtlarındaki doğrusal artışı temel alır.
9. **Aşağı yönlü sapma** alanına, el ile yapılan varlık ölçü kayıtlarının beklenen aralıkta olduğunu doğrulamak için daha alt düzey yüzde değeri ekleyin. Doğrulama, varolan varlık ölçü birimi kayıtlarındaki doğrusal düşüşü temel alır.
10. **Tür** alanında, el ile varlık ölçü kayıtları yaptığınızda tanımlanan aralığın dışındaki sapmalar oluşursa gösterilecek ileti türünü (bilgi, uyarı, hata) seçin.
11. **Varlık türleri** hızlı sekmesinden varlık ölçüsünü kullanabilmesi gereken varlık türlerini ekleyin.
12. **İlgili varlık ölçüleri** hızlı sekmesinde, bu varlık ölçüsü güncelleştirildiğinde otomatik olarak güncelleştirilmesini istediğiniz varlık ölçülerini ekleyin.


>[!NOTE]
>İlgili varlık ölçüsü, yalnızca ilgili varlık ölçüsü, varlık ölçüsü kurulumunda ilişkili olduğu varlık türüne sahipse, ilgili varlık ölçüsü otomatik olarak güncelleştirilir. Örneğin: "Üretim saatleri" için bir varlık ölçüsü ayarlayın ve "Kamyon Motoru" varlık türünü ekleyin. Bu varlık ölçümü güncelleştirildiğinde, ilgili bir sayaç olan "Petrol" aynı varlık ölçüsü değerleri ile güncelleştirilir. **Sayaçlar**'daki kurulum "Saat" kurulumunu içerir. Ayrıca, "Petrol" varlık ölçüsünde, "Kamyon Motoru" varlık türü varlık ölçü ilişkisini sağlamak amacıyla **Varlık türleri** hızlı sekmesine eklenmelidir. Saat ve Petrol varlık ölçüleri kurulumu örneği için aşağıdaki ekran görüntülerine bakın.

Varlık türleri **Sayaçlar**'daki bir varlık ölçüsü türüne eklendiğinde bu varlık ölçüsü otomatik olarak  [Varlık türleri](../setup-for-objects/object-types.md)'ndeki **Sayaçlar** hızlı sekmesinde bulunan varlık türlerine eklenir.

![Şekil 1](media/071-setup-for-objects.png)


