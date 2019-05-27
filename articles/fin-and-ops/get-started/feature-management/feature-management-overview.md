---
title: Özellik yönetimine genel bakış
description: Bu konu Özellik Yönetimi özelliğini ve nasıl kullanabileceğinizi açıklar.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
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
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538715"
---
# <a name="feature-management-overview"></a>Özellik yönetimine genel bakış

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Özellikler, Microsoft Dynamics 365 for Finance and Operations'ın her sürümünde eklenir ve güncelleştirilir. Özellik yönetimi deneyimi, her sürümde teslim edilen özelliklerin listesini görüntüleyebileceğiniz bir çalışma alanı sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz.

## <a name="the-feature-management-workspace"></a>Özellik yönetimi çalışma alanı

Panoda uygun kutucuğu seçerek **Özellik yönetimi** çalışma alanını açabilirsiniz. Özellik yönetimi deneyimi tarafından desteklenen tüm sürümlere ait özelliklerin listesini gösteren bir sayfa görürsünüz. Zamanla Microsoft Özellik yönetimi deneyimini, özellikleri yönetmenize yardımcı olacak ek işlevler içerecek şekilde geliştirecektir.

Özellik listesi sekmesi aşağıdaki bilgileri içerir:

- **Özellik adı** – Eklenen özelliğin açıklaması.
- **Etkin durum** – Bir sembol, bir özelliğin etkinleştirildiğini (onay işareti), etkinleştirilmediğini (boş), etkinleştirilmek üzere zamanlandığını (saat) veya zorunlu olarak etkinleştirildiğini (kilit) gösterir. Burada gösterilen ayar tüm tüzel kişilikler için kullanılır. Bir özellik açılsa bile hala güvenlik tarafından denetlendiğini unutmayın. Bu nedenle özellik güvenlik rolüne göre yalnızca erişimi olan kullanıcılar tarafından kullanılabilir. Ayrıca, yalnızca kullanıcının erişebileceği tüzel kişilikler için de kullanılabilir.
- **Etkinleştirme tarihi** – Özelliğin etkinleştirildiği veya tarih gelecekteki bir tarih ise özelliğin etkinleştirileceği tarih.
- **Özellik eklendi** – Özelliğin ortamınıza eklendiği tarih. Bu tarih, aylık sürüm döngüleri sırasında ortamınızı güncelleştirdiğinizde otomatik olarak girilir.
- **Modül** – Yeni özellikten etkilenen modül.

Bir özellik seçtiğinizde, ayrıntılar bölmesinde özellik listesinin sağında ek bilgiler görüntülenir. Bölmenin en üstünde özellik adı, özelliğin eklendiği tarih, özelliğin etkilediği modül ve **Daha fazla bilgi edinin** bağlantısını görürsünüz. Özelliğin belgelerini görüntülemek için bu bağlantıyı seçin. Belge yoksa, geçici bir sayfaya yönlendirilirsiniz. Ayrıntılar bölmesi ayrıca özellik hakkında kendi açıklamalarınızı ekleyebileceğiniz bir **Açıklama** alanı da içerir.

**Özellik yönetimi** çalışma alanı aynı zamanda içindeki özelliklerin listesi bulunan çeşitli sekmeler içerir. 
- **Yeni** - Son aylık güncelleştirmeden sonra eklenen tüm özellikleri gösterir. Aylık güncelleştirmeleri atladıysanız, son güncelleştirmenizden bu yana yeni özelliklerin tümünü içerecektir. En yeni özellikler listenin en üstünde yer alır. Ayrıca, yeni özelliklerin toplam sayısı sayfanın üst kısmındaki bir kutucukta gösterilir.
- **Etkin değil** - Etkinleştirilmemiş tüm özellikleri gösterir. En yeni özellikler listenin en üstünde yer alır. Ayrıca, yeni özelliklerin toplam sayısı sayfanın üst kısmındaki bir kutucukta gösterilir.
- **Planlanan** - Gelecekteki bir tarihte etkinleştirilmek üzere zamanlanmış tüm özellikleri gösterir. En erken zamanlanan tarihe sahip özellikler listenin en üstünde görüntülenir. Ayrıca, yeni özelliklerin toplam sayısı sayfanın üst kısmındaki bir kutucukta gösterilir.
- **Tümü** - Tüm özellikleri gösterir. En yeni özellikler listenin en üstünde yer alır.


## <a name="enable-a-feature"></a>Bir özelliği etkinleştirme

Bir özellik etkinleştirilmemişse, ayrıntılar bölmesinde **Etkinleştir** düğmesi görüntülenir. Bu özelliği etkinleştirmek için bu düğmeyi kullanabilirsiniz.

1. Etkinleştirmek istediğiniz özelliği seçin ve sonra ayrıntılar bölmesinde **Etkinleştir**'i seçin.
2. Özelliğin etkinleştirilmesi gereken tarihi belirtebileceğiniz bir kaydırıcı görünür. Varsayılan olarak bu tarih Geçerli tarih olarak ayarlanır.
3. Özelliği etkinleştirmek için **Etkinleştir**'i seçin.

Bazı özellikler etkinleştirildikten sonra devre dışı bırakılamaz. Etkinleştirmeye çalıştığınız özellik devre dışı bırakılamıyorsa bir uyarı alırsınız. Bu aşamada, işlemi iptal etmek ve özelliği devre dışı bırakmak için **İptal**'i seçebilirsiniz. Ancak, **Etkinleştir**'i seçip özelliği etkinleştirirseniz daha sonra devre dışı bırakamazsınız.

