---
title: Kıymet servis düzeyleri
description: Bu makalede Varlık Yönetimi'ndeki varlık hizmet düzeyleri açıklanmaktadır.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7429b30253f540925e67ff9239667a0a404f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908699"
---
# <a name="asset-service-levels"></a>Kıymet servis düzeyleri

[!include [banner](../../includes/banner.md)]

 

Bu makalede Varlık Yönetimi'ndeki varlık hizmet düzeyleri açıklanmaktadır. Varlık hizmet düzeyleri varlıklarla ilişkilidir ve bakım isteklerine ve iş emirlerine aktarılır. İş emri planlaması sırasında iş emirlerinin önceliğini hesaplamak için kullanılır. Değişiklik gerekiyorsa, varlık hizmet düzeyleri değiştirilebilir.

İş emri planlaması için derecelendirme puanlarının hesaplanmasıyla ilgili kurulum hakkında daha fazla bilgi için bkz. [Varlık Yönetimi parametreleri](../setup-for-objects/enterprise-asset-management-parameters.md). Varlık hizmet düzeyi için en az bir varsayılan kayıt ayarlamanız gerekir. Bu varsayılan kayıt, iş emri planlaması sırasında başka bir eşleşme bulunamazsa kullanılır.

**Örnek 1:** Başka bir eşleşme bulunmazsa kullanılan varsayılan hizmet düzeyi. Bu kayıtta, yalnızca bir hizmet düzeyi seçin.

**Örnek 2:** Volvo kamyon için işleri planlamak üzere kullanılan yüksek hizmet düzeyi. Bu kayıtta, ilgili bir varlık türü (**Kamyon** gibi), bir üretici (**Volvo**) ve bir hizmet düzeyi seçin.

## <a name="set-up-asset-service-levels"></a>Varlık hizmet düzeyleri ayarlama

1. **Varlık yönetimi** \> **Kurulum** \> **Varlık hizmet düzeyleri**'ni seçin.
2. Bir kayıt oluşturmak için **Yeni**'yi seçin.
3. Varlık hizmet düzeyi için gerekli olan ayrıntı düzeyine bağlı olarak **İşlem yapılacak yerleşim**, **Varlık türü**, **Üretici**, **Model**, **Varlık**, **İş emri türü** ve **Hizmet düzeyi** alanlarında ilgili seçimleri yapın.

    > [!NOTE]
    > Varlık hizmet düzeyi bakım talepleri ve iş emirleri için kullanıldığında, Varlık yönetimi olası bir eşleşmeyi denetlemek için tüm varlık hizmet düzeyi kayıtlarına bakar. Her zaman ilk önce en belirgin birleşimi denetler. Başka bir deyişle, Varlık Yönetimi **İş emri türü** alanı için bir eşleşme arar. Eşleşme bulamazsa **Varlık** alanı için eşleşmeleri denetler ve bu şekilde devam eder. **Varlık hizmet düzeyleri** sayfasının düzeninde gördüğünüz gibi bu davranış en belirgin birleşimi bulmak için Varlık Yönetimi'nin eşleşme için sağdan sola her kaydı denetleyeceği anlamına gelir. Eşleşme bulunmazsa, bu alanlarda hiçbir seçimi olmayan varsayılan kayıt kullanılır.

4. **Hizmet düzeyi** alanında, hizmet düzeyini (önceliği) belirten bir sayı seçin.


> [!NOTE]
> **Varlık hizmeti düzeyleri** sayfasındaki bir varlık hizmet düzeyi kaydını bir iş emri üzerinde zaten kullandıktan sonra değiştirirseniz, bakım taleplerindeki ve iş emirlerindeki hizmet düzeyi buna göre güncelleştirilmez.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]