---
title: B2B özelleştirmelerine yönelik Commerce kataloglarının genişletilebilirlik etkisi
description: Bu makale, Microsoft Dynamics 365 Commerce'deki B2B özelliği için Commerce kataloglarının genişletilebilirlik etkisini açıklamaktadır.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 06d304226270c9c63c6907190dc1038a38f70e44
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136813"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>B2B özelleştirmelerine yönelik Commerce kataloglarının genişletilebilirlik etkisi

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'teki **B2B için Commerce katalogları** özelliğinin genişletilebilirlik etkisini açıklamaktadır.

Katalog bağlamını özel senaryolara göre genişletme ile ilgileniyorsanız, özelleştirmelerinizin güncelleştirilmesi gerekebilir. Bu güncelleştirme, müşterilerin izlemesi gereken standart işlemi izler, çünkü özelleştirmeleri, yükseltmeler yapıldıktan sonra en son özellikleri otomatik olarak desteklemeyebilir. Özelleştirmeleriniz deneyimlerdeki yeni özellik veya hata düzeltmelerini içeriyorsa, özelleştirme kodunu buna göre güncelleştirmenizi öneririz. Bu güncelleştirme, Microsoft'un çekirdek kod için yapmış olabileceği değişikliklere benzer.

Özelleştirmelerinizin güncelleştirilip güncelleştirilmeyeceğini belirlemek için takip eden özelleştirme örneklerini gözden geçirin.

> [!NOTE]
> - Tüm ticari satış uygulama programı arabirimleri (API) katalog bilinçli olmalıdır. Bu nedenle **CatalogID** parametresini geçirmeniz önemlidir.
> - Varsayılan katalog (**CatalogID**=**0**), oturum açan işletmeler arası (B2B) kullanıcılar için geçerli bir katalog değildir. Bu nedenle, site kullanıcılarının 0 kataloğuna erişimi olmadığından, "0" veya varsayılan değer kullanan tüm API çağrıları başarısız olur. Doğru deneyimi elde etmek için, katalog seçicide seçilen katalog kimliğini geçmesi için müşteri API çağrılarının güncelleştirilmesi gerekir. Varsayılan bir değer kullanırsanız ve kullanıcı katalogları değiştirirse, web sitesi seçilen kataloğa ait verileri sağlamalıdır. Bu nedenle, çekirdek Commerce kodundan çalıştırılan API'lerle eşleştirmek için özelleştirilmiş API'ler, seçilen kataloğu iletmelidir.

Aşağıdaki özelleştirme örnekleri için geliştirme güncelleştirmeleri gerekir:

- **1. Örnek:** Müşteri, ürünle ilgili API veya veri eylemi çağıran kendi [veri eylemi](e-commerce-extensibility/data-actions.md)'ni tanıtır. Aşağıdaki güncelleştirme adımları gereklidir:

    1. Veri eylemi bir doğrudan API çağrısı kullanıyorsa, veri eylemini, aşağıdaki örnek çizimde gösterildiği gibi, katalog kimliğini geçebilecek şekilde güncelleştirin.

        ![Katalog kimliğini geçen güncelleştirilmiş veri eylemi.](./media/customization1_a.png)

    1. Veri eylemi, özelleştirme içinde başka bir ürünle ilişkili bir veri eylemini çağırması halinde kodun **requestContext** gibi bazı yeni parametreleri geçebilmesi için güncelleştirilmesi gerekir. **requestContext** parametresi, aşağıdaki örnek çizimde gösterildiği gibi geçerli katalog kimliğini almak için kullanılır.

        ![Yeni parametreyi geçen güncelleştirilmiş veri eylemi.](./media/customization1_b.png)

- **2. Örnek:** Müşteri, [geçersiz kılınmış bir veri eylemine](e-commerce-extensibility/data-action-overrides.md) sahiptir. Aşağıdaki güncelleştirme adımı gereklidir:

    - 1. örnekte olduğu gibi veri eylemini güncelleştirin.

- **3. Örnek:** Müşteri, API veya veri eylemlerine çağrı içeren bir görünüm uzantısına, betik enjektör modülüne veya [kopyalanmış modüle](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module) sahiptir. Aşağıdaki güncelleştirme adımı gereklidir:

    - Kodu, aşağıdaki örnek çizimde gösterildiği üzere 1. örnekteki gibi güncelleştirin.

       ![Yeni parametreyi geçen güncelleştirilmiş kod.](./media/customization3.png)

- **4. Örnek:** Müşteri **getById** API çağrısı kullanır. Aşağıdaki güncelleştirme adımı gereklidir:

    - **getById** API çağrısında bazı sınırlamalar olması ve katalog tanımayı desteklememesi nedeniyle **getByIds** API çağrısına geçin.

- **5. Örnek:** Müşteri, farklı kataloglardan olabilecek birden çok ürün için bilgi alan bir veri eylemine sahip. Aşağıdaki güncelleştirme adımı gereklidir:

    - API çağrılarını katalog kimliğine göre bölün. Örneğin, sepet API'leri için alışveriş sepetinde farklı kataloglardan ürünler bulunabilir. Ürün satırları katalog kimliğine göre gruplandırılmalı ve aşağıdaki örnek çizimde gösterildiği gibi her katalog için API'yi ayrı olarak çağırmalıdır.

        ![Ürün satırlarını katalog kimliğine göre gruplandıran güncelleştirilmiş veri eylemi.](./media/customization5.png)

## <a name="additional-resources"></a>Ek kaynaklar

[B2B siteleri için ticari Katalog oluştur](catalogs-b2b-sites.md)

[B2B için Commerce katalog hakkında SSS](catalogs-b2b-sites-FAQ.md)

[Katalog seçicisi modülü](catalog-picker.md)
