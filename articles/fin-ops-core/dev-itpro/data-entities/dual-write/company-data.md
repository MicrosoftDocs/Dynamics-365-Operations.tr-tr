---
title: Dataverse'ta şirket kavramı
description: Bu makalede, finans ve operasyon uygulamaları ve Dataverse arasında şirket verisi tümleştirmesi açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2bdd99b581be453616e71d0f0f95a7daf75a253a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289789"
---
# <a name="company-concept-in-dataverse"></a>Dataverse'ta şirket kavramı

[!include [banner](../../includes/banner.md)]




Finans operasyon uygulamalarında *şirket kavramı* hem yasal bir yapı hem de bir işletme yapısıdır. Ayrıca veriler için bir güvenlik ve görünürlük sınırıdır. Kullanıcılar her zaman tek bir şirket bağlamında çalışır ve verilerin çoğu şirket tarafından çıkarılır.

Dataverse'da eşdeğer bir kavram yoktur. En yakın kavram, birincil olarak kullanıcı verileri için bir güvenlik ve görünürlük sınırı olan *iş birimidir*. Bu kavram, şirket kavramıyla aynı yasal veya iş etkilerine sahip değildir.

İş birimi ve şirket eşdeğer kavramlar olmadığından, Dataverse tümleştirmesi amacıyla aralarında bire bir (1:1) eşlemesini zorlamak mümkün değildir. Ancak, kullanıcılar varsayılan olarak, uygulamada ve Dataverse'te aynı satırları görebilmelidir; bu nedenle Microsoft, Dataverse'te cdm\_Company adlı yeni bir tabloyu kullanıma sundu. Bu tablo uygulamadaki Şirket tablosuna eşdeğerdir. Satır görünürlüğünün uygulama ve Dataverse'te başlangıçtan itibaren eşdeğer olmasını sağlamaya yardımcı olmak için Dataverse'te veriler için aşağıdaki kurulumu öneriyoruz:

+ Çift yazma için etkinleştirilmiş her finans ve operasyon uygulamaları Şirket satırı için ilişkili bir cdm\_Şirket satırı oluşturulur.

+ cdm\_Company satırı oluşturulduğunda ve çift yazma için etkinleştirildiğinde, aynı ada sahip bir varsayılan iş birimi oluşturulur. Bu iş birimi için otomatik olarak varsayılan bir sahip ekip oluşturulsa da, iş birimi kullanılmaz.
+ Çift Yazma son ekiyle aynı ada sahip ayrı bir sahip olan takım oluşturulur. Ayrıca iş birimi ile de ilişkilidir.

+ Varsayılan olarak, oluşturulan ve Dataverse'e çift yazılan herhangi bir satırın sahibi, ilişkili iş birimine bağlı "DW Sahibi" ekibine ayarlanır.

Aşağıdaki şekilde, Dataverse'daki bu veri ayarının bir örneğini gösterir.

