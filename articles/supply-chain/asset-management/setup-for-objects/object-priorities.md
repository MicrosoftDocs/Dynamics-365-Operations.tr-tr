---
title: Varlık hizmet düzeyleri
description: Bu konuda Varlık Yönetimi'ndeki varlık hizmet düzeyleri açıklanmaktadır.
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
ms.openlocfilehash: f079e6899a2e3949eff5945f867472c801d9e95c
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783664"
---
# <a name="asset-service-levels"></a>Varlık hizmet düzeyleri

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Bu konuda Varlık Yönetimi'ndeki varlık hizmet düzeyleri açıklanmaktadır. Varlık hizmet düzeyleri varlıklarla ilişkilidir ve bakım isteklerine ve iş emirlerine aktarılır. İş emri planlaması sırasında iş emirlerinin önceliğini hesaplamak için kullanılır. Değişiklik gerekiyorsa, varlık hizmet düzeyleri değiştirilebilir.

İş emri planlaması için derecelendirme puanlarının hesaplanmasıyla ilgili kurulum hakkında daha fazla bilgi için bkz. [Varlık Yönetimi parametreleri](../setup-for-objects/enterprise-asset-management-parameters.md). Varlık hizmet düzeyi için en az bir varsayılan kayıt ayarlamanız gerekir. Bu varsayılan kayıt, iş emri planlaması sırasında başka bir eşleşme bulunamazsa kullanılır.

**Örnek 1:** Başka bir eşleşme bulunmazsa kullanılan varsayılan hizmet düzeyi. Bu kayıtta, yalnızca bir hizmet düzeyi seçin.

**Örnek 2:** Volvo kamyon için işleri planlamak üzere kullanılan yüksek hizmet düzeyi. Bu kayıtta, ilgili bir varlık türü (**Kamyon**gibi), bir üretici (**Volvo**) ve bir hizmet düzeyi seçin.

## <a name="set-up-asset-service-levels"></a>Varlık hizmet düzeyleri ayarlama

1. **Varlık yönetimi** \> **Kurulum** \> **Varlık hizmet düzeyleri**'ni seçin.
2. Bir kayıt oluşturmak için **Yeni**'yi seçin.
3. Varlık hizmet düzeyi için gerekli olan ayrıntı düzeyine bağlı olarak **İşlem yapılacak yerleşim**, **Varlık türü**, **Üretici**, **Model**, **Varlık**, **İş emri türü** ve **Hizmet düzeyi** alanlarında ilgili seçimleri yapın.

    > [!NOTE]
    > Varlık hizmet düzeyi bakım talepleri ve iş emirleri için kullanıldığında, Varlık yönetimi olası bir eşleşmeyi denetlemek için tüm varlık hizmet düzeyi kayıtlarına bakar. Her zaman ilk önce en belirgin birleşimi denetler. Başka bir deyişle, Varlık Yönetimi **İş emri türü** alanı için bir eşleşme arar. Eşleşme bulamazsa **Varlık** alanı için eşleşmeleri denetler ve bu şekilde devam eder. **Varlık hizmet düzeyleri** sayfasının düzeninde gördüğünüz gibi bu davranış en belirgin birleşimi bulmak için Varlık Yönetimi'nin eşleşme için sağdan sola her kaydı denetleyeceği anlamına gelir. Eşleşme bulunmazsa, bu alanlarda hiçbir seçimi olmayan varsayılan kayıt kullanılır.

4. **Hizmet düzeyi** alanında, hizmet düzeyini (önceliği) belirten bir sayı seçin.


> [!NOTE]
> **Varlık hizmeti düzeyleri** sayfasındaki bir varlık hizmet düzeyi kaydını bir iş emri üzerinde zaten kullandıktan sonra değiştirirseniz, bakım taleplerindeki ve iş emirlerindeki hizmet düzeyi buna göre güncelleştirilmez.
