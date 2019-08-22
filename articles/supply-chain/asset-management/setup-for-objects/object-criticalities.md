---
title: Varlık kritiklik türleri
description: Bu konuda Varlık Yönetiminde varlık kritiklik türleri açıklanmaktadır.
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
ms.openlocfilehash: 660038060826ade9301e50143e49b53ba3fcd3ab
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783661"
---
# <a name="asset-criticalities"></a>Varlık kritiklikleri

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Bu konuda Varlık Yönetiminde varlık kritiklik türleri açıklanmaktadır. Varlık kritikliği varlıklarla ilişkilidir ve iş emirlerine aktarılır. İş emri üzerinde değiştirilemez. Varlık kritikliği iş emri planlaması sırasında iş emri kritikliğini hesaplamak için kullanılır. Başka bir deyişle, bir varlıktaki bakım işinin şirketinizin üretim zamanlamasını ve üretkenliğini nasıl etkilediğini hesaplamak için kullanılır. İş emri planlaması için derecelendirme puanlarının hesaplanmasıyla ilgili kurulum hakkında daha fazla bilgi için bkz. [Varlık Yönetimi parametreleri](../setup-for-objects/enterprise-asset-management-parameters.md).

Kritikliği ayarlamak için önce varlık kurulumunda kullanılması gereken kritiklik türlerini oluşturun. Daha sonra varlık kritikliklerini ayarlayın.

## <a name="set-up-criticality-types"></a>Kritiklik türlerini ayarlama

1. **Varlık yönetimi** \> **Kurulum** \> **Varlıklar** \> **Kritiklik türleri**'ni seçin.
2. Bir kayıt oluşturmak için **Yeni**'yi seçin.
3. **Kritiklik** alanında, kritikliği gösteren bir sayı girin.
4. **Ad** alanına kritiklik türü için bir ad girin.
5. **Faktör** alanına bir faktör girin. Bu faktör, kullanılması gereken kritiklik kaydını belirlemek için iş emri planlaması hesaplaması sırasında kullanılır. (En yüksek faktörüne sahip kayıt her zaman kullanılır.) Bu ayar, aşağıdaki örnekte gösterildiği gibi, aynı kritiklik değerine sahip olan kritiklik satırları oluşturulmuşsa geçerlidir.

    ![Şekil 1](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Varlıkla kritiklikleri ayarlama

1. **Varlık yönetimi** \> **Kurulum** \> **Varlık kritiklikleri**'ni seçin.
2. Bir kayıt oluşturmak için **Yeni**'yi seçin.
3. Varlık kritikliği için gerekli olan ayrıntı düzeyine bağlı olarak **İşlem yapılacak yerleşim**, **Varlık türü**, **Üretici**, **Model**, **Varlık**, **İş türü kategorisi**, **İş türü**, **İş türü değişkeni** ve **İş gereksinimi** alanlarında ilgili seçimleri yapın.

    > [!NOTE]
    > Bir varlık kritikliği seçildiğinde, Varlık Yönetimi olası bir eşleşme olup olmadığını kontrol etmek için tüm varlık kritiklik kayıtlarına bakar. Her zaman ilk önce en belirgin birleşimi denetler. Diğer bir deyişle, Varlık Yönetimi önce **İş gereksinimi**'ni kontrol eder. Eşleşme bulunmazsa, **İş türü değişkeni**'ni kontrol eder. Eşleşme bulunmazsa, **İş türü**'nü kontrol eder ve bu şekilde devam eder. Sayfa düzeninde gördüğünüz gibi bu davranış en özel birleşimi bulmak için Varlık Yönetimi'nin eşleşme için sağdan sola her kaydı denetlediği anlamına gelir. Eşleşme bulunmazsa, hiçbir seçimi olmayan "varsayılan" kayıt kullanılır.

4. **Kritiklik** alanında, önceki yordamda oluşturduğunuz kritiklik değerlerinden birini seçin.

### <a name="notes-about-criticality-setup"></a>Kritiklik kurulumu hakkında notlar

- Bir iş emri üzerinde kullandıktan sonra bu kurulumdaki bir varlık kritikliğini değiştirirseniz, iş emrindeki kritiklik buna göre güncelleştirilmez.
- İş emrindeki kritiklik, iş emrine bir iş emri satırı eklendiğinde veya silindiğinde yeniden hesaplanır.
- İş emri birkaç iş emri işi içeriyorsa, daima **Kritiklik türleri** sayfasındaki **Faktör** alanına göre en yüksek kritiklik, iş emri üzerinde kullanılır.
- Genellikle, varlık kritikliği zaman içinde değişebilir. Kritiklik yeni ekipman satın alma, yenilemeler gibi durumlardan etkilenebilir. Kritiklik tanımlarınızın geçerli üretim kurulumunuz ile eşleştiğinden emin olmak için varlık kritikliklerini düzenli aralıklarla (örneğin, yılda bir veya her iki yılda bir) yeniden değerlendirmeyi düşünün.
