---
title: Özellik yönetimine genel bakış
description: Bu makalede, Özellik yönetimi ve bunu nasıl kullanabileceğiniz açıklanmaktadır.
author: Peakerbl
ms.date: 01/10/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 0691bc34ac8b57d20cfbeb58b6a2e2a03a57d067
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850074"
---
# <a name="feature-management-overview"></a>Özellik yönetimine genel bakış

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

Özellikler, her sürümüne eklenir ve güncelleştirilir. Özellik yönetimi deneyimi, her sürümde teslim edilen özelliklerin listesini görüntüleyebileceğiniz bir çalışma alanı sağlar. Daha sonra özellik belgelerini görüntülemek ve özellikleri etkinleştirmek veya devre dışı bırakmak için çalışma alanını kullanabilirsiniz.

## <a name="the-feature-management-workspace"></a>Özellik yönetimi çalışma alanı

Panoda uygun kutucuğu seçerek **Özellik yönetimi** çalışma alanını açabilirsiniz. Özellik yönetimi deneyimi tarafından desteklenen tüm sürümlere ait özelliklerin listesini gösteren bir sayfa görürsünüz. 

Özellik listesi sekmesi aşağıdaki bilgileri içerir:

- **Özellik adı** – Eklenen özelliğin açıklaması.
- **Durum**: Simge, bir özelliğin açık olduğunu (onay işareti), kapalı olduğunu (boş), açılmak üzere zamanlandığını (saat), zorunlu olduğunu (kilit), açmadan önce dikkat edilmesi gerektiğini (uyarı simgesi) veya açılamadığını (X) belirtir. Gösterilen ayar tüm tüzel kişilikler için kullanılır. Bir özellik açılsa bile hala güvenlik tarafından denetlendiğini unutmayın. Bu nedenle, özellik yalnızca güvenlik rolüne göre erişimi olan kullanıcılar tarafından kullanılabilir. Ayrıca, yalnızca kullanıcının erişebileceği tüzel kişilikler için de kullanılabilir.
- **Etkinleştirme tarihi** – Özelliğin açıldığı veya açık olarak planlandığı tarih.
- **Özellik eklendi** – Özelliğin ortamınıza eklendiği tarih. Bu tarih, aylık sürüm döngüleri sırasında ortamınızı güncelleştirdiğinizde otomatik olarak girilir.
- **Özellik durumu**: Özelliğin geçerli yaşam döngüsü durumudur: **Önizleme**, **Yayımlanan** (boş olarak gösterilir), **Varsayılan olarak açık** ve **Zorunlu**. Bu durumlar, bu makalenin ilerleyen bölümlerinde daha ayrıntılı olarak ele alınmaktadır. 
- **Modül** – Yeni özellikten etkilenen modül.

> [!NOTE]
> **Özellik durumu** sütunu, 10.0.21 sürümünden itibaren dahil edilmiştir.

Bir özellik seçtiğinizde, ayrıntılar bölmesinde özellik listesinin sağında daha fazla bilgi görüntülenir. Bölmenin en üstünde özellik adı, özelliğin eklendiği tarih, özelliğin etkilediği modül ve **Daha fazla bilgi edinin** bağlantısını görürsünüz. Özelliğin belgelerini görüntülemek için bu bağlantıyı seçin. Belge yoksa, geçici bir sayfaya yönlendirilirsiniz. Ayrıntılar bölmesi ayrıca özellik hakkında kendi açıklamalarınızı ekleyebileceğiniz bir **Açıklama** alanı da içerir.

**Özellik yönetimi**, her biri çalışma alanı aynı zamanda içindeki özelliklerin listesi bulunan çeşitli sekmeler içerir.

- **Yeni** - Bu sekme, son aylık güncelleştirmeden sonra eklenen tüm özellikleri gösterir. Aylık güncelleştirmeleri atladıysanız, sekme, son güncelleştirmeden bu yana eklenen tüm yeni özellikleri gösterir. En yeni özellikler listenin en üstünde yer alır. Ayrıca, yeni özelliklerin toplam sayısı sayfanın üst kısmındaki bir kutucukta gösterilir.
- **Etkin değil**: Bu sekmede, açık olan tüm özellikler gösterilir. En yeni özellikler listenin en üstünde yer alır. Ayrıca sayfanın üst kısmındaki bir kutucuk, şu anda kapalı olan yeni özelliklerin toplam sayısını gösterir.
- **Planlanan** - Bu sekme, gelecekteki açılmak üzere zamanlanmış tüm özellikleri gösterir. En erken zamanlanan tarihe sahip özellikler listenin en üstünde görüntülenir. Ayrıca sayfanın üst kısmındaki bir kutucuk, zamanlanan özelliklerin toplam sayısını gösterir.
- **Tümü** – Bu sekme tüm özellikleri gösterir. En yeni özellikler listenin en üstünde yer alır.

