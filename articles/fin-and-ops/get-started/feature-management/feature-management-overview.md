---
title: Özellik yönetimine genel bakış
description: Bu konu Özellik Yönetimi özelliğini ve nasıl kullanabileceğinizi açıklar.
author: mikefalkner
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: d6aea8651c00b975cf158492e38bb147e908bc56
ms.sourcegitcommit: 672c94704e9a2b0ec7ee3c111d4ceb1bb8597969
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2019
ms.locfileid: "1632065"
---
# <a name="feature-management-overview"></a>Özellik yönetimine genel bakış

[!include [banner](../../includes/banner.md)]

Özellikler, Microsoft Dynamics 365 for Finance and Operations'ın her sürümünde eklenir ve güncelleştirilir. Özellik yönetimi deneyimi, her sürümde teslim edilen özelliklerin listesini görüntüleyebileceğiniz bir çalışma alanı sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz.

## <a name="the-feature-management-workspace"></a>Özellik yönetimi çalışma alanı

Panoda uygun kutucuğu seçerek **Özellik yönetimi** çalışma alanını açabilirsiniz. Özellik yönetimi deneyimi tarafından desteklenen tüm sürümlere ait özelliklerin listesini gösteren bir sayfa görürsünüz. Zamanla Microsoft Özellik yönetimi deneyimini, özellikleri yönetmenize yardımcı olacak ek işlevler içerecek şekilde geliştirecektir.

Özellik listesi sekmesi aşağıdaki bilgileri içerir:

- **Özellik adı** – Eklenen özelliğin açıklaması.
- **Etkin durum** – Bir sembol, bir özelliğin etkinleştirildiğini (onay işareti), etkinleştirilmediğini (boş), etkinleştirilmek üzere zamanlandığını (saat) veya zorunlu olarak etkinleştirildiğini (kilit) gösterir. Burada gösterilen ayar tüm tüzel kişilikler için kullanılır. Bir özellik açılsa bile hala güvenlik tarafından denetlendiğini unutmayın. Bu nedenle özellik güvenlik rolüne göre yalnızca erişimi olan kullanıcılar tarafından kullanılabilir. Ayrıca, yalnızca kullanıcının erişebileceği tüzel kişilikler için de kullanılabilir.
- **Etkinleştirme tarihi** – Özelliğin açıldığı veya açık olarak planlandığı tarih.
- **Özellik eklendi** – Özelliğin ortamınıza eklendiği tarih. Bu tarih, aylık sürüm döngüleri sırasında ortamınızı güncelleştirdiğinizde otomatik olarak girilir.
- **Modül** – Yeni özellikten etkilenen modül.

Bir özellik seçtiğinizde, ayrıntılar bölmesinde özellik listesinin sağında ek bilgiler görüntülenir. Bölmenin en üstünde özellik adı, özelliğin eklendiği tarih, özelliğin etkilediği modül ve **Daha fazla bilgi edinin** bağlantısını görürsünüz. Özelliğin belgelerini görüntülemek için bu bağlantıyı seçin. Belge yoksa, geçici bir sayfaya yönlendirilirsiniz. Ayrıntılar bölmesi ayrıca özellik hakkında kendi açıklamalarınızı ekleyebileceğiniz bir **Açıklama** alanı da içerir.

**Özellik yönetimi**, her biri çalışma alanı aynı zamanda içindeki özelliklerin listesi bulunan çeşitli sekmeler içerir.

- **Yeni** - Bu sekme, son aylık güncelleştirmeden sonra eklenen tüm özellikleri gösterir. Aylık güncelleştirmeleri atladıysanız, sekme, son güncelleştirmeden bu yana eklenen tüm yeni özellikleri gösterir. En yeni özellikler listenin en üstünde yer alır. Ayrıca, yeni özelliklerin toplam sayısı sayfanın üst kısmındaki bir kutucukta gösterilir.
- **Etkin değil** – bu sekmede etkinleştirilmemiş olan tüm özellikler gösterilir. En yeni özellikler listenin en üstünde yer alır. Ayrıca, açılmamış olan yeni özelliklerin toplam sayısı sayfanın üst kısmındaki bir kutucukta gösterilir.
- **Planlanan** - Bu sekme, gelecekteki açılmak üzere zamanlanmış tüm özellikleri gösterir. En erken zamanlanan tarihe sahip özellikler listenin en üstünde görüntülenir. Ayrıca, zamanlama yeni özelliklerin toplam sayısı sayfanın üst kısmındaki bir kutucukta gösterilir.
- **Tümü** – Bu sekme tüm özellikleri gösterir. En yeni özellikler listenin en üstünde yer alır.

## <a name="turn-on-a-feature"></a>Bir özelliği etkinleştirme

Bir özellik etkinleştirilmemişse, ayrıntılar bölmesinde **Şimdi Etkinleştir** düğmesi görüntülenir. Bu özelliği açmak için bu düğmeyi kullanabilirsiniz.

