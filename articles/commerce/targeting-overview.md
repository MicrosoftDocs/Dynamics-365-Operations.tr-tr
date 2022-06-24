---
title: Cihaz, pazar ve coğrafi konum hedefleme
description: Bu makalede; cihaz, pazar ve coğrafi konum bilgilerini kullanarak Microsoft Dynamics 365 Commerce site oluşturucuda hedef kitlelerin ve hedeflerin nasıl oluşturulacağı, düzenleneceği ve yönetileceği açıklanmaktadır.
author: sushma-rao
ms.date: 02/03/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 90772fd942db30bbf4f65a87b1dca4b2aaacee1e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881669"
---
# <a name="device-market-and-geolocation-targeting"></a>Cihaz, pazar ve coğrafi konum hedefleme

[!include [banner](includes/banner.md)]

Bu makalede; cihaz, pazar ve coğrafi konum bilgilerini kullanarak Microsoft Dynamics 365 Commerce site oluşturucuda hedef kitlelerin ve hedeflerin nasıl oluşturulacağı, düzenleneceği ve yönetileceği açıklanmaktadır.

Dynamics 365 Commerce, kullanıcı etkileşimini ve memnuniyetini artırmaya yardımcı olmak üzere özel müşteri grupları (*hedef kitleler* olarak bilinir) için sayfa içeriğinizin varyasyonlarını (*hedefler* olarak bilinir) kişiselleştirmenizi sağlar. Öncelikle bir hedef kitle veya hedef oluşturabilirsiniz. Ancak başarılı bir hedefleme deneyimi bu bileşenlerin her ikisini de gerektirir.

Konum, cihaz bilgileri, oturum açma durumu gibi müşteri verilerine ve müşteri web isteklerinden dinamik olarak türetilen diğer bilgilere göre Commerce site oluşturucuda hedef kitleler oluşturur ve yönetirsiniz. Ayrıca Commerce site oluşturucuda e-ticaret modülleri ve parçalarında hedefler oluşturur ve yönetirsiniz.

**Yasal uyarı**: Bu özelliği, hedefleme ve profil oluşturmayla ilgili olanlar da dahil olmak üzere yürürlükteki tüm yasa ve yönetmeliklere uygun olarak kullanmak sizin sorumluluğunuzdadır. 

## <a name="audiences"></a>Hedef kitleler

Hedef kitle, bir kullanıcı grubudur ve gruba üyelik bir dizi dinamik kural tarafından belirlenir. Bu kurallar, müşteri isteklerinde veya diğer kullanılabilir segmentlerde bulunan bilgilere karşı çalıştırılan basit mantık testleridir. VE/VEYA işleçlerini kullanarak birden çok kuralı birleştirebilirsiniz.

Commerce; cihaz bilgileri, oturum açma durumu, başvuran ve sorgu dizesi parametreleri gibi temel segmentleri yerel olarak destekler. Ayrıca üçüncü taraf sağlayıcılara bağlantılar üzerinden genişletilebilir segmentleri de destekler.

### <a name="basic-segments"></a>Temel segmentler

Varsayılan olarak, aşağıdaki segmentler kullanılabilir ve hedef kitle tanımlarına dahil edilebilir:

- **Oturum açılma durumu**: Kullanıcının kimliğinin doğrulanıp doğrulanmadığını test edin.
- **Cihaz platformu**: Aşağıdaki cihaz türlerini test edin:

    - Mobil
    - Masaüstü
    - Tablet
    - Diğer

- **Cihaz İşletim Sistemi**: Aşağıdaki işletim sistemlerini test edin:

    - Windows
    - Linux
    - iOS
    - Android, Diğer

- **Sorgu dizesi parametreleri**: İstek URL'sinin sorgu dizesi parametresindeki bir anahtar-değer çiftinin varlığını test edin. Örneğin, `www.fabrikam.com/en-us/request?promo=true` URL'si için **promosyon** parametresinin **doğru** değerine sahip olduğunu test etmek için bir kural yazılabilir.
- **Tanımlama bilgisi**: İstek URL'sinde etki alanı için ayarlanmış bir tanımlama bilgisi değeri için test edin. Örneğin, bir Fabrikam.com isteği **CustomLayout** adına ve **1** değerine sahip bir tanımlama bilgisi içerebilir. Tanımlama bilgisi testi, bir tanımlama bilgisinin varlığını kontrol eder ancak açıkça bir tane oluşturmaz. Önceki örnekte, JavaScript daha önce başka bir modülden veya başka bir iş sürecinden **CustomLayout** tanımlama bilgisini ayarlamış olmalıdır.

    > [!NOTE]
    > Tanımlama bilgilerini kullanma şeklinizin geçerli yasalara uyumlu olduğundan emin olun.

