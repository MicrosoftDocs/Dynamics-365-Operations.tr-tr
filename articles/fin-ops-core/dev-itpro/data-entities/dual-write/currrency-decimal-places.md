---
title: Çift yazma için para birimi veri türü geçişi
description: Bu konu, çift yazmanın para birimi için desteklediği ondalık basamak sayısının nasıl değiştirileceğini açıklamaktadır.
author: RamaKrishnamoorthy
ms.date: 12/08/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: e9dc3e6c5fbec9636370b64a9bbdcf8a5834d332
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061848"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Çift yazma için para birimi veri türü geçişi

[!include [banner](../../includes/banner.md)]



Para birimi değerleri için desteklenen ondalık basamak sayısını en fazla 10'a artırabilirsiniz. Varsayılan sınır dört ondalık haneye sahiptir. Ondalık basamakların sayısını artırarak, verileri eşitlemek için çift yazma kullandığınızda veri kaybını engelleyebilirsiniz. Ondalık basamak sayısında artış kabul edilerek yapılan bir değişikliktir. Bunu uygulamak için, Microsoft'tan yardım istemeniz gerekir.

Ondalık basamak sayısının değiştirilmesi işleminde iki adım vardır:

1. Microsoft'tan geçiş talep edin.
2. Dataverse'ta ondalık basamak sayısını değiştirin.

Finans ve Operasyon uygulaması ve Dataverse'ün para birimi değerlerinde aynı sayıda ondalık basamak desteklemesi gerekir. Aksi takdirde, bu bilgiler uygulamalar arasında eşitlendiğinde veri kaybı ortaya çıkabilir. Geçiş işlemi para birimi ve döviz kuru değerlerinin depolanma biçimini yeniden yapılandırır, ancak hiçbir veriyi değiştirmez. Geçiş tamamlandıktan sonra, para birimi kodları ve fiyatlandırma için ondalık basamak sayısı artırılabilir ve kullanıcıların girdiği ve görüntülediği verilerde daha fazla ondalık duyarlığı olabilir.

Geçiş isteğe bağlıdır. Daha fazla ondalık basamak desteğinden avantaj sağlayabilecekseniz, geçiş yapmayı düşünmeniz önerilir. Dörtten fazla ondalık basamak içeren değerlerin gerekli olmadığı kuruluşların geçiş yapması gerekmez.

## <a name="requesting-migration-from-microsoft"></a>Microsoft'tan geçiş talep etme

Dataverse'teki mevcut para birimi sütunları için depolama, dörtten fazla ondalık basamak destekleyemez. Bu nedenle, geçiş işlemi sırasında, para birimi değerleri veritabanındaki yeni dahili sütunlara kopyalanır. Bu işlem, tüm veriler geçirilene kadar sürekli olarak gerçekleşir. Dahili olarak, geçişin sonunda yeni depolama türleri eski depolama türlerinin yerini alır, ancak veri değerleri değiştirilmez. Böylece para birimi sütunları en fazla 10 ondalık basamağı destekleyebilir. Geçiş işlemi sırasında Dataverse kesinti olmadan kullanılabilir.

Aynı zamanda, döviz kurları, geçerli 10 limiti yerine 12'ye kadar ondalık basamağı destekleyecek şekilde değiştirilir. Bu değişiklik, ondalık basamak sayısının hem Finans ve Operasyon uygulaması hem de Dataverse'te aynı olmasını sağlamak için gereklidir.

Geçiş hiçbir veriyi değiştirmez. Para birimi ve döviz kuru sütunları dönüştürüldükten sonra, yöneticiler her hareket para birimi ve fiyatlandırma için ondalık basamak sayısını belirterek sistemi, para birimi sütunları için en çok 10 ondalık basamak kullanacak şekilde yapılandırabilir.

### <a name="request-a-migration"></a>Geçiş talep etme

Bu özelliği kullanılabilir hale getirmek için, **CDSExpandDecimal@microsoft.com** adresine aşağıdaki bilgileri ekleyerek e-posta gönderin:

+ **Konu:** \<organizationID\> için genişletilmiş ondalık desteği etkinleştirme isteği
+ **Gövde:** \<organizationID\> kuruluşum için genişletilmiş ondalık desteğini etkinleştirmek istiyorum.

Bir Microsoft temsilcisi, sonraki adımlar için iki ile üç iş günü içinde sizinle iletişim kuracaktır.

Bir geçiş istediğinizde, aşağıdaki ayrıntılara sahip olmanız ve bunları uygun şekilde planlamanız gerekir:

+ Verileri geçirmek için gereken süre sistemdeki veri miktarına bağlıdır. Büyük veritabanlarının geçiş işlemi birkaç gün sürebilir.
+ Veritabanı boyutu, geçiş işlemi çalışırken geçici olarak artar, çünkü dizinler için ek alan gereklidir. Geçiş tamamlandığında, ek alanın büyük bir çoğunluğu serbest kalır.
+ Geçiş işlemi sırasında, geçişin tamamlanmasını engelleyen hatalar oluşursa, sistem Microsoft Desteği'ne uyarıları gönderir ve Destek personeli müdahale edebilir. Ancak, geçiş sırasında hatalar oluşsa bile, Dataverse olağan kullanım için tamamen kullanılabilir durumda kalır.
+ Geçiş işlemi geri alınamaz.

