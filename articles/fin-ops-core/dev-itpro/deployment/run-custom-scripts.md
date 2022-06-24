---
title: Özel X++ komut dosyalarını sıfır kapalı kalma süresiyle çalıştırma
description: Bu makalede, sisteminizi askıya almak zorunda kalmadan özel X++ komut dosyaları içeren dağıtılabilir paketlerin nasıl yüklenip çalıştırılacağı açıklanmaktadır.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ff01e2ff8ec105603bb91e0b555301f36e8985b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867343"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Özel X++ komut dosyalarını sıfır kapalı kalma süresiyle çalıştırma

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Bu özellik, Microsoft Dynamics Lifecycle Services'dan (LCS) geçmenize veya sisteminizi askıya almanıza gerek kalmadan özel X++ komut dosyaları içeren dağıtılabilir paketleri yüklemenize ve çalıştırmanıza olanak tanır. Bu nedenle, herhangi bir kesintiye neden olmadan küçük veri tutarsızlıklarını düzeltebilirsiniz.

Küçük veri tutarsızlıklarını düzeltmek için X++ komut dosyası kullanmanın yararı, sistemin komut dosyasını çalıştırdığında ilgili tüm tabloları gerektiği gibi otomatik olarak ayarlamasıdır. Bu yaklaşım, düzeltmenin bütünlüğünü sağlamaya yardımcı olur ve yeni tutarsızlıklar getirme riskini en aza indirmeye yardımcı olur.

> [!IMPORTANT]
> Bu özellik yalnızca küçük veri tutarsızlıklarının düzeltilmesi için tasarlanmıştır. Aşağıdaki amaçlar veya başka bir amaç için kullanılmamalıdır:
>
> - Veri toplama
> - Şema değişiklikleri
> - Veri taşıma veya diğer uzun süre çalışan işlemler
> - Normal iş süreçleri, veri tutarlılığı araçları veya diğer self servis araçlar gibi diğer yollarla düzeltilebilen verilerin düzeltilmesi
>
> Bu özellik, yetkili kullanıcıların varlıkları ve kayıtlarını, bu varlıklarla ilişkili iş mantığını çalıştırmak zorunda kalmadan doğrudan değiştirmelerini sağlar. Bu değişiklikler veri bütünlüğü sorunlarına neden olabilir. Bu nedenle, kuruluşunuz bir komut dosyasını çalıştırmadan önce ve/veya çalıştırdıktan sonra iç ve dış denetçilerden (veya diğer eşdeğer paydaşlardan) onay ve imza almanızı gerektirebilir. Uyumluluk nedenleriyle, bazı özellikleri etkileyen değişikliklerin dış raporlarda (mali tablolar gibi) açıklanması veya resmi yetkililere bildirilmesi de gerekebilir. Kuruluşunuz, bu özellik aracılığıyla verilerinde yapılan değişikliklerden, bu değişikliklerin onaylanmasından ve imzalanmasından veya açıklanmasından ve yürürlükteki yasalara uyulmasından tek başına sorumludur. Bu özelliği kullanmanın tüm risklerini taşıyorsunuz.

Sisteme yüklenen tüm dağıtılabilir paketler zorunlu bir iş akışından geçer. Güvenlik önlemi olarak ve görevlerin ayrılmasını sağlamaya yardımcı olmak için, dağıtılabilir bir paketi yükleyen kullanıcının iş akışındaki sonraki adımlar için onaylamasına izin verilmez. Başka bir kullanıcı onaylamalıdır. Ancak, paket onaylandıktan sonra, yükleyen kullanıcının kalan adımları tamamlamasına izin verilir.

Sistem, tüm dağıtılabilir paketlerin bir test çalıştırmasına tabi yapılmasını gerektirir. Komut dosyasının üretim verileri üzerinde çalışmasına izin verilmeden önce, kullanıcı **Test günlüğünü kabul et**'i seçerek çıktının doğru olduğunu doğrulamalıdır. Çıktı doğru değilse kullanıcı **Bırak**'ı seçerek paketi başarısız olarak işaretlemelidir. Bu durumda, komut dosyasının üretim verileri üzerinde çalışmasına izin verilmez.

Yüklenen her paket sisteme kaydedilir ve tanımlanmış bir olay iş akışından geçer. Her olay için sistem, bir zaman damgası ve olayı gerçekleştiren kişinin kimliğini içeren bir günlük tutar. Bu şekilde, sistem bir denetim izi olmasını sağlar.

Aşağıdaki çizimde gösterildiği gibi, sistem her dağıtılabilir paketin X++ içinde nasıl çalıştırılabildiği ve hangi varlıklarla temas edildiği hakkında ayrıntılı bilgi sağlar.

![Komut dosyası ayrıntıları sayfası.](media/script-details.png "Komut dosyası ayrıntıları sayfası")

## <a name="assign-duties-to-users-to-control-access"></a>Erişimi denetlemek için kullanıcılara görev atama

Bu özellik aşağıdaki görevleri sağlar. Yöneticiler bu görevleri, özelliğe erişimi denetlemeye yardımcı olmak için kullanabilir.