- **Başvuran**: Kullanıcı sayfayı istemek için bir bağlantıyı takip ederse başvuran, bağlantıyı barındıran sayfanın URL'sidir.

### <a name="extensible-segments"></a>Genişletilebilir segmentler

Commerce, üçüncü taraf segmentasyon sağlayıcılarına bağlanarak kullanılabilir segmentlerin listesini genişletmenize olanak tanır. Segmentasyon sağlayıcısı kullanılabilir segment türlerini açıklar. Coğrafi konum veya segmentasyon sağlayıcısına nasıl bağlanılacağı hakkında daha fazla bilgi için bkz. [Bağlayıcıları yapılandırma ve etkinleştirme](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - Bir harici sağlayıcı etkinleştirilirse performansı tahmin edilemeyen bir hizmete bağlanabilir. Daha iyi bir kullanıcı deneyimi için bir kullanıcı hedefleme içeren bir sayfa isterse ve bu sayfa, üçüncü taraf segment sağlayıcısını denetleyen bir hedef kitleye başvurursa sayfanın varsayılan sürümü gösterilir.
> - Kullanıcı, tanımlama bilgilerine izin verdiğini onaylamalıdır. Kullanıcının tarayıcısı daha sonra ilgili sağlayıcılardan tüm segmentleri talep eder ve sonuçlar, kullanıcıya döndürülen tanımlama bilgisine yerleştirilir. Sayfaya yapılan sonraki istekler, kullanıcıya hedeflenen içerik sunmak için bu bilgileri kullanır. Tanımlama bilgisi uyumu hakkında daha fazla bilgi için bkz. [Tanımlama bilgisi uyumu](cookie-compliance.md).

**Yasal uyarı:** Bu özelliği etkinleştirirseniz verileriniz seçtiğiniz üçüncü taraf sistemlerle paylaşılır. Varsa, üçüncü tarafa hangi verileri sağladığınızı denetleyin. Üçüncü tarafın veri işleme ve uyumluluk standartlarının Microsoft Dynamics 365 Commerce standartlarından farklı olabileceğini unutmayın. Gizliliğiniz Microsoft için önemlidir. Daha fazla bilgi için [Gizlilik ve Tanımlama Bilgileri bildirimimizi](https://privacy.microsoft.com/privacystatement) okuyun.

### <a name="create-an-audience-in-site-builder"></a>Site oluşturucuda hedef kitle oluşturma

Commerce site oluşturucuda bir hedef kitle oluşturmak için şu adımları izleyin.

1. Soldaki gezinti bölmesinde, **Hedef Kitleler**'i seçin.
1. **Yeni**'yi seçin.
1. Hedef kitle için bir ad girin. İsteğe bağlı olarak etiketler ve bir açıklama da ekleyebilirsiniz.
1. **Oluştur**'u ve ardından **Yeni kural bloğu ekle**'yi seçin. Kural bloğu, VE koşullarıyla birleştirilen bir kurallar topluluğudur. Ayrıca aralarında VEYA koşulları olan birden çok kural bloğu da oluşturabilirsiniz.
1. Segmentleriniz için bir veri kaynağı seçin ve ardından segment adını, işleci ve değerleri belirtin. Kural bloğunda daha fazla kural oluşturabilir ve silebilirsiniz ya da tüm kural bloklarını oluşturabilir ve silebilirsiniz. Gerektiğinde kural bloklarını yukarı veya aşağı da taşıyabilirsiniz.

    > [!NOTE]
    > Listede en çok 100 değer bulunabilir ve her liste öğesi en fazla 50 karakter içerebilir.

1. Hedef kitle yapılandırmasından memnun olduğunuzda **Düzenlemeyi bitir**'i seçin. Ardından, hedef kitleyi yayındaki bir hedefte kullanıma hazır hale getirmek için **Yayımla**'yı seçebilirsiniz. Alternatif olarak, hedefle birlikte hedef kitleyi de yayımlayabilirsiniz. 

Hedef kitle düzenlemek için **Hedef Kitleler** sekmesinde hedef kitlenin köprüsünü seçin ve ardından görüntülenen hedef kitle düzenleyicide **Düzenle**'yi seçin. Hedef kitleye başvuran hedeflerin ve sayfaların listesini görüntülemek için hedef kitle listesi görünümünde hedef kitleyi seçin ve ardından **Atamaları Görüntüle** seçeneğini belirleyin. Hedef kitle listesi görünümünde veya hedef kitle düzenleyicide bir hedef kitleyi silmek için hedef kitle zaten yayımlanmışsa hedef kitleyi yayımdan kaldırın ve ardından komut çubuğunda **Sil**'i seçin.

> [!NOTE]
> Hedef kitleler, Commerce site oluşturucusunda site düzeyinde bir kavramdır. Aynı hedef kitleyi çoklu hedefler arasında paylaşabilirsiniz.

### <a name="rename-an-audience-in-site-builder"></a>Site oluşturucuda hedef kitleleri yeniden adlandırma

Commerce site oluşturucuda bir hedef kitleyi yeniden adlandırmak için şu adımları izleyin.

1. Soldaki gezinti bölmesinde, **Hedef Kitleler**'i seçin.
1. Yeniden adlandırmak istediğiniz hedef kitle segmentinin adını seçin.
1. Hedef kitleyi düzenlemeye başlamak için **Düzenle**'yi seçin.
1. Hedef kitle özellikleri bölmesinde, hedef kitle adının yanındaki kalem simgesini seçin.
1. Hedef kitle adını gerektiği gibi düzenleyin.
1. Ad değişikliğini onaylamak için onay işaretini seçin.
1. **Düzenlemeyi bitir**'i seçin.

## <a name="targets"></a>Hedefler

Hedef, seçilen bir veya daha fazla hedef kitlenin üyelerine gösterilen kullanıcı deneyimidir. Bir sayfada veya bir parçada bir ya da daha fazla modülün varyasyonlarını içerebilir. 

Hedeflerinizin ne kadar süre etkin kalmaları gerektiğini belirtmek için bir zamanlama tanımlayabilirsiniz. Bu eylemin, bir içerik koleksiyonunun ne zaman yayımlanacağını belirleyen bir yayımlama grubunun zamanlama eyleminden ayrı olduğunu unutmayın. Ayrıca seçilen hedef kitlelerinin üyelerine nasıl görüneceğine bakmak için hedeflerinizi önizleyebilirsiniz. Ek olarak, bir çakışma olayında hangi hedefin gösterilmesi gerektiğini belirtmek için hedeflerinize öncelik verebilirsiniz.

### <a name="create-a-target"></a>Hedef oluşturma

Commerce site oluşturucuda sayfa modüllerine bir hedef kabuğu oluşturmak için şu adımları izleyin.

1. Soldaki gezinti bölmesinde **Sayfalar** seçin. Ardından, hedeflemek istediğiniz modüllerin bulunduğu sayfanın köprüsünü seçin.
1. Sayfayı düzenlemek üzere denetlemek için **Düzenle**'yi seçin.
1. Yeni bir hedef kabuğu oluşturmak için **Hedef** menüsünde **Yeni hedef**'i seçin. Sayfada gereksinim duyduğunuz gibi birden fazla hedef oluşturabilirsiniz.
1. Hedefiniz için bir ad ve açıklama girin ve ardından **İleri**'yi seçin.
1. Hedeflenen içeriği görecek hedef kitleleri dahil etmek veya hedef kitleleri hariç tutmak için **Ekle**'yi seçin. Sonra **İleri**'yi seçin.

    > [!NOTE]
    > Hedef kitle ataması, hedef oluşturma sırasında isteğe bağlı bir adımdır. Ancak hedefi yayımlamadan önce, istenen kullanıcı gruplarının hedeflenen içeriği görmesini sağlamak için en az bir hedef kitle eklemelisiniz.

1. Saat dilimi ile başlangıç ve bitiş tarih ve saatlerini seçerek hedefinizin görüntülenmesi için zaman aralığını tanımlayın. Hedefi, bu zaman aralığında her zaman gösterilecek şekilde ayarlayabilir veya belirli gün ve saatleri seçebilirsiniz. Bitirdiğinizde **İleri**'yi seçin.

    > [!NOTE]
    > Belirttiğiniz saatler ve saat dilimi geneldir. Farklı zamanlarda veya farklı saat dilimlerinde farklı konumları hedeflemek isterseniz farklı hedefler oluşturmalı ve her konum için istenilen zamanlamayı tanımlamalısınız.

1. Ayrıntıları inceleyin ve her şey doğru göründüğünde **Hedef deneyimi oluştur**'u ve ardından **Hedefe git**'i seçin. Hedef kabuğu oluşturulur. Artık buna modüller ekleyebilirsiniz.
1. Hedeflenecek modülü seçin, üç noktayı (**...**) ve ardından **Geçerli hedefe ekle**'yi seçin. Bir ana modülü hedeflediğinizde, tüm alt birimleri bu hedefin parçası olur. Hedeflenen modüller yeşil renkle vurgulanır.
1. Hedeflenen modülde gerekli içerik güncelleştirmelerini yapın ve hedefe gerektiği gibi daha fazla modül ekleyin. Ardından tüm değişikliklerinizi kaydetmek için **Kaydet**'i seçin.
1. Hedefinizi yayımlamadan önce, incelemek için komut çubuğunda **Önizleme**'yi seçtiğinizden emin olun. Daha sonra aşağıdaki seçeneklerden birini seçebilirsiniz:

    - **Temel önizleme**: İlişkili hedef kitleler olmadan yalnızca seçilen varyasyonu (varsayılan sayfa veya hedef) önizlemek için bu seçeneği belirleyin.
    - **Gelişmiş önizleme**: Sayfada birden fazla hedefiniz varsa ve bunları seçilen bir hedef kitle kümesine ait bir kullanıcı olarak veya belirli bir tarih/saatte önizlemek istiyorsanız bu seçeneği belirleyin. İlgili hedef kitlelerin listesinden seçim yapmak için **İleri**'yi seçin. Tüm hedef kitleler arasından seçim yapmak için filtreyi de kaldırabilirsiniz.

1. Hedef yapılandırmadan memnun kaldığınızda, hedefi yayımlamak için sayfayı yayımlamanız gerekir. Hedefi hemen yayımlamak için **Yayımla**'yı seçin. Alternatif olarak, sayfanın ne zaman yayımlanacağını zamanlamak için bir yayımlama grubu kullanabilirsiniz. Yayımlama grupları hakkında daha fazla bilgi için bkz. [Yayımlama gruplarıyla çalışma](publish-groups.md).

Parçaları da hedefleyebilirsiniz. Yordam benzerdir. Ancak 1. adımda, sol gezinme bölmesinde **Sayfalar** yerine **Parçalar**'ı seçersiniz.

> [!NOTE]
> Ölçümleriniz üzerinde herhangi bir olumsuz etkiden kaçınmak için sayfada veya parçada bir deneme veya hedeflere sahip olabilirsiniz. Hem denemeniz hem de hedefleriniz olamaz.

### <a name="manage-targets"></a>Hedefleri yönet

Hedefleri düzenlemek, çoğaltmak veya silmek için varsayılan sayfaya veya parçaya gidin ve şu adımları izleyin.

1. Açılır menüden **Hedef**'i ve ardından **Hedefleri yönet**'i seçin.
1. Düzenlemek, çoğaltmak veya silmek için bir hedef seçin.
1. Aynı modülde birden fazla hedefiniz varsa veya birden fazla hedefin çakışan zamanlamaları varsa gösterilmeleri gereken sırayı belirtmek için **Hedeflere öncelik ver**'i seçin. Sayfaya veya bir parçaya birden fazla hedef eklerseniz hedeflere öncelik vermenizi hatırlatmak için **Hedeflere öncelik ver** düğmesi de bildirim çubuğunda görünür. Herhangi bir öncelik belirtilmemişse varsayılan olarak en son hedef seçilir.

### <a name="localize-targets"></a>Hedefleri yerelleştirme

XLIFF dosyaları yerelleştirme amacıyla dışarı ve içeri aktarıldığında, sayfalardaki ve parçalardaki hedefler otomatik olarak dahil edilir. Ancak herhangi bir yerel ayar gerekmiyorsa yerelleştirilmiş XLIFF dosyaları içeri aktarıldıktan sonra bunlar için hedefleri silebilirsiniz.

> [!NOTE]
> Hedefler kanal başına ve yerel ayara göre yönetilir. Kanal veya yerel ayardaki hedeflerde yaptığınız değişiklikler, otomatik olarak diğer kanallara ya da yerel ayarlara taşınmaz.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
