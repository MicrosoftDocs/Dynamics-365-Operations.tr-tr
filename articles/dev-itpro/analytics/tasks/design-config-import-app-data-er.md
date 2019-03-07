---
title: Gelen belgeleri ayrıştırmak için ER yapılandırmaları tasarlama
description: Bu yordam gelen elektronik belgeyi ayrıştırmak için Elektronik raporlama (ER) yapılandırmalarının nasıl kullanılacağını açıklar.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e5f826afa141c0851a963b33e40c58513e60a07
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "326113"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>Gelen belgeleri ayrıştırmak için ER yapılandırmaları tasarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam gelen elektronik belgeyi ayrıştırmak için Elektronik raporlama (ER) yapılandırmalarının nasıl kullanılacağını açıklar. Bu yordamda, örnek şirket Litware, Inc. için oluşturulan gerekli ER yapılandırmalarını içe aktaracak ve bunları gelen elektronik belgeleri ayrıştırmak için kullanacaksınız. Bu yordamdaki adımları tamamlamak için, ilk olarak "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamını tamamlamanız gerekir.

Bu yordam, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur. 

Bu adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir. Başlamadan önce "Uygulama verilerini güncelleştirmek için gelen belgeleri ayrıştırma" (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents) başlıklı konuda listelenen dosyaları indirip kaydedin. Dosyalar: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.  
2. Raporlama konfigürasyonları'na tıklayın.
    * Aşağıdaki senaryo XML biçimindeki gelen elektronik belgeleri ayrıştırma yeteneklerini göstermek için kullanılacaktır: ERP uygulaması (Dynamics 365 for Finance and Operations), web hizmetinden (http://efsta.org/ EFSTA mali hizmeti gibi) veri ister ve uygulama verileri gerektiği gibi güncelleştirmek için gelen yanıtları ayrıştırır. En etkili ayrıştırma yöntemi için, XML biçimindeki gelen belgelerdeki farklı yapıya rağmen tek bir ER biçimi kullanılır.   

## <a name="import-and-review-er-configurations"></a>ER yapılandırmalarını gözden geçirme ve içe aktarma
Gelen dosyada ayrıntıları saklamak için tasarlanan örnek veri modelini içeren ER modeli yapılandırmasını içe aktarın.  
1. Değiştir seçeneğine tıklayın.
2. XML dosyasından yükle'ye tıklayın.
    * Gözat'a tıklayın ve EFSTA model.xml dosyasını seçin.  
3. Tamam'a tıklayın.
4. Ağaçta 'EFSTA modeli' öğesini seçin.
5. Tasarımcı'yı tıklatın.
    * İçe aktarılan veri modelinin yapısını gözden geçirin. enumType numaralandırmasının şu türde hizmet yanıtlarını tanımak üzere tanımlandığını unutmayın: hareket gönderimi hakkına onay almak, gönderilen son hareket hakkında bilgi almak ve desteklenmeyen yanıt türlerini tanımak.   
6. Ağaçta 'Yanıt' öğesini genişletin.
    * ‘Yanıt’ kök öğesinin uygulama verilerini uygun şekilde güncelleştirmek için desteklenen servis yanıtından hangi tür verilerin alınacağını belirlemek üzere tanımlandığını unutmayın.   
7. Sayfayı kapatın.
    * Gelen belgelerin verileri ER veri modelinde depolamak için nasıl ayrıştırılacağını belirten ER biçimi yapılandırmasını içe aktaracaksınız.   
8. Değiştir seçeneğine tıklayın.
9. XML dosyasından yükle'ye tıklayın.
    * Gözat'a tıklayın ve EFSTA format.xml dosyasını seçin.  
10. Tamam'a tıklayın.
11. Ağaçta 'EFSTA modeli' öğesini genişletin.
12. Ağaçta, 'EFSTA modeli\EFSTA biçimi' öğesini seçin.
13. Tasarımcı'yı tıklatın.
14. Genişlet/daralt'a tıklayın.
    * SERVİS TALEBİ biçimi öğesinin kök olarak kullanıldığını ve iç içe geçmiş üç DOSYA öğesi içerdiğini ve bunun bu biçimin farklı biçimledeki gelen dosyaları ayrıştırmak üzere tasarlandığı anlamına geldiğini unutmayın.  
15. Ağaçta, 'Yanıtlar\Hareketi tamamlama\TraC' öğesini seçin.
    * Gönderilen hareket hakkındaki yanıtın ‘TraC’ kök öğesinden başlatıldığını unutmayın.   
16. Ağaçta, 'Yanıtlar\Son hareket talebi\Tra' öğesini seçin.
    * Gönderilen son hareket hakkındaki yanıtın ‘Tra’ kök öğesinden başlatıldığını unutmayın.   
17. Ağaçta, 'Yanıtlar\Beklenmeyen yanıt\Metin' öğesini seçin.
    * Yukarıda belirtilenden farklı olan yanıt türlerini tanımak üzere iç içe geçmiş METİN öğesine sahip üçüncü DOSYA öğesi eklenmiştir.   
18. Biçimi modelle eşle'ye tıklayın.
    * Bu model eşleme, ayrıştırılan gelen belgenin ayrıntılarını veri modeli öğelerini kullanarak saklamak için veri akışı tanımı içerir.  
19. Tasarımcı'yı tıklatın.
20. Ağaçta, 'biçim' metnini genişletin.
21. Ağaçta, 'biçim\Yanıtlar: Servis Talebi(Yanıtlar)' öğesini genişletin.
    * 'Biçim' veri kaynağının yapısını gözden geçirin. Üç yanıt türürünün de ayrı ayrı sunulduğunu unutmayın.   
22. Ağaçta, 'biçim\Yanıtlar: Servis Talebi(Yanıtlar)\aType' öğesini seçin.
    * ‘aType’ veri kaynağı öğesi yanıt türünü belirtmek için eklenmiştir ve ‘Tür’ veri modeli öğesine bağlıdır.  
23. Doğrulamalar sekmesine tıklayın.
24. Ağaçta 'Tür = format.Responses.aType' öğesini seçin.
    * ER doğrulamasının kullanıcıları yanıt yapısının hareket gönderimi onayıyla veya son gönderilen hareketle ilgili bilgilerle (desteklenmeyen yanıt durumu) eşleşmemesi durumunda bilgilendirmek üzere yapılandırılmış olduğunu unutmayın.   
25. Sayfayı kapatın.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Gelen dosyaları ayrıştırmak için yapılandırılan ER biçimi model eşlemesini çalıştırma
Yapılandırılan ER biçiminin gelen hizmet yanıtlarını nasıl ayrıştıracağını görmek üzere test amacıyla oluşturulan model eşlemesini çalıştıracaksınız. Bu adım, farklı web hizmeti yanıtı türlerini simüle etmek için farklı XML dosyaları kullanır.   
1. Response1.xml dosyasını web tarayıcısı gibi bir xml okuyucuda açın. Bu dosyanın tamamlanan hareketle ilgili onay ayrıntılarını içerdiğini (‘TraC’ kök öğesidir) unutmayın.   
2. Çalıştır öğesine tıklayın.
    * Gözat'a tıklayın ve Response1.xml dosyasını seçin.  
3. Tamam'a tıklayın.
    * Ortaya çıkan sonucu inceleyin. Yanıt türünün doğru şekilde tanındığını ve ayrıştırıldığını unutmayın (ERModelEnumDataSourceHandler#EFSTA model#enumType#C hareket tamamlanma durumu anlamına gelir).   
    * Response2.xml dosyasını bir XML okuyucuda açın. Bu dosyanın gönderilen son hareketle ilgili bilgileri içerdiğini (‘Tra’ kök öğesidir) unutmayın.   
4. Çalıştır öğesine tıklayın.
    * Gözat'a tıklayın ve Response2.xml dosyasını seçin.  
5. Tamam'a tıklayın.
    * Ortaya çıkan sonucu inceleyin. Yanıt türünün doğru şekilde tanındığını ve ayrıştırıldığını unutmayın (ERModelEnumDataSourceHandler#EFSTA model#enumType#R sistem yeniden başlama durumu anlamına gelir).   
    * Response3.xml dosyasını bir XML okuyucuda açın. Bu dosyanın TraZ kök öğesinden başlatıldığını ve bu yapının ER biçimi kullanılarak yapılandırılmadığını unutmayın.   
6. Çalıştır öğesine tıklayın.
    * Gözat'a tıklayın ve Response3.xml dosyasını seçin.  
7. Tamam'a tıklayın.
    * Ortaya çıkan sonucu inceleyin. Yanıt türünün desteklenmeyen olarak doğru şekilde tanındığını unutmayın (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). İlgili ileti Bilgi günlüğne yerleştirilmiştir (ER doğrulama ayarına göre) ve veri modelinin çoğu kısmı doldurulmuştur.   
    * Response4.xml dosyasını bir XML okuyucuda açın. Bu dosyanın yapısının başarılı şekilde ayrıştırılan Response1.xml dosyası ile neredeyse aynı olduğuna dikkat edin. ‘TraC’ kök öğesinin iç içe geçmiş öğelerinin sırası dışında bir farklılık yoktur.   
8. Çalıştır öğesine tıklayın.
    * Gözat'a tıklayın ve Response4.xml dosyasını seçin.  
9. Tamam'a tıklayın.
    * Ortaya çıkan sonucu inceleyin. Yanıt türünün desteklenmeyen olarak doğru şekilde tanındığını unutmayın (ERModelEnumDataSourceHandler#EFSTA model#enumType#U)). İlgili ileti Bilgi günlüğne yerleştirilmiştir ve veri modelinin çoğu kısmı doldurulmuştur. Bu nedenle, ER biçiminin geçerli ayarı gelen dosyanın kök öğesindeki iç içe geçmiş öğelerin belirli bir sırası olduğunu kabul eder.   
10. Sayfayı kapatın.
11. Ağaçta, 'Yanıtlar\Hareketi tamamlama\TraC' öğesini seçin.
12. İç içe geçmiş öğeleri ayrıştırma sırası alanında 'Herhangi biri' seçeneğini seçin.
    * ‘İç içe geçmiş öğeleri ayrıştırma sırası’ alanında Herhangi biri seçeneği seçerek bu kök XML öğesi için herhangi bir iç içe geçmiş öğeler sırasına izin verin.  
13. Kaydet'e tıklayın.
14. Biçimi modelle eşle'ye tıklayın.
15. Çalıştır öğesine tıklayın.
    * Gözat'a tıklayın ve Response4.xml dosyasını seçin.  
16. Tamam'a tıklayın.
    * Ortaya çıkan sonucu inceleyin. Yanıt türünün artık uygun şekilde Response1.xml dosyasının eşiti olarak tanındığını unutmayın.  

