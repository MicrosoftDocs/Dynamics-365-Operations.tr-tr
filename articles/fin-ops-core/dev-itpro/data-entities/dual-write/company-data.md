---
title: Common Data Service'da şirket kavramı
description: Bu konu, Finance and Operations ve Common Data Service arasındaki şirket verileri tümleştirmesini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 444bfc1698a206ca34e67f742df63431a3b02649
ms.sourcegitcommit: 7da8811f1a7db858efb76edb0bdf857a47d07600
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/27/2020
ms.locfileid: "3728425"
---
# <a name="company-concept-in-common-data-service"></a>Common Data Service'da şirket kavramı

[!include [banner](../../includes/banner.md)]


Finance and Operations'da *şirket* kavramı hem yasal bir yapı hem de bir işletme yapısıdır. Ayrıca veriler için bir güvenlik ve görünürlük sınırıdır. Kullanıcılar her zaman tek bir şirket bağlamında çalışır ve verilerin çoğu şirket tarafından çıkarılır.

Common Data Service'da eşdeğer bir kavram yoktur. En yakın kavram, birincil olarak kullanıcı verileri için bir güvenlik ve görünürlük sınırı olan *iş birimidir*. Bu kavram, şirket kavramıyla aynı yasal veya iş etkilerine sahip değildir.

İş birimi ve şirket eşdeğer kavramlar olmadığından, Common Data Service tümleştirmesi amacıyla aralarında bire bir (1:1) eşlemesini zorlamak mümkün değildir. Ancak, kullanıcılar varsayılan olarak, uygulamada ve Common Data Service'da aynı kayıtları görebilmelidir; bu nedenle Microsoft, Common Data Service'da cdm\_Şirket adlı yeni bir varlık tanıttı. Bu varlık uygulamadaki Şirket varlığına eşdeğerdir. Kayıtların görünürlüğünün uygulamak ve Common Data Service'ta eşdeğer olmasını sağlamaya yardımcı olmak için, Common Data Service'da aşağıdaki veri ayarının yapılmasını öneriyoruz.

+ Çift yazma için etkinleştirilmiş her Finance and Operations Şirket kaydı için, ilişkili bir cdm\_Şirket kaydı oluşturulur.
+ cdm\_Şirket kaydı oluşturulduğunda ve çift yazma için etkinleştirildiğinde, aynı ada sahip bir varsayılan iş birimi oluşturulur. Bu iş birimi için otomatik olarak varsayılan bir ekip oluşturulsa da, iş birimi kullanılmaz.
+ Aynı ada sahip ayrı bir sahip olan takım oluşturulur. Ayrıca iş birimi ile de ilişkilidir.
+ Varsayılan olarak, oluşturulan ve Common Data Service'a çift yazılan herhangi bir kaydın sahibi, ilişkili iş birimine bağlı "DW Sahibi" ekibine ayarlanır.

Aşağıdaki şekilde, Common Data Service'daki bu veri ayarının bir örneğini gösterir.