- **Özel komut dosyalarını koru** – Bu görev, ortamlarda (\[UAT\] ve üretim kullanıcı kabul testi) özel X++ komut dosyalarını yükleme, test etme, doğrulama ve çalıştırma olanağı sağlar.
- **Özel komut dosyalarını onayla** – Bu görev, yüklenen özel X++ komut dosyasını onaylama olanağı verir. Onay, herhangi bir komut dosyasının test edilebilmesi, doğrulanabilmesi ve çalıştırılabilmesi için zorunlu bir adımdır.

Kötü amaçlı eylem riskini en aza indirmeye yardımcı olmak için, her komut dosyasının yükleyen kullanıcı dışındaki bir kullanıcı tarafından açıkça onaylanması gerekir. Bu özelliği kuruluşunuzda kullanabilmeniz için, bir yöneticinin önceki görevleri en az iki ilgili ve son derece güvenilir kullanıcıya ataması gerekir. Tek bir kullanıcının her iki görevi de olsa, bu kullanıcı yine de kendi komut dosyalarını onaylayamaz.

## <a name="create-a-deployable-package"></a>Dağıtılabilir paket oluşturma

Bu özellik, Visual Studio'da oluşturulabilen düzenli bir dağıtılabilir paket gerektirir. Talimatlar için bkz. [Modellerin dağıtılabilir paketlerini oluşturma](../deployment/create-apply-deployable-package.md).

Dağıtılabilir paketiniz tam olarak bir çalıştırılabilir X++ sınıfı içermelidir. Başka bir deyişle, aşağıdaki imzaya sahip bir yöntem içeren bir sınıfa sahip olmalıdır.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Ana yöntemin adı küçük harfli olmalıdır.

## <a name="code-example"></a>Kod örneği

Aşağıdaki kod örneği, dağıtılabilir bir paketin nasıl yapılandırılabileceğini gösterir.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Önerilen yöntemler

Aşağıdaki listede, komut dosyasını başarıyla yazmak, uygulamak ve çalıştırmak için bazı en iyi yöntemler açıklanmaktadır. Listede her duruma yer verilmemiştir ve yalnızca rehberlik olarak kabul edilmelidir.

- Komut dosyasının sonuna bir başarılı iletisi **yazın**. Bu şekilde, komut dosyasının özel durumlar olmadan çalıştırdığını görebileceksiniz.
- Hareket kapsamının açık işlemesini **ekleyin**.
- `update()` yöntemleri gibi varolan iş mantığını **kullanın** ancak `doUpdate()`, `doInsert()`ve `doDelete()` yöntemlerini kullanarak iş mantığını **atlamayın**. Bu yaklaşım, bağımlı verilerin doğru şekilde işlenmesini sağlamaya yardımcı olur. Ayrıca, daha fazla veri tutarsızlığı riskini önemli ölçüde azaltacaktır.
- Şirket bağlamını **onaylayın**. Bu yaklaşım, bir komut dosyası çalışırken sık karşılaşılan hataları ortaya çıkarır. Örneğin, komut dosyasının yanlış şirkette çalıştırılıp çalıştırılmadığını ortaya çıkarır.
- Etkilenen kayıt sayısının beklentilerinizle eşleştiğinden **emin olun**. Bu yaklaşım, komut dosyası hazırlanırken verilerin sistemde beklenmedik şekilde kaydırılıp kaydırılmadığını ortaya koymaktadır.
- Her komut dosyası için benzersiz sınıf adları **kullanın** (örneğin, ada bir iş öğesine başvuru dahil ederek). Bu yaklaşım, komut dosyasını yüklediğinizde ad çakışması sorunlarını önler. Bir komut dosyasının yeni bir yinelemesi gerekiyorsa ona yeni bir ad verdiğinizden emin olun.
- Her komut dosyasını önce üretim dışı bir ortamda **test edin**. Amaçlanan etkiyi ve ilgili veriler üzerinde amaçlanan yan etkilere yönelik test yapın. Etkilenebilecek tüm iş süreçlerinin daha sonra başarıyla ve tam olarak tamamlanabildiğinden emin olun.

## <a name="upload-and-run-a-deployable-package"></a>Dağıtılabilir paketi yükleme ve çalıştırma

Komut dosyasını yüklemek ve çalıştırmak için aşağıdaki yordamı kullanın.

1. Finans ve Operasyon uygulamanızda, **Sistem yönetimi \> Periyodik görevler \> Veritabanı \> Özel komut dosyaları**'na gidin.
1. **Yükle**'yi seçin.
1. Bu makalede daha önce açıklandığı gibi oluşturduğunuz dağıtılabilir paketi seçin. Komut dosyasının amacını belirtmeniz istenecektir.
1. Komut dosyası artık dosyayı yükleyen kullanıcı dışında bir kullanıcı tarafından onaylanmalıdır. Onaylayan kullanıcı aşağıdaki adımları izlemelidir:

    1. **Sistem yönetimi \> Periyodik \> Veri tabanı \> Özel komut dosyaları**'na gidin.
    1. Onaylanacak komut dosyasını seçin ve sonra **Ayrıntılar**'ı seçin.
    1. Eylem Bölmesinde, **İşlem iş akışı** sekmesinde **Başlat** grubunda **Onayla** veya **Reddet**'i seçin. **Onayla**'yı seçerseniz komut dosyası onaylandı olarak işaretlenir ve test için kilidi açılır. **Reddet**'i seçerseniz komut dosyası kilitlenir. Her iki durumda da, olay günlüğe kaydedilir ve komut dosyasının bir kopyası sistemde tutulur.

