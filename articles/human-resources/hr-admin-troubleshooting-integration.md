---
title: Finans ile tümleştirme SSS
description: Bu konu altında, bir İnsan Kaynakları ve Finance tümleştirmesinde hangi verilerin eşitleneceği açıklanmaktadır.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f57e995dfcc04de8384d15f238c45290b3c3cbd
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067631"
---
# <a name="integration-with-finance-faq"></a>Finans ile tümleştirme SSS


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bu makalede, Dynamics 365 Human Resources, Dynamics 365 Finance ile tümleştirildiğinde hangi verilerin eşitleneceğine dair sıkça sorulan sorular yanıtlanmaktadır.

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>Power Apps uygulamasında Dynamics 365 Talent uygulama kullanıcısını düzenleyebilir miyim?

Hayır. Eğer Human Resources uygulama kullanıcısını düzenlerseniz, Human Resources ve Dataverse arasındaki bütünleşme başarısız olabilir. Aşağıdaki tabloda, Talent uygulama kullanıcısı için varsayılan ayarlar gösterilmektedir.

| Tam Ad | Başvuru kodu | Azure AD Nesne kodu | Başvuru kodu URI |
| --- | --- | --- | --- |
| Dynamics365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![Talent uygulama kullanıcısı için varsayılan ayarlar.](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Tüm veriler mi eşitlenir yoksa yalnızca bazı veri varlıkları mı?

Bir veri alt kümesi eşitlenir. Tüm varlıkların listesi için bkz. [Dynamics 365 Finance tümleştirmesi](hr-admin-integration-finance.md).

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>Dataverse'e eşitlenen verileri neden göremiyorum?

Varsayılan olarak, Dataverse tümleştirmesi sağlanan demo verileri içermeyen yeni ortamlarda kapalıdır. Varsayılan olarak, demo verileri içeren yeni ortamlarda açıktır ve ortam sağlandığında veri eşitlemesi başlar. Ortamınız veri eşitlemeye hazır olduktan sonra tümleştirmeyi açabilirsiniz. Daha fazla bilgi için bkz. [Dataverse tümleştirmesini yapılandırma](hr-admin-integration-common-data-service.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Yeni bir eşlemeyi şablonları kullanmadan oluşturabilir miyim?

Şablonları, başlangıç noktasıdır. Kendi şablonunuzu oluşturabilirsiniz, ancak şablon bir tümleştirme projesi oluşturma sırasında her zaman gereklidir. Veri tümleştirme (DI) şablonları ve projeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse için veri tümleştirme](/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>İnsan Kaynakları ve Finance arasında aktarmak üzere mali boyutlar eşleyebilir miyim?

Mali boyutlar şu anda Dataverse içinde mevcut değildir ve bunu sonucunda varsayılan şablonun parçası değildir. Bu varlık planlanmıştır, ancak şu anda zaman çizelgesi mevcut değildir.

Finance içinde bulunan ancak Human Resources içinde bulunmayan veri için iki sistemi birbirine Human Resources için **Bağlantıları yapılandır**'ı kullanarak bağlayın.

![Mali boyutları eşleme.](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Bazı durumlarda çalışanları içe aktardığım zaman, Finance'te devre dışı çalışanlar haline geliyorlar. Neden?

Çalışanların İnsan Kaynakları içinde etkin bir çalışma ayrıntısı kaydı yoksa bu hatayı alabilirsiniz. Bunu çözümlemek için **Personel Yönetimi \> Çalışanlar \> Çalışma Geçmişi \> Veri Yöneticisi**'ne gidin ve etkin bir çalışan ayrıntı kaydı olduğunu doğrulayın.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Yalnızca bir alan alt kümesine eşleşmeyi seçersem, eşleştirilmemiş alanlara yapılan değişiklikler bir eşitleme tetikler mi?

Veri eşitleme yürütme planını izler. Tümleştirme, alanın tümleştirme eşleştirmesinin parçası olup olmadığından bağımsız olarak kayıttaki herhangi bir alan değişirse kaydı çekecektir.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Yalnızca etkin alt değişiklikleri ve işten çıkarılan kayıtların nasıl gönderebilirim?

"Gelişmiş sorgu" kullanarak, kaynak verisini hedefe aktarmadan önce filtreleyebilir ve şekillendirebilirsiniz.

![Etkin çalışan gelişmiş sorgusu.](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Belirli bir varlık için hangi alanların Finance'e gönderileceğini belirtebilir miyim?

Alanlar tümleştirme görevinden eklenebilir veya çıkartılabilir. Dataverse tablosu içinde mevcut olan tüm veri alanlarıİnsan Kaynakları'ndan doldurulmayacaktır.
Ek veriler Power Apps ile doldurulabilir.

![Bir tümleştirme görevinden alanları ekleme veya çıkartma.](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Tümleştirmeyi bir toplu iş olarak ayarlıyorum, ancak hedef sisteme İnsan Kaynakları bağlantıyı kaybetti. Aynı değişiklik kümesini hedef sisteme nasıl gönderebilirim?

Özel durum işleme için özel bir kurulum gerekli değildir. Veri Tümleştirme, kaynak ve hedefte gerçekleşen hatları yakalar ve raporlar ve el ile yeniden denemelere izin verecektir. Ancak, el ile veri düzeltmeye izin vermez. Veri güncelleştirmeleri gerekliyse, kaynak veya hedefte gerçekleştirilmelidir.

## <a name="can-i-set-up-bi-directional-integration"></a>Çift yönlü tümleştirme ayarlayabilir miyim?

Hayır, tümleştirme şu anda yalnızca tek yönlüdür (İnsan Kaynakları'ndan finans ve operasyon uygulamalarına). Bununla birlikte, İnsan Kaynakları'ndan Finance'e veri göndermek için bir varsayılan şablon vardır.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Tümleştirmemin bir parçası olarak kayıt silinmesine izin verebilir miyim?

Hayır, Veri Tümleştirici, silinen kayıtları veri aktarımı için yakalamayacaktır. Yalnızca veri oluşturma ve güncelleştirme (UPSERT) şu anda dahildir.

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Hatalı yürütmeyi yeniden çalıştırabilir miyim? Bu durumda, tam dosya mı gönderir yalnızca değişiklikleri mi?

Veri Tümleştiricinin ilk çalıştırılması her zaman tam çalıştırmadır. Sonraki yürütmeler değişiklik izlemeye dayanır. Bir hatalı çalışma yürütülürse, yürütme kapsamdaki kayıtları çıkartır ve Dataverse'ten en güncel değişiklikleri gönderir.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Proje kaydettiğimde, "Proje eşleme hatalarına sahip" hatasını alıyorum. Ne yapmam gerekir?

Tümleştirme anahtarlarınızı kurulumunu denetleyin, kurulum için gerekli değişiklikleri yapın ve sonra varlıkları projedeki yenileyin.

Varsayılan şablon kullanıldığında, tümleştirme anahtarları otomatik olarak alınacak. Var olan şablona yeni görevler eklendiğinde bu sorun ortaya çıkabilir.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Çalışanların işe sahip olduğu N sayıda tüzel varlığa sahipsem, bunların her biri için eşleşme oluşturmam gerekir mi?

Evet, Finance'teki her bir tüzel kişilik için, veri tümleştirmede ayrı bir tümleştirme projesine gereksiniminiz olacaktır.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Microsoft tarafından sağlanan varsayılan şablonun parçası olmayan verileri aktarmak gerekiyor. Bunu yapabilir miyim?

Evet, var olan şablondan alanlar kaldırılabilir veya eklenebilir. Şablon diğer Dataverse tabloları için ek verileri dahil etmek üzere değiştirilebilir. Varlığın, şablona dahil edilmesi için Dataverse içinde olması gerekir. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Kısa süre önce Finance ve İnsan Kaynakları ortamları oluşturdum ve "Veri değeri tutarlılık kısıtlamalarını ihlal ediyor" hatasını alıyorum. Neden?

Bu hatanın nedenleri arasında şunlar olabilir:

- Veri aktarma, kaynakta (Dataverse) yinelenen kayıtların ayıklanmasıyla sonuçlandı.

- Veri aktarımı, finans ve operasyon uygulamalarına ihtiyaç duyulan alanlar için boş değerlere sahip. Verinin Dataverse içindeki olduğundan ve Finance and Operations gereksinimlerini karşıladığından emin olun.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Yürütme hataları varsa ve Çalışan kimliği eşitlenmediyse, hatalı çalışan kaydına sahip geçmiş işi nasıl bulabilirim?

Veri Tümleştirici, Finance'te birden fazla proje oluşturur. Veri Tümleştirici görevi ve Finance projesi arasındaki ilişki bire bir ilişkidir.

Veri Tümleştirici yürütme geçmişinden zamanı takip edin ve Finance'te dizin -1 olan projeyi arayın. Görev numarası Veri Tümleştirici'de 9 ise, Finance'teki dizin 8'dir.

1. Veri Tümleştiricisinden görev dizinini yakalayın (bu örnekte "9"dur).

    ![Veri Tümleştiricisinden görev dizinini yakalama.](media/CaptureTaskIndex.png)

2. Projenin yürütme zamanını izleyin.

    ![Projenin yürütme zamanını izleme.](media/CaptureTimeOfExecution.png)

3. Finance'te - 1 dizini belirleyin. Bu örnekte, sonek "8"e sahip olan ve yürütme zamanı dizin "0" projesi olan proje, Adım 2'deki yürütme zamanı ile eşleşiyor.

    ![Dizini tanımlama.](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>İnsan Kaynakları ve finans'yı tümleştirdikten sonra, İnsan Kaynakları verilerimi finans içinde görmüyorum. Ne yapmam gerekir?

Finance'e tümleştirme iki adımlı bir işlemdir. Öncelikle, İnsan Kaynakları verisinin güncelleştirilmiş ve Dataverse içinde kullanılabilir olduğundan emin olun. Bu neredeyse gerçek zamanlı bir eşitlemedir ve Power Apps içinde veri tabloları içindeki veriye bakarak doğrulanabilir.

![Dataverse içindeki veri.](media/DataInCDS.png)

Veri Dataverse'te beklendiği gibi görüntülenmiyorsa, varlığın tümleştirme ile desteklendiğinden emin olun. Dataverse içine ek veri dahil etmek için Microsoft tarafından bir değişiklik gerekir.

Varlık destekleniyorsa ve veri Dataverse içinde kullanılabilirse, Veri Tümleştiricisi içinde eşleştirmenin doğru olduğunu doğrulayın. Tümleştirme eşleştirmesi doğru gözüküyorsa, veri yönetimi işlerini başarıyla çalıştırıldığını doğrulayın. Toplu işlerin yürütülmesinde hatalar ortaya çıkabilir. Veri Yönetimi hakkında daha fazla bilgi için bkz. [Veri yönetimi](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Çalışanlarımın adresleri Finance'e aktardıktan sonra doğru görünmüyor. Ne yapmalıyım?

**Konum Kodu** için numara serisi, İnsan Kaynakları'ta ve Finance'te aynı düzeni kullanır. Numara sırasının her iki tarafta da benzersiz olması gerekir, bu sayede veriyi Dataverse'den finans ve operasyon uygulamalarına tümleştirirken adres çakışmaları gerçekleşmez.

İnsan Kaynakları tümleştirmesi sırasında, numara serilerinin İnsan Kaynakları ve Finance içinde aynı olmadığını doğrulayın. Tüm numara serilerinin, verinin her iki sistemde de tutulabildiği yerlerde aynı olmadığını doğrulayın.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Bağlantımı kümesi oluştururken, Bağlantı açılır listesinde bağlantıyı göremiyorum. Ne yapmam gerekir?

Bağlantılarınızı oluştururken Dynamics 365 Finance'i ve Dataverse'ü seçtiğinizden emin olun.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Çalışmaları eşitlerken “CompanyInfo_FK mevcut değil" veya “Değer 12/31/2154 11:59:59 pm', 'Çalışma sonlanma tarihi' ilgili 'Çalışma' tablosunda bulunamadı.” hatasını alıyorum. Ne yapmalıyım?

Doğru tüzel varlıkları eşlediğinizden emin olun. Tüzel varlık eşitleme, varsayılan şablonun parçası değildir, bu nedenle İnsan Kaynakları ve Dataverse bulunan her bir tüzel varlığın Finance'te de mevcut olması beklenir. İlişkili Bağlantı Kümesi için doğru tüzel varlıkları seçtiğinizden emin olun.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Projemi ayarladıktan sonra Finance için alan eşleşmesi boş görünüyor. Ne yapmalıyım?

Finance'te veri varlıklarını **Veri yönetimi \> Çerçeve Parametreleri \> Varlık ayarları \> Varlık listesini yenile**'ye giderek yenileyin. Bunun tamamlanması birkaç dakika sürer ve daha sonra bu eşleşmeleri görmeniz gerekir. Yeni proje oluşturulduğunda bu sorun oluşur.

![Eksik alan eşlemeleri.](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Ek kaynaklar

- Veri Tümleştirici (DI): 

  - [Veriyi Microsoft Dataverse içine tümleştir](/powerapps/administrator/data-integrator)

  - [Veri Tümleştirici hata yönetimi ve sorun giderme](/powerapps/administrator/data-integrator-error-management)

  - [Power Apps, Microsoft Power Automate ve Dataverse'te sistem tarafından oluşturulan günlükler için DSR taleplerine yanıt verme](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Veri Yönetimi:

  - [Veri yönetimi](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

