---
title: Gelen belgeleri ayrıştırmak için ER yapılandırmaları tasarlama
description: Bu yordam gelen elektronik belgeyi ayrıştırmak için Elektronik raporlama (ER) yapılandırmalarının nasıl kullanılacağını açıklar.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8068850ee143540ff9f3b6222485d3ecd2a2a82020063f34cfd7b5a69826eda3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756393"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>Gelen belgeleri ayrıştırmak için ER yapılandırmaları tasarlama

[!include [banner](../../includes/banner.md)]

Bu yordam gelen elektronik belgeyi ayrıştırmak için Elektronik raporlama (ER) yapılandırmalarının nasıl kullanılacağını açıklar. Bu yordamda, örnek şirket Litware, Inc. için oluşturulan gerekli ER yapılandırmalarını içe aktaracak ve bunları gelen elektronik belgeleri ayrıştırmak için kullanacaksınız. Bu yordamdaki adımları tamamlamak için öncelikle "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamını tamamlamanız gerekir.

Bu yordam, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.

Bu adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir. Başlamadan önce "Uygulama verilerini güncelleştirmek için gelen belgeleri ayrıştırma" [Gelen belgeleri ayrıştırma](../parse-incoming-electronic-documents.md) başlıklı konuda listelenen dosyaları indirip kaydedin. Dosyalar: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.
2. Raporlama yapılandırmaları'nı seçin.
    * Aşağıdaki senaryo, XML biçiminde gelen elektronik belgeleri ayrıştırma özellikleri göstermek için kullanılacaktır: ERP uygulaması, web hizmetinden (ör. [efsta](http://efsta.org/) mali hizmeti) veri ister ve uygulama verilerini gerektiği gibi güncelleştirmek için gelen yanıtları ayrıştırır. En etkili ayrıştırma yöntemi için, XML biçimindeki gelen belgelerdeki farklı yapıya rağmen tek bir ER biçimi kullanılır.

## <a name="import-and-review-er-configurations"></a>ER yapılandırmalarını gözden geçirme ve içe aktarma

Gelen dosyada ayrıntıları saklamak için tasarlanan örnek veri modelini içeren ER modeli yapılandırmasını içe aktarın.

1. Döviz'i seçin.
2. XML dosyasından yükle'yi seçin.
    * Göz at'ı seçin ve EFSTA model.xml dosyasını seçin.
3. Tamam'ı seçin.
4. Ağaçta 'EFSTA modeli' öğesini seçin.
5. Tasarımcı’yı seçin.
    * İçe aktarılan veri modelinin yapısını gözden geçirin. enumType numaralandırması, şu türde hizmet yanıtlarını tanımak üzere tanımlanmıştır: işlem gönderimi hakkında onay almak, gönderilen son işlem hakkında bilgi almak ve desteklenmeyen yanıt türlerini tanımak.
6. Ağaçta 'Yanıt' öğesini genişletin.
    * "Yanıt" kök öğesi, uygulama verilerini uygun şekilde güncelleştirmek için desteklenen servis yanıtından hangi tür verilerin alınacağını belirlemek üzere tanımlanmıştır.
7. Sayfayı kapatın.
    * Gelen belgelerin verileri ER veri modelinde depolamak için nasıl ayrıştırılacağını belirten ER biçimi yapılandırmasını içe aktaracaksınız.
8. Döviz'i seçin.
9. XML dosyasından yükle'yi seçin.
    * Göz at'ı seçin ve EFSTA format.xml dosyasını seçin.
10. Tamam'ı seçin.
11. Ağaçta 'EFSTA modeli' öğesini genişletin.
12. Ağaçta, 'EFSTA modeli\EFSTA biçimi' öğesini seçin.
13. Tasarımcı’yı seçin.
14. Genişlet/daralt'ı seçin.
    * CASE biçimi öğesi, kök olarak kullanılır ve iç içe geçmiş üç FILE öğesi içerir. Bu durum, bu biçimin farklı biçimlerdeki gelen dosyaları ayrıştıracak şekilde tasarlandığı anlamına gelir.
15. Ağaçta, 'Yanıtlar\Hareketi tamamlama\TraC' öğesini seçin.
    * Gönderilen işlem hakkındaki yanıt, "TraC" kök öğesinden başlatılır.
16. Ağaçta, 'Yanıtlar\Son hareket talebi\Tra' öğesini seçin.
    * Gönderilen son işlem hakkındaki yanıt, "Era" kök öğesinden başlatılır.
17. Ağaçta, 'Yanıtlar\Beklenmeyen yanıt\Metin' öğesini seçin.
    * Yukarıda belirtilenden farklı olan yanıt türlerini tanımak üzere iç içe geçmiş METİN öğesine sahip üçüncü DOSYA öğesi eklenmiştir.
18. Biçimi modelle eşle'yi seçin.
    * Bu model eşleme, ayrıştırılan gelen belgenin ayrıntılarını veri modeli öğelerini kullanarak saklamak için veri akışı tanımı içerir.
19. Tasarımcı’yı seçin.
20. Ağaçta, 'biçim' metnini genişletin.
21. Ağaçta, 'biçim\Yanıtlar: Servis Talebi(Yanıtlar)' öğesini genişletin.
    * 'Biçim' veri kaynağının yapısını gözden geçirin. Üç yanıt türü de ayrı ayrı sunulur.
22. Ağaçta, 'biçim\Yanıtlar: Servis Talebi(Yanıtlar)\aType' öğesini seçin.
    * ‘aType’ veri kaynağı öğesi yanıt türünü belirtmek için eklenmiştir ve ‘Tür’ veri modeli öğesine bağlıdır.
23. Doğrulamalar sekmesini seçin.
24. Ağaçta 'Tür = format.Responses.aType' öğesini seçin.
    * ER doğrulaması, kullanıcıları yanıt yapısının işlem gönderimi onayıyla veya son gönderilen işlemle ilgili bilgilerle (desteklenmeyen yanıt durumu) eşleşmemesi durumunda bilgilendirmek üzere yapılandırılmıştır.
25. Sayfayı kapatın.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Gelen dosyaları ayrıştırmak için yapılandırılan ER biçimi model eşlemesini çalıştırma

Yapılandırılan ER biçiminin gelen hizmet yanıtlarını nasıl ayrıştıracağını görmek üzere test amacıyla oluşturulan model eşlemesini çalıştıracaksınız. Bu adım, farklı web hizmeti yanıtı türlerini simüle etmek için farklı XML dosyaları kullanır.

1. Response1.xml dosyasını web tarayıcısı gibi bir xml okuyucuda açın. Bu dosya, tamamlanan işlemle ilgili onay ayrıntıları içerir ("TraC" kök öğesidir).
2. Çalıştır'ı seçin.
    * Göz at'ı seçin ve Response1.xml dosyasını seçin.
3. Tamam'ı seçin.
    * Ortaya çıkan sonucu inceleyin. Yanıt türü doğru şekilde tanınır ve ayrıştırılır (`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` işlem tamamlanma durumu anlamına gelir).
    * Response2.xml dosyasını bir XML okuyucuda açın. Bu dosya, gönderilen son işlemle ilgili bilgileri içerir (`Tra` kök öğesidir).
4. Çalıştır'ı seçin.
    * Göz at'ı seçin ve Response2.xml dosyasını seçin.
5. Tamam'ı seçin.
    * Ortaya çıkan sonucu inceleyin. Yanıt türü doğru şekilde tanınır ve ayrıştırılır (`ERModelEnumDataSourceHandler#EFSTA model#enumType#R`, sistem yeniden başlatma durumu anlamına gelir).
    * Response3.xml dosyasını bir XML okuyucuda açın. Bu dosya, TraZ kök öğesinden başlatılır ve bu yapı ER biçimi kullanılarak yapılandırılmamıştır.
6. Çalıştır'ı seçin.
    * Göz at'ı seçin ve Response3.xml dosyasını seçin.
7. Tamam'ı seçin.
    * Ortaya çıkan sonucu inceleyin. Yanıt türü, doğru şekilde desteklenmiyor olarak tanınır (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). İlgili ileti Bilgi günlüğne yerleştirilmiştir (ER doğrulama ayarına göre) ve veri modelinin çoğu kısmı doldurulmuştur.
    * Response4.xml dosyasını bir XML okuyucuda açın. Bu dosyanın yapısı, başarılı şekilde ayrıştırılan Response1.xml dosyası ile neredeyse aynıdır. "TraC" kök öğesinin iç içe geçmiş öğelerinin sırası dışında bir farklılık yoktur.
8. Çalıştır'ı seçin.
    * Göz at'ı seçin ve Response4.xml dosyasını seçin.
9. Tamam'ı seçin.
    * Ortaya çıkan sonucu inceleyin. Yanıt türü, doğru şekilde desteklenmiyor olarak tanınır (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). İlgili ileti Bilgi günlüğne yerleştirilmiştir ve veri modelinin çoğu kısmı doldurulmuştur. Bu davranışın nedeni, ER biçimi geçerli ayarının gelen dosyanın kök öğesindeki iç içe geçmiş öğelerin belirli bir sırası olduğunu kabul etmesidir.
10. Sayfayı kapatın.
11. Ağaçta, 'Yanıtlar\Hareketi tamamlama\TraC' öğesini seçin.
12. İç içe geçmiş öğeleri ayrıştırma sırası alanında 'Herhangi biri' seçeneğini seçin.
    * ‘İç içe geçmiş öğeleri ayrıştırma sırası’ alanında Herhangi biri seçeneği seçerek bu kök XML öğesi için herhangi bir iç içe geçmiş öğeler sırasına izin verin.
13. Kaydet'i seçin.
14. Biçimi modelle eşle'yi seçin.
15. Çalıştır'ı seçin.
    * Göz at'ı seçin ve Response4.xml dosyasını seçin.
16. Tamam'ı seçin.
    * Ortaya çıkan sonucu inceleyin. Yanıt türü, artık doğru şekilde Response1.xml dosyasının eşiti olarak tanınır.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]