---
title: Dynamics 365 for Talent ile Dynamics 365 for Finance and Operations tümleştirmesi SSS
description: Bu konu içinde bir tümleştirme ve Talent ve Finance and Operations işlemlerini hangi verilerin eşitleneceğini açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 438c2b5689e450b9aae9c55168993f2ee84be4d5
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/12/2019
ms.locfileid: "950095"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>Dynamics 365 for Talent ile Dynamics 365 for Finance and Operations tümleştirmesi SSS

[!include [banner](includes/banner.md)]

Bu konu, hangi verilerin Dynamics 365 for Talent, Dynamics 365 for Finance and Operations ile tümleştirildiğinde eşitleneceğine dair sıkça sorulan soruları yanıtlar.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Tüm veriler mi eşitlenir yoksa yalnızca bazı veri varlıkları mı?

Core İnsan Kaynakları (HR) ile, verinin bir alt kümesi eşitlenir. Tüm varlıkların listesi için bkz. [Dynamics 365 for Talent'tan Dynamics 365 for Finance and Operations tümleştirmesi](talent-financeandoperations-integration.md).

Attract ve Onboard için tüm veri Common Data Service için yereldir.

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Yeni bir eşlemeyi şablonları kullanmadan oluşturabilir miyim?

Şablonları, başlangıç noktasıdır. Kendi şablonunuzu oluşturabilirsiniz, ancak şablon bir tümleştirme projesi oluşturma sırasında her zaman gereklidir. Veri tümleştirme (DI) şablonları ve projeleri hakkında daha fazla bilgi için bkz. [Common Data Service için veri tümleştirme](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>Talent ve Finance and Operations arasında aktarmak için finansal boyutlar eşleyebilir miyim?

Mali boyutlar şu anda Common Data Service içinde mevcut değildir ve bunu sonucunda varsayılan şablonun parçası değildir. Bu varlık planlanmıştır, ancak şu anda zaman çizelgesi mevcut değildir.

Finance and Operations içinde bulunan ancak Talent içinde bulunmayan veri için iki sistemi birbirine Talent için **Bağlantıları yapılandır**'ı kullanarak bağlayın. Talent ve Finance and Operations arasındaki bağlantıları yapılandırma hakkında daha fazla bilgi için bkz [yeni veya değiştirilmiş olarak ne olduğunu Dynamics 365 for Talent Core HR (31 Ekim 2018)](whats-new-talent-october-31.md).

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>Bazı durumlarda çalışanlar aldığımda, Finance and Operations içinde devre dışı çalışanlar haline gelirler. Neden?

Çalışanların Talent içinde etkin bir çalışma ayrıntısı kaydı yoksa bu hatayı alabilirsiniz. Bunu çözümlemek için **Personel Yönetimi \> Çalışanlar \> Çalışma Geçmişi \> Veri Yöneticisi**'ne gidin ve etkin bir çalışan ayrıntı kaydı olduğunu doğrulayın.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Yalnızca bir alan alt kümesine eşleşmeyi seçersem, eşleştirilmemiş alanlara yapılan değişiklikler bir eşitleme tetikler mi?

Veri eşitleme yürütme planını izler. Tümleştirme, alanın tümleştirme eşleştirmesinin parçası olup olmadığından bağımsız olarak kayıttaki herhangi bir alan değişirse kaydı çekecektir.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Yalnızca etkin alt değişiklikleri ve işten çıkarılan kayıtların nasıl gönderebilirim?

"Gelişmiş sorgu" kullanarak, kaynak verisini hedefe aktarmadan önce filtreleyebilir ve şekillendirebilirsiniz.

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>Belirli bir varlık için hangi alanların Finance and Operations'a gönderileceğini belirtebilir miyim?

Alanlar tümleştirme görevinden eklenebilir veya çıkartılabilir. Common Data Service varlığı içinde mevcut olan tüm veri alanları Core HR'dan doldurulmayacaktır.
Ek veriler PowerApps ile doldurulabilir.

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Tümleştirmeyi bir toplu iş olarak ayarlıyorum, ancak hedef sisteme Talent bağlantıyı kaybetti. Aynı değişiklik kümesini hedef sisteme nasıl gönderebilirim?

Özel durum işleme için özel bir kurulum gerekli değildir. Veri Tümleştirme, kaynak ve hedefte gerçekleşen hatları yakalar ve raporlar ve el ile yeniden denemelere izin verecektir. Ancak, el ile veri düzeltmeye izin vermez. Veri güncelleştirmeleri gerekliyse, kaynak veya hedefte gerçekleştirilmelidir.

## <a name="can-i-set-up-bi-directional-integration"></a>Çift yönlü tümleştirme ayarlayabilir miyim?

Hayır, tümleştirme şu anda yalnızca tek yönlüdür (Talent'tan Finance and Operations'a). Bununla birlikte, Talent'tan Finance and Operations'a veri göndermek için bir varsayılan şablon vardır.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Tümleştirmemin bir parçası olarak kayıt silinmesine izin verebilir miyim?

Hayır, Veri Tümleştirici, silinen kayıtları veri aktarımı için yakalamayacaktır. Yalnızca veri oluşturma ve güncelleştirme (UPSERT) şu anda dahildir.

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Hatalı yürütmeyi yeniden çalıştırabilir miyim? Bu durumda, tam dosya mı gönderir yalnızca değişiklikleri mi?

Veri Tümleştiricinin ilk çalıştırılması her zaman tam çalıştırmadır. Sonraki yürütmeler değişiklik izlemeye dayanır. Bir hatalı çalışma yürütülürse, yürütme kapsamdaki kayıtları çıkartır ve Common Data Service'ten en güncel değişiklikleri gönderir.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Proje kaydettiğimde, "Proje eşleme hatalarına sahip" hatasını alıyorum. Ne yapmam gerekir?

Tümleştirme anahtarlarınızı kurulumunu denetleyin, kurulum için gerekli değişiklikleri yapın ve sonra varlıkları projedeki yenileyin.

Varsayılan şablon kullanıldığında, tümleştirme anahtarları otomatik olarak alınacak. Varolan şablona yeni görevler eklendiğinde bu sorun ortaya çıkabilir.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Çalışanların işe sahip olduğu N sayıda tüzel varlığa sahipsem, bunların her biri için eşleşme oluşturmam gerekir mi?

Evet, Finance and Operations içindeki her bir düzel varlık için, veri tümleştirmede ayrı bir tümleştirme projesine ihtiyaç duyarsınız.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Microsoft tarafından sağlanan varsayılan şablonun parçası olmayan verileri aktarmak gerekiyor. Bunu yapabilir miyim?

Evet, varolan şablondan alanlar kaldırılabilir veya eklenebilir. Şablon diğer Common Data Service varlıkları için ek verileri dahil etmek üzere değiştirilebilir. Varlığın, şablona dahil edilmesi için Common Data Service içinde olması gerekir. 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Yeni Finance and Operations ve Talent ortamları oluşturdum ve "Veri değeri tutarlılık kısıtlamalarını ihlal ediyor" hatasını alıyorum. Neden?

Bu hatanın nedenleri arasında şunlar olabilir:

- Veri aktarma, kaynakta (Common Data Service) yinelenen kayıtların ayıklanmasıyla sonuçlandı.

- Veri aktarımı, Finance and Operations'ta ihtiyaç duyulan alanlar için boş değerlere sahip. Verinin Common Data Service içindeki olduğundan ve Finance and Operations gereksinimlerini karşıladığından emin olun.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Yürütme hataları varsa ve Çalışan kimliği eşitlenmediyse, hatalı çalışan kaydına sahip geçmiş işi nasıl bulabilirim?

Veri Tümleştirici, Finance and Operations içinde birden fazla proje oluşturur. Veri Tümleştirici görevi ve Finance and Operations projesi arasındaki ilişki birebir bir ilişkidir.

Veri Tümleştirici yürütme geçmişinden zamanı takip edin ve Finance and Operations içindeki dizin -1 olan projeyi arayın. Görev numarası Veri Tümleştircisinde 9 ise, Finance and Operations içindeki dizin 8'dir.

1. Veri Tümleştiricisinden görev dizinini yakalayın (bu örnekte "9"dur).

![Veri Tümleştiricisinden görev dizinini yakalayın.](media/CaptureTaskIndex.png)

2. Projenin yürütme zamanını izleyin.

![Projenin yürütme zamanını izleyin](media/CaptureTimeOfExecution.png)

3. Finance and Operations'ta, dizin - 1'i belirleyin. Bu örnekte, sonek "8"e sahip olan ve yürütme zamanı dizin "0" projesi olan proje, Adım 2'deki yürütme zamanı ile eşleşiyor.

![Dizini tanımlayın](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>Talent ve Finance and Operations tümleştirmesinden sonra Talent verilerimi Finance and Operations içinde görmüyorum. Ne yapmam gerekir?

Finance and Operations tümleştirmesi iki adımlı bir işlemdir. Öncelikle, Talent verisinin güncelleştirilmiş ve Common Data Service içinde kullanılabilir olduğundan emin olun. Bu neredeyse gerçek zamanlı bir eşitlemedir ve PowerApps içinde veri girişleri içindeki veriye bakarak doğrulanabilir.

![Common Data Service içindeki veri](media/DataInCDS.png)

Veri Common Data Service'te beklendiği gibi görüntülenmiyorsa, varlığın tümleştirme ile desteklendiğinden emin olun. Common Data Service içine ek veri dahil etmek için Microsoft tarafından bir değişiklik gerekir.

Varlık destekleniyorsa ve veri Common Data Service içinde kullanılabilirse, Veri Tümleştiricisi içinde eşleştirmenin doğru olduğunu doğrulayın. Tümleştirme eşleştirmesi doğru gözüküyorsa, veri yönetimi işlerini başarıyla çalıştırıldığını doğrulayın. Toplu işlerin yürütülmesinde hatalar ortaya çıkabilir. Veri Yönetimi hakkında daha fazla bilgi için bkz. [Veri yönetimi](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>Çalışanlarımın adresleri onları Finance and Operations'a aktardıktan sonra doğru değil. Ne yapmalıyım?

**Konum Kimliği** için numara serisi, Talent ve Finance and Operations içinde aynı düzeni kullanır. Numara serisinin her iki tarafta da benzersiz olması gerekir, bu sayede veriyi Common Data Service'ten Finance and Operations'a tümleştirirken adres çakışmaları gerçekleşmez.

Talent tümleştirmesi sırasında, numara serilerinin Talent ve Finance and Operations içinde aynı olmadığını doğrulayın. Tüm numara serilerinin, verinin her iki sistemde de tutulabildiği yerlerde aynı olmadığını doğrulayın.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Bağlantımı kümesi oluştururken, Bağlantı açılır listesinde bağlantıyı göremiyorum. Ne yapmam gerekir?

Bağlantılarınızı oluştururken Dynamics 365 for Finance and Operations (şu anda önizlemede) ve Common Data Service seçtiğinizden emin olun.

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Çalışmaları eşitlerken “CompanyInfo_FK mevcut değil" veya “Değer 12/31/2154 11:59:59 pm', 'Çalışma sonlanma tarihi' ilgili 'Çalışma' tablosunda bulunamadı.” hatasını alıyorum. Ne yapmalıyım?

Doğru tüzel varlıkları eşlediğinizden emin olun. Tüzel varlık eşitleme, varsayılan şablonun parçası değildir, bu nedenle Talent ve Common Data Service bulunan her bir tüzel varlığın Finance and Operations'ta da mevcut olması beklenir.
İlişkili Bağlantı Kümesi için doğru tüzel varlıkları seçtiğinizden emin olun.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>Projemi ayarladıktan sonra, Finance and Operations için alan eşlemenin boş olduğu gözüküyor. Ne yapmalıyım?

Finance and Operations içinde veri varlıklarını **Veri yönetimi \> Çerçeve parametreleri \> Varlık ayarları \> Varlık listesini yenile**'ye giderek yenileyin. Bunun tamamlanması birkaç dakika sürer ve daha sonra bu eşleşmeleri görmeniz gerekir. Yeni proje oluşturulduğunda bu sorun oluşur.

![Eksik alan eşlemeleri](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Ek kaynaklar

- Veri Tümleştirici (DI): 

  - [Veriyi Common Data Service içine tümleştir](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [Veri Tümleştirici hata yönetimi ve sorun giderme](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [PowerApps, Microsoft Flow ve Common Data Service içinde sistem tarafından oluşturulan DSR taleplerine yanıt vermek](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Veri Yönetimi:

  - [Veri yönetimi](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