1. Komut dosyası, amacına uygun olduğundan emin olmak için test edilmelidir. Test eden kullanıcı, yükleyici veya onaylayan kullanıcı veya gerekli izinlere sahip üçüncü bir kullanıcı olabilir. Test eden kullanıcı aşağıdaki adımları izlemelidir:

    1. **Sistem yönetimi \> Periyodik \> Veri tabanı \> Özel komut dosyaları**'na gidin.
    1. Test edilecek komut dosyasını seçin ve sonra **Ayrıntılar**'ı seçin.
    1. Eylem Bölmesinde, **İşlem iş akışı** sekmesinde **Test** grubunda **Testi çalıştır**'ı seçin. Komut dosyası, sistemin çeşitli günlükleri ve SQL deyimlerini toplarken otomatik olarak iptal edeceği geçici bir işlem içinde çalıştırılır.
    1. Komut dosyası çalıştırmayı tamamladığında, günlükleri gözden geçirin ve sonuçların beklentilerinizi karşıladığını doğrulayın. Şu adımlardan birini izleyin:

        - Test sonucundan memnunsanız komut dosyasının çalıştırılmasına izin vermek için Eylem Bölmesi'nin **İşlem iş akışı** sekmesindeki **Test** grubunda **Test günlüğünü kabul et**'i seçin. Olay günlüğü, komut dosyasının test edildiğini, kimin ve ne zaman test ettiğini gösterir.
        - Test sonucundan memnun değilseniz komut dosyasının çalıştırılmasını önlemek için Eylem Bölmesi'nin **İşlem iş akışı** sekmesindeki **Sonlandır** grubunda **Bırak**'ı seçin. Sistem, komut dosyasının bir kopyasını geçmişinin bir günlüğüyle birlikte saklayacaktır.

1. Komut dosyasının beklentilerinizi karşıladığından emin olduğunuzda, çalıştırmak için Eylem Bölmesi'nin **İşlem iş akışı** sekmesindeki **Çalıştır** grubunda **Çalıştır**'ı seçin. Bu komut önceki test çalıştırması ile aynı işlemi yapar ancak işlem sonunda tamamlanır.
1. Komut dosyası çalışmayı tamamladıktan sonra sonucu kontrol edin ve komut dosyasının istediğiniz gibi çalıştığını onaylayın. Şu adımlardan birini izleyin:

    - Sonuçtan memnunsanız Eylem Bölmesi'nin **İşlem iş akışı** sekmesindeki **Sonlandır** grubunda **Amaç çözümlendi**'yi seçin. Olay günlüğü, komut dosyasının başarıyla çalıştırıldığını ve komut dosyasının kim tarafından ne zaman doğrulandığını gösterir. Komut dosyası kaydedilir ancak kilitlidir ve yeniden çalıştırılabilir.
    - Sonuçtan memnun değilseniz Eylem Bölmesi'nin **İşlem iş akışı** sekmesindeki **Sonlandır** grubunda **Amaç çözümlenmedi**'yi seçin. Olay günlüğü, komut dosyasının amaçlanan amacını yerine getiremediği gerçeğini yansıtır ve komut dosyasını kimin ne zaman çalıştırdığını gösterir. Komut dosyası kaydedilir ancak kilitlidir ve yeniden çalıştırılabilir. Ancak, sistem komut dosyası eylemini otomatik olarak geri almaz. Başarısız komut dosyasının sisteminizdeki etkisini geri almak için yeni bir komut dosyası yazmanız, içeri aktarmanız ve çalıştırmanız gerekebilir.

Son adımdaki seçiminiz komut dosyasının son durumunu tanımlar. Süreci ihtiyaç duyduğunuz kadar tekrarlayabilirsiniz.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>LCS aracılığıyla dağıtılabilir bir paket yükleme ve çalıştırma

Dağıtılabilir paketinizi önceki bölümde açıklandığı gibi Finans ve Operasyon uygulamanız için kullanıcı arabirimi üzerinden dağıtmak yerine, LCS'ye yükleyebilir ve dağıtmak için normal yordamı kullanabilirsiniz. Daha fazla bilgi için bkz. [Dağıtılabilir paketleri komut satırından yükleme](../deployment/install-deployable-package.md).

Bu yaklaşım daha az kısıtlamaya sahip olsa da, daha az hata koruması sağlar. Ayrıca, tüm sunucuların yeniden başlatılması gerektiğinden, bazı kapalı kalma sürelerine neden olur.