![Common Data Service'da veri ayarı](media/dual-write-company-1.png)

Bu yapılandırma nedeniyle, USMF şirketiyle ilgili herhangi bir kayıt, Common Data Service'daki USMF iş birimine bağlı olan bir takıma ait olacaktır. Bu nedenle, iş birimi düzeyinde görünürlük için ayarlanan bir güvenlik rolü aracılığıyla bu iş birimine erişimi olan herhangi bir kullanıcı artık bu kayıtları görebilir. Aşağıdaki örnek, takımlara bu kayıtlara doğru erişimi sağlamak amacıyla nasıl kullanılabileceğini gösterir.

+ "Satış Yöneticisi" rolü "USMF Satış" takımı üyelerine atanır.
+ "Satış Yöneticisi" rolüne sahip kullanıcılar, üye oldukları aynı işi birimine üye olan hesap kayıtlarına erişebilir.
+ "USMF Satış" ekibi, daha önce bahsedilen USMF iş birimine bağlıdır.
+ Bu nedenle, "USMF Satış" ekibinin üyeleri Finance and Operations'taki USMF Şirket varlığından gelen "USMF DW" kullanıcısı tarafından sahip olunan herhangi bir hesabı görebilir.

![Ekipler nasıl kullanılabilir](media/dual-write-company-2.png)

Önceki örnekte gösterildiği gibi iş birimi, şirket ve ekip arasındaki bu 1:1 eşleme yalnızca bir başlangıç noktasıdır. Bu örnekte, yeni bir "Avrupa" iş birimi hem DEMF hem de ESMF için üst öğe olarak Common Data Service'ta el ile ayarlanır. Bu yeni kök iş birimi çift yazma ile ilgili değildir. Ancak, "EUR Satış" ekibinin üyelerine, ilgili güvenlik rolündeki **Üst/Alt İş Birimi** veri görünürlüğünü ayarlayarak hem DEMF hem de ESMF'deki hesap verilerine erişim vermek için kullanılabilir.

Tartışılması gereken son bir konu da çift yazmanın kayıtların sahip olan hangi takıma atayacağının nasıl belirlendiğidir. Bu davranış, cdm\_Şirket kaydındaki **Varsayılan sahibi olan takım** alanı tarafından denetlenir. Bir cdm\_Şirket kaydı çift yazma için etkinleştirildiğinde, bir eklenti otomatik olarak ilişkili iş birimi ve sahibi olan takımı (zaten yoksa) oluşturur ve **Varsayılan sahibi olan takım** alanını ayarlar. Yönetici bu alanı farklı bir değere değiştirebilir. Ancak, varlık çift yazma için etkinleştirildiği sürece yönetici alanı temizleyemez.

> [!div class="mx-imgBorder"]
![Varsayılan sahibi olan takım alanı](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Şirket bölümleme ve yeniden örnekleme

Common Data Service tümleştirmesi verileri bölümlemek için şirket tanımlayıcısını kullanarak şirket eşliği getirir. Aşağıdaki örnekte gösterildiği gibi, tüm şirkete özgü varlıklar, cdm\_Şirket varlığıyla çok-bir (N:1) ilişkisine sahip olmaları için genişletilir.

> [!div class="mx-imgBorder"]
![Şirkete özgü varlık ile cdm_Şirket varlığı arasındaki N:1 ilişkisi](media/dual-write-bootstrapping.png)

+ Kayıtlar için, bir şirket eklendikten ve kaydedildikten sonra, değer salt okunur olur. Bu nedenle, kullanıcılar doğru şirketi seçtiğinden emin olmalıdır.
+ Yalnızca şirket verilerine sahip kayıtlar uygulama ile Common Data Service arasında çift yazma için uygundur.
+ Var olan Common Data Service verileri için, yönetici tarafından yürütülen bir yeniden örnekleme deneyimi yakında kullanıma sunulacaktır.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Müşteri etkileşimi uygulamalarında şirket adını otomatik olarak doldurma

Müşteri etkileşimi uygulamalarında şirket adını otomatik olarak doldurmanın birkaç yolu vardır.

+ Sistem yöneticisiyseniz **Gelişmiş Ayarlar > Sistem > Güvenlik > Kullanıcılar** seçeneğine giderek varsayılan şirketi ayarlayabilirsiniz. **Kullanıcı** formunu açın ve **Kuruluş Bilgileri** bölümünde **Formlarda varsayılan olarak kullanılacak şirket** değerini ayarlayın.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Kuruluş bilgileri bölümünde varsayılan şirketi ayarlayın.":::

+ **İş Birimi** düzeyi için **SystemUser** varlığına **Yazma** erişiminiz varsa **Şirket** açılır menüsünden bir şirket seçerek tüm formlardaki varsayılan şirketi değiştirebilirsiniz.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Yeni bir hesaptaki şirket adını değiştirme.":::

+ Birden fazla şirketteki verilere **Yazma** erişiminiz varsa farklı bir şirkete ait kaydı varsayılan şirketi değiştirebilirsiniz.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Kayıt seçmek, varsayılan şirketi değiştirir.":::

+ Sistem yapılandırıcısı veya yöneticisiyseniz ve özel bir formda şirket verilerini otomatik olarak doldurmak istiyorsanız [form olaylarını](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids) kullanabilirsiniz. **msdyn_/DefaultCompany.js** öğesine JavaScript başvurusu ekleyip aşağıdaki olayları kullanın. İstediğiniz kullanıma hazır formu (ör. **Hesap** formu) kullanabilirsiniz.

    + Form için **OnLoad** olayı: **defaultCompany** alanını ayarlayın.
    + **Şirket** alanı için **OnChange** olayı: **updateDefaultCompany** alanını ayarlayın.

## <a name="apply-filtering-based-on-the-company-context"></a>Şirket bağlamına göre filtre uygulama

Özel formlarınızda veya standart formlara eklenmiş özel arama alanlarınızda şirket bağlamına göre filtre uygulamak için formu açın ve **İlgili Kayıtlara Filtre Uygulama** bölümünü kullanarak şirket filtresi uygulayın. Belirli bir kayıttaki temel şirkete dayalı olarak filtre gerektiren her arama alanı için bunu ayarlamalısınız. Aşağıdaki resimde bu ayar **Hesap** için gösterilmiştir.

:::image type="content" source="media/apply-company-context.png" alt-text="Şirket bağlamını uygulama":::