## <a name="changing-the-number-of-decimal-places"></a>Ondalık basamak sayısının değiştirilmesi

Geçiş tamamlandıktan sonra, Dataverse daha fazla ondalık basamak içeren sayıları depolayabilir. Yöneticiler, belirli para birimi kodları ve fiyatlandırma için kaç ondalık basamak kullanılacağını seçebilirler. Microsoft Power Apps, Power BI, ve Power Automate kullanıcıları daha sonra daha fazla ondalık basamak içeren sayıları görüntüleyebilir ve kullanabilir.

Bu değişikliği yapmak için Power Apps'te aşağıdaki ayarları güncelleştirmeniz gerekir:

+ **Sistem Ayarları: Fiyatlandırma için para birimi duyarlığı** - **Sistem genelinde fiyatlandırma için kullanılan para birimi duyarlığını ayarla** sütunu **Fiyatlandırma Duyarlılığı** seçildiğinde, para biriminin kuruluş için nasıl davranacağını tanımlar.
+ **İş Yönetimi: Para birimleri** - **Para Birimi Duyarlığı** sütunu, belirli bir para birimi için özel bir ondalık basamak sayısı belirlemenizi sağlar. Kuruluş genelinde ayara geri dönüş vardır.

Bazı kısıtlamalar bulunur:

+ Bir tablo üzerinde para birimi sütununu yapılandıramazsınız.
+ Yalnızca **Fiyatlandırma** ve **Hareket Para Birimi** düzeylerinde dörtten fazla ondalık basamak belirtebilirsiniz.

### <a name="system-settings-currency-precision-for-pricing"></a>Sistem Ayarları: Fiyatlandırma için para birimi duyarlığı

Geçiş tamamlandıktan sonra, yöneticiler para birimi duyarlığını ayarlayabilir. **Ayarlar \> Yönetim**'e gidin ve **Sistem Ayarları**'nı seçin. Daha sonra, **Genel** sekmesinde, **Tüm sistemde fiyatlandırma için kullanılan para birimi duyarlığını ayarlayın** sütunundaki değeri aşağıda gösterildiği şekilde değiştirin.

![Para birimi için sistem ayarları.](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>İş Yönetimi: Para Birimleri

Belirli bir para birimi için para birimi duyarlığının fiyatlandırma için kullanılan para birimi duyarlığından farklı olmasını istiyorsanız, bunu değiştirebilirsiniz. **Ayarlar \> İş Yönetimi**'ne gidin **Para birimleri**'ni ve ardından değiştirilecek para birimini seçin. Sonra, aşağıdaki çizimde gösterildiği gibi, **Para Birimi Duyarlığı** sütununu istediğiniz ondalık basamak sayısına ayarlayın.

![Belirli bir yerel ayar için para birimi ayarları.](media/specific-currency.png)

### <a name="tables-currency-column"></a>Tablolar: Para birimi sütunu

Belirli para birimi sütunları için yapılandırılabilecek ondalık basamak sayısı dört ile sınırlıdır.

### <a name="default-currency-decimal-precision"></a>Varsayılan para birimi ondalık duyarlığı
Geçiş senaryolarında ve geçiş dışı senaryolarda varsayılan para birimi ondalık duyarlığının beklenen davranışı için aşağıdaki tabloya bakın. 

| Oluşturulma tarihi  | Para birimi ondalık alanı    | Mevcut kuruluş (Para birimi alanının geçişi yapılmadı) | Mevcut kuruluş (Para birimi alanının geçişi yapıldı) | Derleme 9.2.21062.00134 sonrası oluşturulan yeni kuruluş |
|---------------------------------------------------------|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|------------------------------------------------|
| Derleme 9.2.21111.00146 öncesi oluşturulan para birimi alanı  |     |  |       |
|    | Kullanıcı arabiriminde görünen maksimum duyarlık   | 4 basamak    | 10 basamak    | Yok    |
| | Veritabanı ve DB sorgu sonuçları kullanıcı arabiriminde görünen maksimum duyarlık         | 4 basamak   | 10 basamak   | Yok    |
| Derleme 9.2.21111.00146 sonrası oluşturulan para birimi alanı |    |  |     |   |
|   | Kullanıcı arabiriminde görünen maksimum ondalık duyarlığı     | 4 basamak   | 10 basamak   | 10 basamak     |
|          | Veritabanı ve DB sorgu sonuçları kullanıcı arabiriminde görünen maksimum ondalık duyarlığı | 10 basamak. Ancak yalnızca 4 tanesi önemli olup 4 ondalık basamak dışındaki tüm basamaklar sıfırdır. Bu, gerekirse kuruluşun daha basit ve hızlı şekilde geçirilmesini sağlar. | 10 basamak      | 10 basamak     |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
