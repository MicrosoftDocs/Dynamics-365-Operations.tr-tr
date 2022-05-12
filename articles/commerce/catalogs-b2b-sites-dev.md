---
title: B2B özelleştirmeleri için Commerce kataloglarının genişletilebilirlik etkisi
description: Bu konu, Microsoft Dynamics 365 Commerce'deki B2B için Commerce kataloglarının genişletilebilirlik etkisini açıklamaktadır.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: aff333bfe8003233dd5d8181aa8c5dd7eaeffcd0
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/29/2022
ms.locfileid: "8656875"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>B2B özelleştirmeleri için Commerce kataloglarının genişletilebilirlik etkisi

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'deki **B2B için Commerce kataloglarının** genişletilebilirlik etkisini açıklamaktadır.

Katalog bağlamını özel senaryolara göre genişletme ile ilgileniyorsanız, özelleştirmelerinizin güncelleştirilmesi gerekebilir. Bu güncelleştirme, müşterilerin izlemesi gereken standart işlemi izler, çünkü bunların özelleştirmeleri, yükseltmeler yapıldıktan sonra en son özellikleri otomatik olarak desteklemeyebilir. Özelleştirmeleriniz deneyimlerdeki yeni özellik veya hata düzeltmelerini içeriyorsa, özelleştirme kodunu buna göre güncelleştirmenizi öneririz. Bu güncelleştirme, Microsoft'un çekirdek kod için yapmış olabileceği değişikliklere benzer.

Özelleştirmelerinizin güncelleştirilip güncelleştirilmeyeceğini belirlemek için takip eden özelleştirme örneklerini gözden geçirin.

> [!NOTE]
> - Tüm ticari satış uygulama programı arabirimleri (API) katalog bilinçli olmalıdır. Bu nedenle **CatalogID** parametresini geçirmeniz önemlidir.
> - Varsayılan katalog (**CatalogID**=**0**), oturum açan işletmeler arası (B2B) kullanıcılar için geçerli bir katalog değil. Bu nedenle, site kullanıcılarının 0 kataloğuna erişimi olmadığından, "0" veya varsayılan değer kullanan tüm API çağrıları başarısız olur. Doğru deneyimi elde etmek için, katalog seçicide seçilen katalog kimliğini geçmesi için müşteri API çağrılarının güncelleştirilmesi gerekir. Varsayılan bir değer kullanırsanız ve kullanıcı katalogları değiştirirse, web sitesi seçilen kataloğa ait verileri sağlamalıdır. Bu nedenle, çekirdek Commerce kodundan çalıştırılan API'lerle eşleştirmek için, özelleştirilmiş API'ler seçilen kataloğu iletmelidir.

Aşağıdaki özelleştirme çalışmaları için geliştirme güncelleştirmeleri gerekir:

- **Durum 1:** Müşteri, ürünle ilgili bir API veya [veri eylemi](e-commerce-extensibility/data-actions.md) çağıran kendi veri eylemini tanıtır. Aşağıdaki güncelleştirme adımları gereklidir:

    1. Veri eylemi bir doğrudan API çağrısı kullanıyorsa, veri eylemini, aşağıdaki örnek çizimde gösterildiği gibi, katalog kimliğini geçebilecek şekilde güncelleştirin.

        ![Katalog kimliğini geçen güncelleştirilmiş veri eylemi.](./media/customization1_a.png)

    1. Veri eylemi, özelleştirme içinde başka bir ürünle ilişkili bir veri eylemini çağırırsa, kodun, **requestContext** gibi bazı yeni parametreleri geçebilmesi için güncelleştirilmesi gerekir. **requestContext** parametresi, aşağıdaki örnek çizimde gösterildiği gibi, geçerli Katalog kimliğini almak için kullanılır.

        ![Yeni parametreyi geçen güncelleştirilmiş veri eylemi.](./media/customization1_b.png)

- **Durum 2:** Müşteri, [geçersiz kılınmış bir veri eylemine](e-commerce-extensibility/data-action-overrides.md) sahiptir. Aşağıdaki güncelleştirme adımı gereklidir:

    - Durum 1 için veri eylemini güncelleştirin.

- **Durum 3:** Müşteri API veya veri eylemlerine çağrı içeren bir görünüm uzantısına, bir kod enjektör modülüne veya [kopyalanmış modüle](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module) sahiptir. Aşağıdaki güncelleştirme adımı gereklidir:

    - Kodu, aşağıdaki örnekte gösterildiği gibi, durum 1 olarak güncelleştirin.

       ![Yeni parametreyi geçen güncelleştirilmiş kod.](./media/customization3.png)

- **Durum 4:** Bir müşteri **getById** API çağrısı kullanır. Aşağıdaki güncelleştirme adımı gereklidir:

    - **getById** API çağrısında bazı sınırlamalar olduğu ve katalog tanımayı desteklemediği için bunun yerine **getByIds** API çağrısına geçin.

- **Durum 5:** Müşteri, farklı kataloglardan olabilecek birden çok ürün için bilgi alan bir veri eylemine sahip. Aşağıdaki güncelleştirme adımı gereklidir:

    - API çağrılarını Katalog kimliğine göre bölün. Örneğin, sepet API'leri için alışveriş sepetinin farklı kataloglardan ürünler bulunabilir. Ürün satırları katalog koduna göre gruplandırılmalı ve aşağıdaki örnek çizimde gösterildiği gibi her katalog için API'yi ayrı olarak çağırmalıdır.

        ![Ürün satırlarını katalog koduna göre gruplandıran güncelleştirilmiş veri eylemi.](./media/customization5.png)

## <a name="additional-resources"></a>Ek kaynaklar

[B2B siteleri için ticari Katalog oluştur](catalogs-b2b-sites.md)

[B2B için Commerce katalog hakkında SSS](catalogs-b2b-sites-FAQ.md)