- Açmak istediğiniz özelliği seçin, daha sonra ayrıntılar bölmesinde **Şimdi Etkinleştir**'i seçin. Özellik açık.

Açtıktan sonra bazı özellikler kapatılamaz. Açmaya çalıştığınız bir özellik kapatılamıyorsa, bir uyarı alırsınız. Bu aşamada, işlemi iptal etmek ve özelliği kapatmak için **İptal**'i seçebilirsiniz. Ancak, **Etkinleştir**'i seçip özelliği açarsanız daha sonra kapatamazsınız.

Özellik açıldıktan sonra, ayrıntılar bölmesindeki **Daha fazla bilgi edinin** bağlantısının altında bir ileti görüntülenir. Bu mesaj, özelliğin açıldığını veya özelliğin gelecekteki bir zamanda açılmak üzere zamanladığını belirtir. İleti, özellik listesinde özelliği her seçtiğinizde görüntülenecektir.

Gelecekte açık olarak zamanlanan özellikler **Zamanlanmış** sekmesinde görüntülenir. Sistem tarihiyle temsil edilen saat dilimine göre bir toplu işlem, belirtilen tarihteki gece yarısına açık olacak.

## <a name="reschedule-a-feature"></a>Bir özelliği yeniden zamanlama

Bir özellik gelecekte açılmak üzer zamanlanmışsa, bir **Zamanla** düğmesi ayrıntılar bölmesinde görüntülenir. **Etkinleştirme tarihini** değeri, başka bir tarihe değiştirmek için bu düğmeyi kullanabilirsiniz.

1. Yeniden zamanlamak için zamanlanmış özelliği seçin ve sonra ayrıntılar bölmesinde **Zamanla**'yı seçin.
2. Görüntülenen iletişim kutusunda, **Etkinleştirme tarihi** alanında, özelliğin açılması gereken yeni tarihi belirtin.
3. Özelliği yeniden zamanlamak için **Etkinleştir**'i veya zamanlamayı iptal etmek için **Devre dışı bırak**'ı seçin.

## <a name="turn-off-a-feature"></a>Bir özelliği kapatmak

Bir özellik açıksa, ayrıntılar bölmesinde **Devre dışı bırak** düğmesi görüntülenir. Bu özelliği kapatmak için bu düğmeyi kullanabilirsiniz. Özellik etkinleştirildikten sonra kapatılamıyorsa, **Devre dışı bırak** düğmesi kullanılamaz.

- Kapatmak için özelliği seçin ve sonra ayrıntılar bölmesinde **Devre dışı bırak**'ı seçin. Bu özellik kapanır ve **Etkinleştirme tarihi** alanı temizlenir.

Özellik kapandıktan sonra, ayrıntılar bölmesindeki **Daha fazla bilgi edinin** bağlantısının altında bir ileti görüntülenir. Bu ileti, özelliğin henüz açılmadığını belirtir. İleti, özellik listesinde özelliği her seçtiğinizde görüntülenecektir. Açılmamış özellikler **Etkinleştirilmemiş** sekmesinde görünür.

## <a name="features-that-must-be-turned-on"></a>Açılması gereken özellikler

Bazen, güncelleştirme yaptığınızda otomatik olarak açılması gereken kritik bir özellik sunulabilir. Bu özellikler, **Etkinleştirme tarihi** alanında belirtilen tarihte otomatik olarak açılır. Bu özellikler için, ayrıntılar bölmesindeki **Daha fazla bilgi edinin** bağlantısının altında bir ileti görüntülenir. Bu mesaj, özelliğin açıldığını veya özelliğin gelecekteki bir zamanda açılacağını belirtir. İleti, özellik listesinde özelliği her seçtiğinizde görüntülenecektir.

## <a name="turn-on-all-features-automatically"></a>Tüm özellikleri otomatik olarak aç

Varsayılan olarak, çalışma ortamınıza eklenen tüm özellikler zorunlu özellikler olmadıkça kapalıdır. Ancak, tüm yeni özellikleri otomatik olarak etkinleştirmek istiyorsanız, yeni özellikler eklendiğinde neler olacağını değiştirmek için çalışma alanı başlığının altındaki açılan listeyi kullanabilirsiniz.

- **Tüm yeni özellikler, varsayılan olarak etkinleştirilecektir**'i seçerek ortamınıza eklenen tüm yeni özelliklerin otomatik açılmasını sağlayın.
- **Tüm yeni özellikler, varsayılan olarak devre dışı olacaktır**'i seçerek ortamınıza eklenen tüm yeni özelliklerin otomatik kapatılmasını sağlayın.

## <a name="assigning-roles"></a>Rolleri atama