![Dataverse'da veri ayarı.](media/dual-write-company-1.png)

Bu yapılandırma nedeniyle, USMF şirketiyle ilgili herhangi bir satır, Dataverse'teki USMF iş birimine bağlı olan bir takıma ait olacaktır. Bu nedenle, iş birimi düzeyinde görünürlük için ayarlanan bir güvenlik rolü aracılığıyla bu iş birimine erişimi olan herhangi bir kullanıcı artık bu satırları görebilir. Aşağıdaki örnekte, bu satırlara doğru erişimi sağlamak amacıyla takımların nasıl kullanılabileceği gösterilmektedir.

+ "Satış Yöneticisi" rolü "USMF Satış" takımı üyelerine atanır.
+ "Satış Yöneticisi" rolüne sahip kullanıcılar, üye oldukları aynı işi birimine üye olan hesap satırlarına erişebilir.
+ "USMF Satış" ekibi, daha önce bahsedilen USMF iş birimine bağlıdır.
+ Bu nedenle, "USMF Satış" ekibinin üyeleri finans ve operasyon uygulamalarındaki USMF Şirket tablosundan gelen "USMF DW" kullanıcısı tarafından sahip olunan herhangi bir hesabı görebilir.

![Takımlar nasıl kullanılabilir.](media/dual-write-company-2.png)

Önceki örnekte gösterildiği gibi iş birimi, şirket ve ekip arasındaki bu 1:1 eşleme yalnızca bir başlangıç noktasıdır. Bu örnekte, yeni bir "Avrupa" iş birimi hem DEMF hem de ESMF için üst öğe olarak Dataverse'ta el ile ayarlanır. Bu yeni kök iş birimi çift yazma ile ilgili değildir. Ancak, "EUR Satış" ekibinin üyelerine, ilgili güvenlik rolündeki **Üst/Alt İş Birimi** veri görünürlüğünü ayarlayarak hem DEMF hem de ESMF'deki hesap verilerine erişim vermek için kullanılabilir.

Tartışılması gereken son bir madde de çift yazmanın satırları hangi sahip takıma atayacağını belirleme yöntemidir. Bu davranış, cdm\_Company satırındaki **Varsayılan sahibi olan takım** sütunu tarafından denetlenir. Bir cdm\_Company satırı çift yazma için etkinleştirildiğinde, bir eklenti otomatik olarak ilişkili iş birimi ve sahibi olan takımı (zaten yoksa) oluşturur ve **Varsayılan sahibi olan takım** sütununu ayarlar. Yönetici bu sütunu farklı bir değere değiştirebilir. Ancak, tablo çift yazma için etkinleştirildiği sürece yönetici sütunu temizleyemez.

> [!div class="mx-imgBorder"]
![Varsayılan sahibi olan takım sütunu.](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Şirket bölümleme ve yeniden örnekleme

Dataverse tümleştirmesi verileri bölümlemek için şirket tanımlayıcısını kullanarak şirket eşliği getirir. Aşağıdaki çizimde gösterildiği gibi, tüm şirkete özgü tablolar, cdm\_Company tablosutka çok-bir (N:1) ilişkisine sahip olmaları için genişletilir.

> [!div class="mx-imgBorder"]
![Şirkete özgü tablo ile cdm_Company tablosu arasındaki N:1 ilişkisi.](media/dual-write-bootstrapping.png)

+ Satırlar için, bir şirket eklendikten ve kaydedildikten sonra, değer salt okunur olur. Bu nedenle, kullanıcılar doğru şirketi seçtiğinden emin olmalıdır.
+ Yalnızca şirket verilerine sahip satırlar uygulama ile Dataverse arasında çift yazma için uygundur.
+ Var olan Dataverse verileri için, yönetici tarafından yürütülen bir yeniden örnekleme deneyimi yakında kullanıma sunulacaktır.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Müşteri etkileşimi uygulamalarında şirket adını otomatik olarak doldurma

Müşteri etkileşimi uygulamalarında şirket adını otomatik olarak doldurmanın birkaç yolu vardır.

+ Sistem yöneticisiyseniz **Gelişmiş Ayarlar > Sistem > Güvenlik > Kullanıcılar** seçeneğine giderek varsayılan şirketi ayarlayabilirsiniz. **Kullanıcı** formunu açın ve **Kuruluş Bilgileri** bölümünde **Formlarda varsayılan olarak kullanılacak şirket** değerini ayarlayın.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Kuruluş bilgileri bölümünde varsayılan şirketi ayarlayın.":::

+ **İş Birimi** düzeyi için **SystemUser** tablosuna **Yazma** erişiminiz varsa **Şirket** açılır menüsünden bir şirket seçerek tüm formlardaki varsayılan şirketi değiştirebilirsiniz.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Yeni bir hesaptaki şirket adını değiştirme.":::

+ Birden fazla şirketteki verilere **Yazma** erişiminiz varsa farklı bir şirkete ait satırı seçerek varsayılan şirketi değiştirebilirsiniz.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Satır seçmek, varsayılan şirketi değiştirir.":::

+ Sistem yapılandırıcısı veya yöneticisiyseniz ve özel bir formda şirket verilerini otomatik olarak doldurmak istiyorsanız [form olaylarını](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids) kullanabilirsiniz. **msdyn_/DefaultCompany.js** öğesine JavaScript başvurusu ekleyip aşağıdaki olayları kullanın. İstediğiniz kullanıma hazır formu (ör. **Hesap** formu) kullanabilirsiniz.

    + Form için **OnLoad** olayı: **defaultCompany** sütununu ayarlayın.
    + **Şirket** sütunu için **OnChange** olayı: **updateDefaultCompany** sütununu ayarlayın.

## <a name="apply-filtering-based-on-the-company-context"></a>Şirket bağlamına göre filtre uygulama

Özel formlarınızda veya standart formlara eklenmiş özel arama sütunlarınızda şirket bağlamına göre filtre uygulamak için formu açın ve **İlgili Kayıtlara Filtre Uygulama** bölümünü kullanarak şirket filtresi uygulayın. Belirli bir satırdaki temel şirkete dayalı olarak filtre gerektiren her arama sütunu için bunu ayarlamalısınız. Aşağıdaki resimde bu ayar **Hesap** için gösterilmiştir.

:::image type="content" source="media/apply-company-context.png" alt-text="Şirket bağlamını uygulama.":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