## <a name="feature-states"></a>Özellik durumları
Özellikler, Özellik yönetiminde tanıtılmalarından üründe zorunlu hale gelinceye kadar çeşitli durumlar arasında geçiş yapabilir. Bu bölümde, geçerli özellik durumları açıklanmaktadır.

### <a name="preview-features-optional"></a>Önizleme özellikleri (isteğe bağlı)

Ürün takımları yeni bir özelliği başlangıçta bir önizleme özelliği olarak başlatmaya karar verebilir. Önizleme özellikleri varsayılan olarak etkin değildir ve isteğe bağlıdır. Sahibi olan ürün takımı başarılı bir önizleme dönemini tamamladıktan sonra özellikleri yayımlanacak şekilde güncelleştirir.

> [!NOTE]
> Önizleme özellikleri belirli önizleme [hüküm ve koşullarına](https://go.microsoft.com/fwlink/?linkid=2105274) tabidir. 

### <a name="released-features-optional"></a>Yayımlanan özellikler (isteğe bağlı)

Bu özellikler için **Özellik durumu** sütunu boştur. Başlangıçta yayımlanan olarak eklenen özellikler varsayılan olarak açık değildir ve bu özellikleri etkinleştirmek isteğe bağlıdır. Önizlemeden güncelleştirilen özellikler etkinleştirme durumlarını korur.

### <a name="on-by-default-features-optional"></a>Varsayılan olarak açık özellikler (isteğe bağlı)

**Varsayılan olarak açık** olarak güncelleştirilen özellikler varsayılan olarak açıktır ancak devre dışı bırakılabilir. En az altı ay boyunca **Yayımlanan** durumunda kaldıktan sonra, devre dışı bırakılabilen özelliklerin bir sonraki ana sürümde bu duruma geçmeleri beklenir. **Varsayılan olarak açık**'a geçiş yapan özelliklerin, sürümün [Yenilikler](../whats-new-changed.md) makalesinde bildirilmeleri beklenir. Güncelleştirme, sahibi olan ürün takımı tarafından başlatılır.

> [!NOTE]
> Bu özellikler otomatik olarak etkinleştirileceğinden, kuruluşunuzun bu özellikleri almaya hazır olup olmadığını veya daha fazla zaman gerekip gerekmediğini belirlemeniz önemlidir. Daha fazla zaman gerekiyorsa bu özellikleri geçici olarak devre dışı bırakmanız gerekebilir. Bir özelliğin **Varsayılan olarak açık** durumuna geçişinin genellikle özelliğin **Zorunlu** durum haline gelmesi hedeflenmeden önceki ana sürümde yapıldığını unutmayın. Bu noktada, özelliği devre dışı bırakma seçeneğiniz olmaz. 

### <a name="mandatory"></a>Zorunlu

**Zorunlu** durumu, özellikler için beklenen son durumdur. Özelliklerin açık olduğunu ve Microsoft ile iletişim kurmadan bunları devre dışı bırakamayacağınızı gösterir. İsteğe bağlı özelliklerin iki ana sürümden sonra zorunlu hale gelmesi beklenir. Kritik özellikler, özel durum nedeniyle zorunlu olarak tanıtılabilir.

## <a name="example-of-expected-feature-lifecycles"></a>Beklenen özellik yaşam döngüsü örneği

Devre dışı bırakılabilen ve yayımlanan olarak eklenmiş olup Nisan sürümünden önce veya bu sürümün bir parçası olarak isteğe bağlı olan özelliklerin bir sonraki Ekim sürümünde **Varsayılan olarak açık** durumuna geçmesi beklenir. Bu özelliklerin bir sonraki yılın Nisan ayında **Zorunlu** olmaları beklenir.

Devre dışı bırakılabilen ve yayımlanan olarak eklenmiş olup Nisan sürümünden önce veya bu sürümün bir parçası olarak isteğe bağlı olan özelliklerin bir sonraki yılın Nisan ayında **Zorunlu** durumuna geçmesi beklenir.

## <a name="enable-a-feature"></a>Bir özelliği etkinleştirme

Bir özellik açılmamışsa ayrıntılar bölmesinde **Şimdi etkinleştir** düğmesi görünür. Bu özelliği etkinleştirmek için bu düğmeyi kullanabilirsiniz.

Bazı özellikler etkinleştirildikten sonra devre dışı bırakılamaz. Açmaya çalıştığınız bir özellik etkinleştirilemiyorsa bir uyarı alırsınız. Bu noktada, işlemi iptal etmek ve özelliği devre dışı bırakmak için **İptal**'i seçebilirsiniz. Ancak özelliği etkinleştirirmek için **Etkinleştir**'i seçerseniz daha sonra devre dışı bırakamazsınız.

Bazı özelliklerde, siz özelliği etkinleştirmeden önce ek bilgi sağlayan bir ileti görüntülenir. Bu özellikler sarı bir uyarı sembolüyle belirtilir. Özellik etkinleştirildiğinde neler olacağını daha iyi anladığınızdan emin olmak için ek bilgileri dikkatle okumalısınız. Ancak özelliği açmak için yine de **Etkinleştir**'i seçebilirsiniz.

Bazı özellikler, bir eylem alınıncaya kadar özelliğin etkinleştirilmediğini gösteren bir ileti görüntüler. Bu özellikler kırmızı X sembolüyle belirtilir. Özellik etkinleştirilmeden önce açıklama kısmında açıklanan eylemleri gerçekleştirmelisiniz. Örneğin, bir yapılandırma anahtarı devre dışı bırakılıncaya kadar bir özelliği kullanamazsını, önce yapılandırma anahtarını devre dışı bırakmanız ve ardından özelliği etkinleştirmek için özellik yönetimine geri dönmelisiniz.

Özellik etkinleştirildikten sonra, ayrıntılar bölmesindeki **Daha fazla bilgi** bağlantısının altında bir ileti görüntülenir. Bu ileti, özelliğin etkinleştirildiğini veya özelliğin etkinleştirilmek üzere zamanlandığı gelecekteki tarihi belirtir. İleti, özellik listesinde özelliği her seçtiğinizde görüntülenecektir.

Gelecekte etkinleştirilmek üzere zamanlanmış özellikler **Zamanlandı** sekmesinde görünür. Bir toplu işlem, sistem tarihiyle temsil edilen saat dilimine göre belirtilen tarihteki gece yarısında bu özellikleri etkinleştirir.

## <a name="reschedule-a-feature"></a>Bir özelliği yeniden zamanlama

Bir özellik gelecekte etkinleştirilmek üzere zamanlanmışsa ayrıntılar bölmesinde bir **Zamanla** düğmesi görünür. **Etkinleştirme tarihini** değeri, başka bir tarihe değiştirmek için bu düğmeyi kullanabilirsiniz.

1. Yeniden zamanlamak için zamanlanmış özelliği seçin ve sonra ayrıntılar bölmesinde **Zamanla**'yı seçin.
2. Görüntülenen iletişim kutusundaki **Etkinleştirme tarihi** alanında, özelliğin etkinleştirilmesi gereken yeni tarihi belirtin.
3. Özelliği yeniden zamanlamak için **Etkinleştir**'i veya zamanlamayı iptal etmek için **Devre dışı bırak**'ı seçin.

## <a name="disable-a-feature"></a>Bir özelliği devre dışı bırakma

Bir özellik etkinleştirilmişse ayrıntılar bölmesinde **Devre Dışı Bırak** düğmesi görünür. Bu özelliği devre dışı bırakmak için bu düğmeyi kullanabilirsiniz. Özellik devre dışı bırakılamıyorsa **Devre Dışı Bırak** düğmesi kullanılamaz. 

Özellik devre dışı bırakıldıktan sonra, ayrıntılar bölmesindeki **Daha fazla bilgi** bağlantısının altında bir ileti görünür. Bu ileti, özelliğin henüz etkinleştirilmediğini belirtir. İleti, özellik listesinde özelliği her seçtiğinizde görüntülenecektir. Etkinleştirilmemiş özellikler **Etkin değil** sekmesinde görünür.

## <a name="features-that-must-be-enabled"></a>Etkinleştirilmesi gereken özellikler

Bazı durumlarda, bir güncelleştirme yaptığınızda otomatik olarak etkinleştirilmesi gereken bir kritik özellik sunulur. Bu özellikler, **Etkinleştirme tarihi** alanında belirtilen tarihte otomatik olarak etkinleştirilir. Bu özellikler için, ayrıntılar bölmesindeki **Daha fazla bilgi edinin** bağlantısının altında bir ileti görüntülenir. Bu ileti, özelliğin etkinleştirildiğini veya özelliğin etkinleştirilmek üzere zamanlandığı gelecekteki tarihi belirtir. İleti, özellik listesinde özelliği her seçtiğinizde görüntülenecektir.

## <a name="enable-all-features"></a>Tüm özellikleri etkinleştir

**Tümünü Etkinleştir** düğmesini seçerek tüm özellikleri etkinleştirebilirsiniz. 

**Tümünü etkinleştir**'i seçtiğinizde, aşağıdaki bilgileri sağlamanız gereken yerde bir seçenek görünür:

- Etkinleştirilmeden önce onay gerektiren tüm özelliklerin listesi. Listedeki özellikleri etkinleştirmek istiyorsanız **Onay gerektiren özellikleri etkinleştir** düğmesi için **Evet**'i seçin.
- Etkinleştirilemeyen özellilkerin listesi gösterilecektir. Bu özellikler etkinleştirilmez.

Etkinleştirilebilir tüm özellikler etkinleştirilecektir. Bir özellik gelecekte etkinleştirilmek üzere planlandıysa plan değişmeyecektir. 

## <a name="enable-all-features-automatically"></a>Tüm özellikleri otomatik olarak etkinleştirme

Tüm yeni özellikleri otomatik olarak etkinleştirmek isterseniz yeni özellikler eklendiğinde ne olacağını değiştirmek için çalışma alanı başlığının altındaki açılır listeyi kullanabilirsiniz.

- Ortamınıza eklenen tüm yeni özellikleri otomatik olarak etkinleştirmek için **Yeni özellikleri otomatik olarak etkinleştir**'i seçin.
- Tüm kullanılabilir yeni özelliklerin ortamınıza eklendiğinde varsayılan olarak kapalı olması için **Yeni özellikleri otomatik olarak etkinleştirme**'yi seçin.

Tüm özelliği otomatik olarak etkinleştirdiğinizde, **Tümünü Etkinleştir** düğmesini tıkladığınızda etkinleştirilecek tüm özellikleri etkinleştirir. Bu, onay gerektiren özellikleri veya bir eylem alınıncaya kadar etkinleştirilemez özellikleri etkinleştirmez.

## <a name="check-for-updates"></a>Güncelleştirmeleri denetle

Özellikler, her günceştirmeden sonra ortamınıza eklenir. Ancak, **Güncelleştirmeleri denetle** düğmesine tıklayarak güncelleştirmeleri el ile denetleyebilirsiniz. Güncelleştirme sonra sisteme eklenen herhangi bir özellik, özellikler listesine eklenecektir. Örneğin, bir sürümden sonra kesintisiz bir özellik etkinse güncellemeleri kontrol edebilirsiniz ve özellik listenize eklenir.

## <a name="assigning-roles"></a>Rolleri atama

**Özellik Yönetimi** çalışma alanı, sistem yöneticileri tarafından ve özellik yönetimi rolü veya özellik görüntüleyicisi rolüne atanmış kullanıcılar tarafından açılabilir. Bu iki rol özellik yönetimi deneyimini destekleyecek şekilde oluşturuldu. Özellik yöneticisi rolündeki kullanıcılar, herhangi bir özelliği açabilir veya kapatabilir. Ayrıca bu özellik için **Açıklamalar** bölümünü de güncelleştirebilir. Özellik görüntüleyicisi rolündeki kullanıcılar yalnızca **Özellik yönetimi** çalışma alanını görüntüleyebilir. Özellikleri açıp kapatamazlar.

Özellik yöneticisi rolü ve Özellik görüntüleyicisi rolü, bir kullanıcının sahip olduğu güvenliği geçersiz kılmaz. Kullanıcının özellikleri açıp kapatamayacağını denetlerler. Özelliklerin kendisine erişim sağlamazlar.

## <a name="features-that-use-configuration-keys"></a>Yapılandırma anahtarlarını kullanan özellikler

Bir özellik konfigürasyon anahtarını kullanırsa, ancak konfigürasyon anahtarı açık değilse, **Özellik Yönetimi** çalışma alanı özelliği kullanılabilen özellikler listesinde göstermez. Yapılandırma anahtarını açtıktan sonra, **Güncelleştirme için denetle** menü öğesini kullanarak özellik listesini güncelleştirmeniz gerekir. Özellik daha sonra özellik listesinde görünür.

Konfigürasyon anahtarını kapatırsanız, özellik listesinden kaldırılmaz.

## <a name="data-entities"></a>Veri varlıkları

**Özellik yönetimi** olarak adlandırılan bir veri varlığı, bir ortamdan Özellik yönetimi özelliklerini içe aktarmanızı sağlar ve sonra başka bir ortama içe aktarabilirsiniz. Bu varlık, yalnızca var olan özellikleri güncelleştirir. Varlıktaki işletme mantığı, **Özellik yönetimi** çalışma alanı üzerinde kullanılan aynı kuralların, içe aktarma tamamlandığında kullanılmasına yardımcı olur. Örneğin, içe aktarma işlemi sırasında tarihi kaldırarak zorunlu özellik ayarını geçersiz kılamazsınız.

Aşağıdaki örnekler, veri içe aktarmak için **Özellik Yönetimi** varlığını kullandığınızda ortaya çıkan durumu tanımlar.

- **Etkin** alanının değerini **Evet** olarak değiştirirseniz özellik etkinleştirilir ve **Etkinleştirme tarihi** alanı geçerli tarihe ayarlanır.
- **Etkin** alanının değerini **Hayır** olarak ayarlarsanız veya **EnableDate** alanını boş bırakırsanız özellik devre dışı bırakılır ve **Etkinleştirme tarihi** alanı temizlenir. Zorunlu özelliği veya etkinleştirildikten sonra devre dışı bırakılamayan bir özelliği devre dışı bırakamazsınız.
- **EnableDate** alanının değerini gelecekteki bir tarihle değiştirirseniz, özellik bu tarih için zamanlanır.
- **Etkin** alanının değerini, **Evet** olarak değiştirirseniz ve **EnableDate** alanının değerini gelecekteki bir tarihe değiştirirseniz, özellik bu tarih için zamanlanır. 
- **Etkin** alanının değerini, **Hayır** olarak değiştirirseniz ve **EnableDate** alanının değerini gelecekteki bir tarihe değiştirirseniz, özellik bu tarih için zamanlanır.
- Özellik etkinse ve gelecekteki bir tarihe ayarlanmış bir **EnableDate** alanı eklerseniz özellik etkin kalır. Özelliği yeniden zamanlamak için **Etkin** alanının değerini **Hayır** olarak değiştirmelisiniz.

## <a name="feature-management-and-flighting"></a>Özellik yönetimi ve denemesi

Özellik yönetimi, her sürümde sunulan özellikleri denetlemenize olanak tanır. Deneme sürümü, Microsoft teams'in özellikleri sınırlı sayıda müşteriye sunmasını sağlayarak özelliklerin tüm müşterileri etkilemeden test edilebilmesini ve doğrulanabilmesini sağlar. Özellik yönetimi, herhangi bir özelliğin deneme sürümünü kontrol etmez.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>ISV özelliklerini veya özel özellikleri açmak için Özellik yönetimini kullanma

Özellik yönetimi şu anda bağımsız yazılım satıcılarından (ISV) ve özel özelliklerde bulunan özellikler için kullanılamamaktadır. Ancak Microsoft, özellik yönetimini geliştirmek için daha fazla işlevsellik ekliyor. Bu geliştirmeler tamamlandıktan sonra, Microsoft, Özellik yönetimini tüm özellikler tarafından kullanılabilir hale getirir ve özellikleri kullanmak için bunları güncelleştirmeye ilişkin yönergeleri sağlar.

## <a name="frequently-asked-questions-faq"></a>Sık sorulan sorular (SSS)

### <a name="when-are-features-added-removed-or-changed"></a>Özellikler ne zaman eklenir, kaldırılır veya değiştirilir? 
Özellikler, sahibi olan ürün takımları tarafından yapılan kod değişiklikleri yoluyla eklenir, kaldırılır ve değiştirilir. Bu değişiklikleri almak için ortamlar güncelleştirilmelidir.

### <a name="does-a-feature-become-mandatory-automatically"></a>Bir özellik otomatik olarak zorunlu hale gelir mı? 
Hayır, bir özellik otomatik olarak zorunlu hale gelmez. Sahibi olan ürün takımlarının bir kod değişikliği yapması gerekir.

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Neden belirli bir "zorunluluk nedeniyle etkinleştirme tarihi" yok? 
Güncelleştirme sürümü zamanlaması değişkendir, ortam güncelleştirme zamanlaması değişkendir ve müşteriler bazı güncelleştirmeleri atlamayı isteyebilir. Sonuç olarak, belirli tarihler belirlenmesi zordur. 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>Zorunlu özellikler için belgeler nerededir? 
Bu belgeler, Dynamics 365 uygulama takımlarından gelir. Bu özelliklerden genellikle [İstemci özellik durumlarına yapılan güncelleştirmeler](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states) veya [Kaldırılmış ya da kullanım dışı özellikler](../../../dev-itpro/migration-upgrade/deprecated-features.md) bölümünde bahsedilir. 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Bir özelliğin zorunlu olarak etkinleştirileceğini belirten bir ürün içi bildirim veya sinyal var mıdır? 
Özelliği zorunlu hale getirme ile ilgili bir bildirim mekanizması şu anda mevcut değildir.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Daha önceden müşterinin haberi olmadan özellikler etkinleştirildi mi? 
Evet, özellikler aşağıdaki durumlarda müşterinin bilgisi olmadan etkinleştirilebilir:
- Bu özellik **Varsayılan olarak açık** durumuna taşınmıştır. Bu durumda, özellik yine de devre dışı bırakılabilir. 
- Özellik **Zorunlu** olarak güncelleştirilir. Bu değişiklik yalnızca ana sürüm ile birlikte gerçekleşir. Kritik özellikler, özel durum olarak herhangi bir güncelleştirmede **Zorunlu** durumuna taşınabilir.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>Özellik sınırlı dağıtımı nedir ve özellik yönetimiyle nasıl ilişkilidir? 
Özellik sınırlı dağıtımları, Microsoft'un denetlediği gerçek zamanlı açma/kapama geçişleridir. Bunlar Özellik Yönetimi tarafından sağlanan müşteri denetiminden ayrıdır. 
- Özel Önizleme özellikleri, Özellik Yönetiminde, sınırlı dağıtımları yapılana kadar listelenmeyecektir. Üretimde, müşterinin gerçekleşmesi için özel bir programın parçası olmayı kabul etmesi gerekir.
- Genel Önizleme özellikleri ve Serbest bırakılan özellikler (genel kullanıma sunulan) sınırlı dağıtımları kapatılmadıkça Özellik Yönetimi'nde listelenecektir. Bir özelliğin sınırlı dağıtımını kapatmak, önemli bir sorun bulunursa (genellikle müşteri başına bir işlem olduğunda), ürün takımları için son çare seçeneği olarak kabul edilir.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>Daha önceden müşterinin haberi olmadan özelliklerin sınırlı dağıtımı kapatıldı mı? 
Evet, bir özellik işlevsel bir etkisi olmadan bir ortamın işleyişini etkiliyorsa, varsayılan olarak etkinleştirilebilir.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>Özellik etkinleştirme kod içinde nasıl denetlenebilir?
Özellik sınıfının bir örneğini geçirerek, **FeatureStateProvider** sınıfında  **isFeatureEnabled** yöntemini kullanın. Örnek: 

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>Özellik etkinleştirme meta veri içinde nasıl denetlenebilir?
**FeatureClass** özelliği, bazı meta verilerin bir özellikle ilişkili olduğunu belirtmek için kullanılabilir. **BatchContentionPreventionFeature** gibi özellik için kullanılan sınıf adı kullanılmalıdır. Bu meta veriler yalnızca bu özellikte görünür. **FeatureClass** özelliği menülerde, menü öğelerinde, enum değerlerinde ve tablo/görünüm alanlarında kullanılabilir.

### <a name="what-is-a-feature-class"></a>Özellik sınıfı nedir?
Özellik Yönetimindeki özellikler *özellik sınıfları* olarak tanımlanır. Özellik sınıfı **IFeatureMetadata uygular** ve Özellik Yönetimi çalışma alanına kendisini tanımlamak için özellik sınıfı özniteliğini kullanır. Kodda **FeatureStateProvider** API'sı ve meta verilerde **FeatureClass** sınıf özelliği kullanılarak etkinleştirme için kontrol edilebilecek çok sayıda özellik sınıfı örneği vardır. Örnek: 

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>Bazı özellik sınıfları tarafından uygulanan IFeatureLifecycle nedir?
IFeatureLifecycle, özellik yaşam döngüsü aşamasını gösteren bir Microsoft iç mekanizmasıdır. Özellikler şu olabilir:
- `PrivatePreview`: Sınırlı dağıtımın görünür olmasını gerektirir.
- `PublicPreview`: Varsayılan olarak gösterilir ancak özelliğin önizlemede olduğunu belirten bir uyarı görüntülenir.
- `Released`: Tam olarak yayınlanmış.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