**Özellik Yönetimi** çalışma alanı, sistem yöneticileri tarafından ve özellik yönetimi rolü veya özellik görüntüleyicisi rolüne atanmış kullanıcılar tarafından açılabilir. Bu iki rol özellik yönetimi deneyimini destekleyecek şekilde oluşturuldu. Özellik yöneticisi rolündeki kullanıcılar, herhangi bir özelliği açabilir veya kapatabilir. Ayrıca bu özellik için **Açıklamalar** bölümünü de güncelleştirebilir. Özellik görüntüleyicisi rolündeki kullanıcılar yalnızca **Özellik yönetimi** çalışma alanını görüntüleyebilir. Özellikleri açıp kapatamazlar.

Özellik yöneticisi rolü ve Özellik görüntüleyicisi rolü, bir kullanıcının sahip olduğu güvenliği geçersiz kılmaz. Kullanıcının özellikleri açıp kapatamayacağını denetlerler. Özelliklerin kendisine erişim sağlamazlar.

## <a name="features-that-use-configuration-keys"></a>Yapılandırma anahtarlarını kullanan özellikler

Bir özellik konfigürasyon anahtarını kullanırsa, ancak konfigürasyon anahtarı açık değilse, **Özellik Yönetimi** çalışma alanı özelliği kullanılabilen özellikler listesinde göstermez. Yapılandırma anahtarını açtıktan sonra, **Güncelleştirme için denetle** menü öğesini kullanarak özellik listesini güncelleştirmeniz gerekir. Özellik daha sonra özellik listesinde görünür.

Konfigürasyon anahtarını kapatırsanız, özellik listesinden kaldırılmaz.

## <a name="data-entities"></a>Veri varlıkları

**Özellik yönetimi** olarak adlandırılan bir veri varlığı, bir ortamdan Özellik yönetimi özelliklerini içe aktarmanızı sağlar ve sonra başka bir ortama içe aktarabilirsiniz. Bu varlık, yalnızca varolan özellikleri güncelleştirir. Varlıktaki işletme mantığı, **Özellik yönetimi** çalışma alanı üzerinde kullanılan aynı kuralların, içe aktarma tamamlandığında kullanılmasına yardımcı olur. Örneğin, içe aktarma işlemi sırasında tarihi kaldırarak zorunlu özellik ayarını geçersiz kılamazsınız.

Aşağıdaki örnekler, veri içe aktarmak için **Özellik Yönetimi** varlığını kullandığınızda ortaya çıkan durumu tanımlar.

- **Etkinleştirilmiş** alanını, **Evet** olarak değiştirirseniz, özellik açılır ve **Veriyi etkinleştir** alanı geçerli tarihe ayarlanır.
- **Etkin** alanının değerini **Hayır** olarak ayarlarsanız veya **EnableDate** alanını boş bırakırsanız, özellik kapatılır ve **Etkin tarihi** alanı temizlenir. Zorunlu bir özelliği veya açıldıktan sonra kapatılamayan bir özelliği kapatamazsınız.
- **EnableDate** alanının değerini gelecekteki bir tarihle değiştirirseniz, özellik bu tarih için zamanlanır.
- **Etkin** alanının değerini, **Evet** olarak değiştirirseniz ve **EnableDate** alanının değerini gelecekteki bir tarihe değiştirirseniz, özellik bu tarih için zamanlanır. 
- **Etkin** alanının değerini, **Hayır** olarak değiştirirseniz ve **EnableDate** alanının değerini gelecekteki bir tarihe değiştirirseniz, özellik bu tarih için zamanlanır.
- Bir özellik açıksa ve gelecekteki bir tarihe ayarlanmış bir **EnableDate** alanı eklerseniz, özellik açık kalır. Özelliği yeniden zamanlamak için **Etkin** alanını **Hayır** olarak değiştirmeniz gerekir.

## <a name="feature-management-and-flighting"></a>Özellik yönetimi ve denemesi

Özellik yönetimi, her sürümde teslim edilen özellikleri denetlemenize olanak tanır. Deneme sürümü, Microsoft teams'in özellikleri sınırlı sayıda müşteriye sunmasını sağlayarak özelliklerin tüm müşterileri etkilemeden test edilebilmesini ve doğrulanabilmesini sağlar. Özellik yönetimi, herhangi bir özelliğin deneme sürümünü kontrol etmez.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>ISV özelliklerini veya özel özellikleri açmak için Özellik yönetimini kullanma

Özellik yönetimi şu anda bağımsız yazılım satıcılarından (ISV) ve özel özelliklerde bulunan özellikler için kullanılamamaktadır. Ancak Microsoft, özellik yönetimini geliştirmek için daha fazla işlevsellik ekliyor. Bu geliştirmeler tamamlandıktan sonra, Microsoft, Özellik yönetimini tüm özellikler tarafından kullanılabilir hale getirir ve özellikleri kullanmak için bunları güncelleştirmeye ilişkin yönergeleri sağlar.