Özellik etkinleştirildikten sonra, ayrıntılar bölmesindeki **Daha fazla bilgi edinin** bağlantısının altında bir ileti görüntülenir. Bu ileti, özelliğin etkinleştirildiğini ya da özelliğin ileride ne zaman etkinleştirileceğini belirtir. Gelecekteki bir tarih kullanırsanız, özellik **Planlanan** listesinde görüntülenecektir. Bu ileti, özellik listesinde özelliği her seçtiğinizde görüntülenir. Gelecekte zamanlanmış özellikler, sistem tarihi tarafından temsil edilen saat dilimine bağlı olarak bir toplu işlem tarafından gece yarısında etkinleştirilir. 

## <a name="reschedule-a-feature"></a>Bir özelliği yeniden zamanlama

Bir özellik gelecek için etkinleştirilmişse, ayrıntılar bölmesinde **Yeniden zamanla** düğmesi görüntülenir. **Etkinleştirme tarihini** başka bir tarihe değiştirmek için bu düğmeyi kullanabilirsiniz.

1. Yeniden zamanlamak istediğiniz zamanlanmış özelliği seçin ve sonra ayrıntılar bölmesinde **Yeniden zamanla**'yı seçin.
2. Özelliğin etkinleştirilmesi gereken tarihi belirtebileceğiniz bir kaydırıcı görünür. 
3. Özelliği yeniden zamanlamak için **Etkinleştir**'i veya zamanlamayı iptal etmek için **Devre dışı bırak**'ı seçin.

## <a name="disable-a-feature"></a>Bir özelliği devre dışı bırakma

Bir özellik etkinleştirilmişse, ayrıntılar bölmesinde **Devre dışı bırak** düğmesi görüntülenir. Bu özelliği devre dışı bırakmak için bu düğmeyi kullanabilirsiniz. Özellik etkinleştirildikten sonra devre dışı bırakılamıyorsa **Devre dışı bırak** düğmesi kullanılamaz.

- Devre dışı bırakmak istediğiniz özelliği seçin ve sonra ayrıntılar bölmesinde **Devre dışı bırak**'ı seçin.

- Özellik devre dışı bırakılır ve tarih temizlenir.

Özellik devre dışı bırakıldıktan sonra, ayrıntılar bölmesindeki **Daha fazla bilgi edinin** bağlantısının altında bir ileti görüntülenir. Bu ileti, özelliğin henüz etkinleştirilmediğini ve **Etkinleştirilmedi**listesinde görüneceğini bildirir. İleti, özellik listesinde özelliği her seçtiğinizde görüntülenir.

## <a name="features-that-must-be-enabled"></a>Etkinleştirilmesi gereken özellikler

Güncelleştirme yaptığınızda otomatik olarak etkinleştirilmesi gereken kritik bir özellik sunulabilir. Bu özellik **Etkinleştirme tarihinde** otomatik olarak etkinleştirilir. Ayrıntılar bölmesindeki **Daha fazla bilgi edinin** bağlantısının altında bir ileti görüntülenecektir. Bu ileti, özelliğin etkin olduğunu veya **Etkinleştirme tarihinde** otomatik olarak etkinleştirileceğini belirtir. İleti, özellik listesinde özelliği her seçtiğinizde görüntülenir.

## <a name="assigning-roles"></a>Rolleri atama

**Özellik Yönetimi** çalışma alanı, sistem yöneticileri tarafından ve Özellik yönetimi deneyimini desteklemek üzere oluşturulan Özellik Yöneticisi veya Özellik görüntüleyicisi rollerine atanan kullanıcılar tarafından açılabilir. Özellik yöneticisi rolündeki kullanıcılar, herhangi bir özelliği açabilir veya kapatabilir. Ayrıca bu özellik için açıklamalar bölümünü de güncelleştirebilir. Özellik görüntüleyicisi rolündeki kullanıcılar yalnızca **Özellik yönetimi** çalışma alanını görüntüleyebilir. Özellikleri açıp kapatamazlar.

Özellik yöneticisi rolü ve Özellik görüntüleyicisi rolü, bir kullanıcının sahip olduğu güvenliği geçersiz kılmaz. Roller yalnızca etkinleştirme özelliklerine erişimi denetler. Özelliklerin kendisine erişim sağlamaz.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>ISV özelliklerini veya özel özellikleri etkinleştirmek için Özellik yönetimini kullanma

Özellik yönetimi işlemi şu anda ISV özellikleri veya özel özellikler için kullanılamaz. Özellik yönetimini geliştirmek için ek işlevler ekleyeceğiz ve bu geliştirmeler tamamlandığında Özellik yönetiminin tüm özelliklere açacak ve özelliğin nasıl güncelleştirileceği konusunda size özel yönergeler sağlayacağız.

## <a name="feature-management-and-flighting"></a>Özellik yönetimi ve denemesi

Özellik yönetimi, her sürümde teslim edilen özellikleri denetlemenize olanak tanır. Deneme sürümü, Microsoft ekiplerin özellikleri sınırlı sayıda müşteriye sunmasını sağlayarak özelliklerin tüm müşterileri etkilemeden test edilebilmesini ve doğrulanabilmesini sağlar. Özellik yönetimi, herhangi bir özelliğin deneme sürümünü kontrol etmez.
