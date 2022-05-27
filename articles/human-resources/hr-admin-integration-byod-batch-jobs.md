---
title: BYOD zamanlanmış toplu işlerini iyileştirme
description: Bu konuda, Microsoft Dynamics 365 Human Resources ile kendi veritabanınızı getirin (BYOD) özelliğini kullanırken performansı nasıl iyileştirebileceğiniz açıklanmaktadır.
author: twheeloc
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 2fcdc89ce65fd123b4cf845acf83070119cc3701
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717184"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>BYOD zamanlanmış toplu işlerini iyileştirme


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, kendi veritabanınızı getirin (BYOD) özelliğini kullanırken performansı nasıl iyileştirebileceğiniz açıklanmaktadır. Kendi veritabanınızı getirme hakkında daha fazla bilgi için bkz. [Kendi veritabanınızı getirme (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

## <a name="performance-considerations-for-data-export"></a>Veri dışarı aktarma için performans ile ilgili hususlar

Varlıklar hedef veritabanında yayımlandıktan sonra verileri taşımak için **Veri yönetimi** çalışma alanında Dışarı aktarma işlevini kullanabilirsiniz. Dışa aktarma işlevi, bir veya daha fazla varlık içeren bir Veri taşıma işi tanımlamanızı sağlar. Verileri dışarı aktarma hakkında daha fazla bilgi için bkz. [Verileri içeri ve dışarı aktarma işlerine genel bakış](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

**Dışarı aktarma** sayfasını, verileri farklı hedef veri biçimlerine (ör. virgülle ayrılmış değerler (CSV) dosyası) aktarmak için kullanılabilir. Bu sayfa, bir diğer hedef olarak SQL veritabanlarını da destekler.

Birden fazla varlık içeren bir veri projesi oluşturabilir ve bu veri projesinin çalışmasını zamanlamak için toplu iş kullanabilirsiniz. **Toplu olarak dışa aktar** seçeneğini belirlerseniz veri dışarı aktarma işini belirli aralıklarla çalışacak şekilde zamanlayabilirsiniz.

BYOD dışarı aktarma işleminin genel güvenilirliğinin korunması için dışarı aktarma projesine birden fazla varlık eklerken dikkatli olmanız gerekir. Aynı projeye eklenecek varlık sayısını belirlerken aşağıdaki parametreleri dikkate alın:

- Varlıkların karmaşıklığı
- Her varlık için beklenen veri hacmi
- Dışarı aktarma işleminin iş düzeyinde tamamlanması için gereken toplam süre

En iyi performans için, tek bir projeye yüzlerce varlık eklemekten kaçının. Her biri daha az sayıda varlık içeren birden çok iş oluşturmanızı öneririz.

## <a name="scheduling-byod-batch-jobs"></a>BYOD toplu işlerini zamanlama

Microsoft Dynamics 365 Human Resources kullanıcılarının etkilenmesini en aza indirmek için BYOD toplu işlerini gece veya mesai saatlerinden sonra çalıştırın. Yinelenen toplu işlerin saat dilimini kontrol edin. Bazı toplu işler Pasifik Standart Saati (PST) kullanabilir.

Performans sorunlarını önlemek için BYOD toplu işlerinin zamanlama sıklığını yapılandırırken aşağıdaki etkenleri göz önünde bulundurun:

- Her bir toplu işi tamamlamak için gereken süre
- BYOD'deki verilerle ilgili işletme ihtiyacı

Her toplu işin sıklığını, işin bir sonraki planlanan çalışma zamanından önce eksiksiz biçimde tamamlanmasını sağlayacak bir değere ayarlayın. Human Resources'ın performansını olumsuz etkileyebileceğinden aynı anda birden fazla iş çalıştırmaktan kaçının.

En iyi performans için, BYOD toplu işlerini zamanlarken her zaman **Dışarı Aktar** sayfasındaki **Toplu olarak dışa aktar** seçeneğini kullanın. **Yönet \> Yinelenen veri işlerini yönet**'te yinelenen dışarı aktarma işlemleri zamanlamayın.

## <a name="incremental-export"></a>Artımlı dışarı aktarma

Veri dışarı aktarma için bir varlık eklediğinizde artımlı gönderme (dışa aktarma) veya tam gönderme yapabilirsiniz. Tam göndermede, BYOD veritabanındaki varlığın tüm mevcut kayıtları silinir. Ardından, Human Resources varlığından geçerli kayıt kümesi eklenir.

Artımlı gönderme yapmak için **Varlıklar** sayfasında her varlık için değişiklik izleme özelliğini açmanız gerekir. Daha fazla bilgi için bkz. [Varlıklar için değişiklik izlemeyi etkinleştirme](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Artımlı göndermeyi seçerseniz ilk gönderim her zaman tam gönderme şeklinde yapılır. SQL, bu ilk tam göndermedeki değişiklikleri izler. Yeni bir kayıt eklendiğinde veya bir kayıt güncelleştirildiğinde ya da silindiğinde, değişiklik hedef varlığa yansıtılır.

## <a name="time-outs"></a>Zaman aşımları

BYOD dışarı aktarma işlemleri için varsayılan zaman aşımlarını aşağıda görebilirsiniz:

- Kesme işlemleri için on dakika
- Toplu ekleme işlemleri için bir saat

Hacim yüksek olduğunda bu zaman aşımı ayarları yeterli olmayabilir. Bunları güncelleştirmek için **Veri yönetimi \> Çerçeve parametreleri \> Kendi veritabanınızı getirin**'e gidin. Bu zaman aşımları şirkete özgüdür ve her şirket için ayrı olarak ayarlanmalıdır.

## <a name="known-limitations"></a>Bilinen sınırlamalar

BYOD özelliğinde aşağıdaki sınırlamalar geçerlidir:

- Eşitleme sırasında veritabanınızda etkin kilit olmamalıdır. Etkin kilitler, yazma işleminin yavaş olmasına ve hatta verilerinizin Azure SQL veritabanınıza aktarılamamasına neden olabilir.
- Bileşik varlıkları kendi veritabanınıza aktaramazsınız. Şu anda bileşik varlıklar desteklenmemektedir. Bileşik varlığı oluşturan ayrı ayrı varlıkları dışarı aktarmanız gerekir. Ancak, her iki varlığı da aynı veri projesinde dışarı aktarabilirsiniz.
- Benzersiz anahtarlara sahip olmayan varlıklar, artımlı gönderme kullanılarak dışarı aktarılamaz. Özellikle birkaç hazır varlığın kayıtlarını artımlı olarak dışarı aktarmaya çalıştığınızda bu sınırlamayla karşılaşabilirsiniz. Bu varlıklar, verilerin içeri aktarılmasını sağlamak için tasarlandıklarından benzersiz anahtarları yoktur.

## <a name="troubleshooting"></a>Sorun Giderme

### <a name="incremental-push-doesnt-work-correctly"></a>Artımlı gönderme düzgün çalışmıyor

**Sorun:** Bir varlık için tam gönderim gerçekleştiğinde **seçili** bir deyimi kullanırsanız BYOD'de büyük bir kayıt kümesi görürsünüz. Ancak artımlı gönderim yaptığınızda, BYOD 'de yalnızca birkaç kayıt görürsünüz. Artımlı gönderim tüm kayıtları silmiş ve BYOD'ye yalnızca değiştirilmiş kayıtları eklemiş gibi görünür.

**Çözüm:** SQL değişiklik izleme tabloları beklenen durumda olmayabilir. Bu tür durumlarda, varlığın değişiklik izleme özelliğini kapatıp yeniden açmanız önerilir. Daha fazla bilgi için bkz. [Varlıklar için değişiklik izlemeyi etkinleştirme](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="staging-tables-arent-clearing"></a>Hazırlama tabloları temizlenmiyor

**Sorun:** Proje için hazırlama yaparken hazırlama tabloları doğru şekilde temizlenmiyor. Tablolardaki veriler büyümeye devam ediyor ve performans sorunlarına neden oluyor.

**Çözüm:** Hazırlama tablolarında yedi günlük geçmiş tutulur. **İçe aktarma hazırlamasını temizleme** toplu işi tarafından, hazırlama tablolarındaki yedi günden daha eski geçmiş veriler otomatik olarak temizlenir. Bu iş takılı kalırsa tablolar düzgün bir şekilde temizlenmeyecektir. Bu toplu işi yeniden başlatmak, hazırlama tablolarının otomatik olarak temizlenmesi işini devam ettirir.

## <a name="see-also"></a>Ayrıca bkz.

[Veri yönetimine genel bakış](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Kendi veritabanınızı getirin (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Veri içe ve dışa aktarma işlerine genel bakış](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Varlıklar için değişiklik izlemeyi etkinleştirme](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
