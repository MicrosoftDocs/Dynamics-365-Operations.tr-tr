---
title: Muhasebe dağılımları
description: Bu konuda, muhasebe dağılımları hakkında bilgiler verilmekte ve muhasebe dağılımlarını işlemek için kullanılabilecek seçenekler açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a627ba33065086d21c758a1b8d8f2fa2f6ef02
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448969"
---
# <a name="accounting-distributions"></a>Muhasebe dağılımları

[!include [banner](../includes/banner.md)]

Bu konuda, muhasebe dağılımları hakkında bilgiler verilmekte ve muhasebe dağılımlarını işlemek için kullanılabilecek seçenekler açıklanmaktadır. Muhasebe dağılımları, bir kaynak belgenin parasal tutarlarını belirli genel muhasebe hesaplarına tahsis etmek için kullanılır. 

Muhasebe dağılımları, örneğin satın alma emri, satıcı faturası, gider raporu ve serbest metin faturası gibi her bir kaynak belge tarafından kullanılan ve genişletilen, program genelinde geçerli bir özelliktir. Varsayılan olarak, her bir kaynak belge satırı ve parasal tutar için bir varsayılan muhasebe dağılımı üretilir ve bu dağılım, değişikler için koşullu olarak etkinleştirilir. 

> [!NOTE] 
> Bazı belgeler, siparişlere ve faturalara yönelik masraflar gibi başlık belgesi parasal tutarlarını destekler. 

Genel muhasebe dağılımı özellikleri, muhasebe dağılımlarının işlenmesi için aşağıdaki seçenekleri sağlar:

-   **Tutarları dağıtma** – Vergiler ve masraflar gibi tek bir belge başlığı veya satırı ve tüm alt satırların muhasebe dağılımlarını görüntüleyin ve düzenleyin.
    -   Üst parasal tutar dağıtımları (ana dağıtımlar) için, ana hesap ve mali boyutlar doğrudan ızgaradaki segmentlenmiş giriş kontrolünde düzenlenebilir. Genişletilmiş fiyat, böyle bir ana dağıtımın tipik bir örneğidir.
    -   Dağıtım tutarları, belgenin belirtilen para birimine dayalıdır. Tipik olarak, bu para birimi hareket para birimidir. Muhasebe ve raporlama para birimi tutarları alt defte hesaplarının bir parçası oluşturulur.
    -   Dağıtımlar, hesap tarihini ve hesap olayını gösterir. Tipik olarak, belge nakledilene/günlüğe kaydedilene kadar hesap olayı **ok** olarak ayarlanır. Bu noktada, hesap olayı **Orijinal** durumuna gelir. Dağıtımlar nakledildikten sonra dağıtımları değiştiremezsiniz.
    -   **Bölme** düğmesi ana dağıtımlar için etkinleştirilebilir. **Bölme** yeni muhasebe dağılımları oluşturur ve bölme işlemi yüzdeye, tutara veya miktara dayalı olabilir.
    -   **Eşit olarak dağıt** düğmesi, tutarın tüm dağıtımlar arasında otomatik olarak tahsis edilmesi için **Bölme** düğmesiyle birlikte kullanılabilir.
    -   **Sıfırlama** düğmesi birden fazla dağıtım mevcut olduğundan ana dağıtımlar için etkinleştirilebilir. **Sıfırla** tüm mevcut dağıtımları silerek ve varsayılan dağıtımları yeniden oluşturarak dağıtımda el ile yapılan değişiklikleri sıfırlar.
    -   İskonto, masraf ve satış vergisi gibi herhangi bir alt dağıtım her zaman ana dağıtımı izler. Ana/alt ilişkisini **Referans** &gt; **Ana bilgi** altından görebilirsiniz.
    -   Ana hesap ve mali boyut alt dağıtımlar için de düzenlenebilir.
    -   Muhasebe dağılımları üzerindeki mali boyutlar bir belgenin genişletilebildiği varsayılan düzeni takip eder.
    -   Fark dağıtımları bir satıcı faturası ile bir satın alma emri arasındaki eşleşme vb. gibi eşleşen senaryolarda oluşturulabilir. Muhasebe dağılımı arasındaki eşleşme ilişkilerini **Referans** &gt; **Belge bilgileri** altından görebilirsiniz.
    -   **Doğru** düğmesi, düzeltmeyi destekleyen belgeler için görüntülenir ve etkinleştirilir. **Doğru** yeni dağıtımları oluşturur. İlk olarak, özgün dağıtımları tersine çeviren dağıtımlar oluşturulur. Bu dağıtımlar değiştirilemez. Daha sonra, yeni doğru muhasebe dağılımları oluşturulur. Bu dağıtımlar, orijinal dağıtımların değiştirilmesi durumunda değiştirilebilir.
    -   **Proje bilgileri** düğmesi bir satır bir projeyle ilişkili olduğunda etkinleştirilir. Proje muhasebe dağılımları, finansman kaynağı ve hat özelliği gibi bilgileri değiştirmenize izin verir.
    -   Geçerli belge muhasebe durumunu **Referans** içerisinde görebilirsiniz. Durum tüm belge içindir ve belgenin işlemde mi yoksa tamamlanmış mı olduğunu belirtir.
-   **Dağılımları göster**: Belgedeki tüm satırlar ve parasal tutarlar için muhasebe dağılımlarını görüntüleyin. Muhasebe dağılımlarını bu görünümden değiştiremezsiniz.

Sürüm 10.0.13, yeni alanların doğru ayarlandığından emin olmak için hesap dağıtım tablosunu doğrulayan bir özellik eklenmiştir. Bu özellik, **Kaynak belge muhasebe çerçevesini kullanan belgeler için verilerin ek doğrulanmasını etkinleştir** olarak adlandırılır. Özelliği kullanmak için **Özellik yönetimi** çalışma alanını kullanarak etkinleştirmelisiniz. Özelliği etkinleştirmek için **Özellik yönetimi** sayfasındaki **Arama** alanında özelliğin adını arayın ve **Şimdi etkinleştir**'i seçin.

Daha fazla bilgi için bkz. [Satıcı faturaları için muhasebe dağılımları ve muavin defteri günlük girdileri](accounting-distributions-subledger-journal-entries-vendor-invoices.md).
