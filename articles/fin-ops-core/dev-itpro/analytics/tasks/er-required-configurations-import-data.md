---
title: ER Harici bir dosyadan veri almak için gerekli olan yapılandırmaları oluşturma
description: Aşağıdaki adımlar, Sistem yöneticisi veya Elektronik raporlama geliştirici rolüne sahip bir kullanıcının harici bir dosyadan Microsoft Dynamics 365 Finance uygulamasına verileri içeri aktarmak için Elektronik raporlama (ER) yapılandırmalarını nasıl tasarlayabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9b26f4963f32be34ae1d954a3f363be7ea28d41
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684295"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>ER Harici bir dosyadan veri almak için gerekli olan yapılandırmaları oluşturma

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar, Sistem yöneticisi veya Elektronik raporlama geliştirici rolüne sahip bir kullanıcının harici bir dosyadan uygulamaya verileri içeri aktarmak için Elektronik raporlama (ER) yapılandırmalarını nasıl tasarlayabileceğini açıklar. Bu örnekte bir örnek şirket olan Litware, Inc. için gerekli ER yapılandırmalarını oluşturacaksınız. Bu adımları tamamlamak için önce "ER Bir yapılandırma sağlayıcısı oluştur ve bunu etkin olarak işaretle" Görev kılavuzundaki adımları tamamlamanız gerekir. Bu adımlar USMF veri kümesi kullanılarak tamamlanabilir. Ayrıca, Elektronik raporlamaya genel bakış konusundan (https://go.microsoft.com/fwlink/?linkid=852550): bağlantıları kullanarak şu dosyaları yerel olarak indirmeniz ve kaydetmeniz gerekir: 1099model.xml, 1099format.xml, 1099entries.xml, 1099entries.xlsx.

ER, iş kullanıcılarına harici veri dosyalarının tablolara .XML veya .TXT biçiminde içeri aktarılmasını yapılandırma özelliği sunar. Öncelikle, içeri aktardığınız verileri temsil etmek üzere soyut veri modeli ve ER veri modeli yapılandırmasının tasarlanması gerekir. Ardından, içeri aktarmakta olduğunuz dosyanın yapısını ve verileri dosyadan soyut veri modeline taşırken kullanacağınız yöntemi tanımlamanız gerekir. Bu soyut veri modeli için tasarlanan veri modeliyle eşleşen ER biçim yapılandırmasının oluşturulması gerekir. Ardından, veri modeli yapılandırması içeri aktarılan verilerin soyut veri modeli verileri olarak nasıl kalıcı hale geldiğini ve tabloları güncelleştirmek için nasıl kullanıldığını tanımlayan bir eşleme ile genişletilmelidir.  ER veri modeli yapılandırması, veri modelinin uygulama hedefleriyle bağını tanımlayan yeni bir model eşlemesiyle birlikte eklenmesi gerekir.  

Aşağıdaki senaryo ER veri içeri aktarma yeteneklerini gösterir. Bu, harici olarak izlenen ve ardından 1099'lar için Satıcı kapatmasından sonradan raporlanmak için içeri aktarılan satıcı hareketlerini içerir.   

## <a name="add-a-new-er-model-configuration"></a>Yeni bir ER model yapılandırması ekleme
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.

    Örnek şirket 'Litware, Inc.' için yapılandırma sağlayıcısının olduğunu doğrulayın için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlendiğini doğrulayın. Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.   

2. Raporlama konfigürasyonları'na tıklayın.

    Veri içeri aktarmayı desteklemek için yeni bir model oluşturmak yerine, daha önce indirdiğiniz 1099model.xml dosyasını yükleyin. Bu dosya, satıcıların hareketlerinin özel veri modelini içerir. Bu veri modeli, AOT veri varlığındaki veri bileşenleriyle eşlenmiştir.   

3. Değiştir seçeneğine tıklayın.
4. XML dosyasından yükle'ye tıklayın.

    Gözat düğmesine tıklayın ve önceden indirdiğiniz 1099model.xml dosyasına gidin.  

5. Tamam'a tıklayın.
6. Ağaçta, "1099 Ödemeleri modeli" öğesini seçin.

## <a name="review-data-model-settings"></a>Veri modeli ayarlarını gözden geçirme
1. Tasarımcı'ya tıklayın.

    Bu model, satıcıların hareketlerini iş açısından göstermek için tasarlanmıştır ve uygulamadan bağımsızdır.   

2. Ağaçta, "1099-MISC" öğesini genişletin.
3. Ağaçta, "1099-MISC\Hareketler" öğesini seçin.
4. Ağaçta, "1099-MISC\Hareketler" öğesini genişletin.

    Bu modelin Hareketler öğesi, tek tek hareketleri gösterir. Alt öğeler, her hareket için satıcı hesabı ve hareket tarihi gibi gerekli bilgileri belirtmek için kullanılır.   

5. Sayfayı kapatın.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Veri içe aktarmayı destekleyen yeni bir ER biçim yapılandırması ekleme
Bu alt görevdeki adımlar, harici dosyalardan veri içeri aktarmayı yönetmek için yeni bir biçim yapılandırması oluşturmayı gösterir.   
1. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
2. Yeni alanına, "1099 Ödemeler modeli veri modelini temel alan biçim" yazın.
3. Veri içe aktarmayı destekler alanında Evet'i seçin.
4. Bu sayfayı kapatmak için ESC tuşuna basın.

    Veri içeri aktarma işlemini desteklemek için yeni bir biçim oluşturmak yerine daha önce indirdiğiniz 1099format.xml dosyasını yükleyin. Bu dosya, içeri aktarmakta olduğunuz dosyanın tanımlanmış yapısını ve bu yapının, satıcı hareketlerinin özel veri modeliyle eşleştirilmesini içerir.   
5. Değiştir seçeneğine tıklayın.
6. XML dosyasından yükle'ye tıklayın.
    Gözat düğmesine tıklayın ve önceden indirdiğiniz 1099format.xml dosyasına gidin.  
7. Tamam'a tıklayın.
8. Ağaçta, "1099 Ödemeleri modeli" öğesini genişletin.
9. Ağaçta, "1099 Ödemeleri modeli\Satıcıların hareketlerini içe aktarma biçimi" öğesini seçin.

## <a name="review-format-settings"></a>Biçim ayarlarını gözden geçirme
1. Tasarımcı'yı tıklatın.
2. "Ayrıntıları göster" öğesini açın.
3. Genişlet/daralt'a tıklayın.
4. Genişlet/daralt'a tıklayın.

    Tasarlanan biçim, harici dosyanın beklenen yapısını gösterir. Bu dosya XML biçiminde olmalı ve dosyada kapatma kök öğesi bulunmalıdır. Her satıcının hareketi, sıfırdan çok sayıda katlılığa sahip olma olarak tanımlanan hareket öğesi ile gösterilir. Bu, gelen dosyanın sıfır hareketten çok sayıda harekete kadar çeşitli hareketler içerebileceği anlamına gelir. "Hareket" öğesinin iç içe geçmiş öğeleri, tek bir hareketin özniteliklerini gösterir. Ülke dışındaki tüm özniteliklerin zorunlu olarak işaretlendiğine dikkat edin. Bu, içeri aktarma dosyasında bulunmaları gerektiği anlamına gelir.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Veri modeline biçim eşlemesinin ayarlarını gözden geçirme
1. Biçimi modelle eşle'ye tıklayın.

    "Satıcıların hareketlerini içeri aktarmak için" eşlemesi, gelen XML dosyasından 1099-MISC tanımı seçilerek tanımlanan özel veri modelinin seçili bölümüne transfer kurallarını içerir.  

2. Tasarımcı'yı tıklatın.
3. "Ayrıntıları göster" öğesini açın.
4. Ağaçta, "biçim: Kayıt" öğesini genişletin.
5. Ağaçta, "biçim: Kayıt" öğesini seçin.

    Tasarlanan biçimin, burada bir veri kaynağı bileşeni olarak sunulduğuna dikkat edin.  

6. Ağaçta, `format: Record\*settlement: XML Element 1..1 (settlement): Record` öğesini genişletin.
7. Ağaçta, `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list` öğesini genişletin.
8. Ağaçta, `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record` öğesini genişletin.
9. Ağaçta, `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record` öğesini genişletin.
10. Ağaçta, `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record` öğesini seçin.

    Zorunlu ve isteğe bağlı biçim öğelerinin gösteriminin, önceden tanımlanmış "biçim" veri kaynağı bileşeninde farklı olduğuna dikkat edin.  
11. Ağaçta, "Hareketler: Kayıt listesi= format.settlement.'$enumerated' " öğesini genişletin.

    İçeri aktarılan dosyanın yapısını tanımlayan biçim öğelerinin özel veri modeli öğelerine bağlı olduğuna dikkat edin. Bu bağlamalara göre, içeri aktarılan XML dosyasının içeriği, mevcut veri modelinin çalışma zamanında saklanır. Ülke öğesinin bağlamasına dikkat edin. Gelen dosyada böyle bir öğe bulunmayan her hareket öğesi için, veri modelinde varsayılan ülke kodu olarak "ABD" kullanılır.  

12. Doğrulamalar sekmesine tıklayın.

    Bu biçim eşlemesi, iş açısından ele alınan içeri aktarılan verilerin kesinliğini doğrulamak için kullanıcı tanımlı mantık içerebilir. Örneğin, tanımlı ülke kodu bulunmayan içeri aktarılan dosyadaki her hareket için ayara göre, Bilgi günlüğünde kullanıcıya bu durumu bildiren ve hareketin sıra numarasını gösteren bir uyarı mesajı oluşturulur.  

13. Sayfayı kapatın.

## <a name="run-the-format-mapping-to-the-data-model"></a>Veri modeline biçim eşlemesini çalıştırma
Test amacıyla bu biçim eşlemesini yürütün. Daha önce indirdiğiniz 1099entries.xml dosyasını kullanın. Bu dosyayı, satıcı hareketlerini yönetmek için kullanılan 1099entries.xlsx çalışma kitabından dışarı aktarabilirsiniz. Oluşturulan çıktı, seçilen XML dosyasından içeri aktarılır ve gerçek içe aktarmada özel veri modelini doldurur.  

1. Çalıştır öğesine tıklayın.

    Gözat düğmesine tıklayın ve önceden indirdiğiniz 1099entries.xml dosyasına gidin.  

2. Tamam'a tıklayın.

    İçeri aktarılan dosyadaki bir hareket için eksik bir ülke kodu hakkında uyarı iletisine dikkat edin.  
    
    Seçili dosyadan içeri aktarılan ve veri modeline taşınan verileri temsil eden XML biçimindeki çıktıyı gözden geçirin.   

3. Sayfayı kapatın.
4. Sayfayı kapatın.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Hedeflere model eşlemesi ayarlarını gözden geçirme
1. Ağaçta, "1099 Ödemeleri modeli" öğesini seçin.
2. Tasarımcı'yı tıklatın.
3. Modeli veri kaynağına eşle'yi tıklayın.

    1099 el ile yapılan hareket içe aktarmalarının eşlemesi, Hedefe yön türüyle tanımlanmıştır. Bu, verileri içeri aktarmayı desteklemek için girildiği ve içeri aktarılan harici dosyanın soyut veri modeli olarak nasıl kalıcı hale geldiğini ve uygulamada tabloları güncelleştirmek için nasıl kullanıldığını tanımlayan kural ayarlarını içerdiği anlamına gelir.  

4. Tasarımcı'ya tıklayın.
5. Ağaçta, "model: Veri modeli 1099 Ödemeleri modeli" öğesini genişletin.
6. Ağaçta, "model: Veri modeli 1099 Ödemeleri modeli\Hareketler: Kayıt listesi" öğesini genişletin.

    Tasarlanan modelin, burada bir veri kaynağı öğesi olarak sunulduğuna dikkat edin. Çalışma zamanında, harici dosyadan içeri aktarılan verileri içerir. İçeri aktarılan satıcı hesabı hareketinin sistemde mevcut olup olmadığı, içeri aktarma ülke ve il kodlarının birleşiminin bulunup bulunmaması da dahil olmak üzere içeri aktarılan verilerin mevcut uygulamanın verileriyle uyumlu olmasını sağlamak üzere birkaç tablo, veri kaynak öğesi olarak eklenmiştir.  

7. Ağaçta, "model: Veri modeli 1099 Ödemeleri modeli\Hareketler: Kayıt listesi\\$failed: Hesaplanan alan = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean" öğesini seçin.
8. Düzenle öğesine tıklayın.
9. Formülü düzenle'ye tıklayın.

    Tek bir içeri aktarılan hareket için en az bir doğrulama başarısız olduğunda, bu hareket, veri kaynağı özniteliği "$failed" tarafından başarısız olarak işaretlenir.  

10. Sayfayı kapatın.
11. İptal'e tıklayın.
12. Ağaçta, "tax1099trans: Tablo 'VendSettlementTax1099' kayıtları= model.Validated" öğesini seçin.
13. Hedefi düzenle'ye tıklayın.

    Bu ER hedefi, içeri aktarılan verilerin uygulama tablolarını nasıl güncelleştireceğini belirtmek için eklendi. Bu durumda, VendSettlementTax1099 veri tablosu seçildi. Kayıt eylemi olarak Ekle seçili olduğundan, içeri aktarılan hareketler VendSettlementTax1099 tablosuna eklenir. Tek model eşlemesinin çeşitli hedefleri içerebileceğine dikkat edin. Bu, içeri aktarılan verilerin aynı anda birden fazla uygulamanın tablolarını güncelleştirmek için kullanılabileceği anlamına gelir. Tablolar, görünümler ve veri varlıkları ER hedefleri olarak kullanılabilir.   

    Eşleme, uygulamada bu eylem için özel olarak tasarlanan (bir düğme veya menü öğesi gibi) bir noktadan çağrılırsa ER hedefi, tümleştirme noktası olarak işaretlenmelidir. Bu örnekte, bu ERTableDestination #VendSettlementTax1099 noktasıdır.  

14. İptal'e tıklayın.
15. Tümünü göster'e tıklayın.
16. Yalnızca eşlenmişleri göster'e tıklayın.
17. Ağaçta, "tax1099trans: Tablo 'VendSettlementTax1099' kayıtları= model.Validated" öğesini genişletin.

    Yalnızca doğrulanan hareketleri içeren veri kaynağı öğesinin oluşturulan hedefe bağlandığına dikkat edin. Uygulamaların verileriyle uyumsuz olanları atlamak için içeri aktarılan hareketlere filtre uygulayabilirsiniz.  

18. Ağaçta, "failed: Tablo 'VendSettlementTax1099Entity' kayıtları= model.Failed" öğesini seçin.
19. Doğrulamalar sekmesine tıklayın.

    Bu model eşlemesi, mevcut uygulama verilerinden içeri aktarılan verilerin kesinliğini doğrulamak için kullanıcı tanımlı mantık içerebilir. Örneğin; mevcut ayara göre içeri aktarılan dosyada sistemde bulunmayan bir satıcı hesabı olan her hareket için, kullanıcıyı bilgilendiren ve yanlış satıcı hesap kodunu belirten bir uyarı iletisi oluşturulur.  

    İçeri aktarma işlemenin devam etmesi veya durdurulması gerektiğini ve zaten gerçekleştirilmiş eklemelerin/güncelleştirmelerin saklanabileceğini veya geri alınabileceğini belirlemek üzere her doğrulama için Doğrulama sonrası eylem seçeneğinin kullanılabileceğine dikkat edin.  

20. Yalnızca eşlenmişleri göster'e tıklayın.
21. Tümünü göster'e tıklayın.
22. Sayfayı kapatın.

    Tasarlanan biçim ve model eşlemelerini test etmek için bu model eşlemesini yürütün. 1099entries.xml dosyasını kullanın. Seçili dosyadaki veriler, sisteme içeri aktarılır.  

23. Çalıştır öğesine tıklayın.

    İletişim kutusunun, içeri aktarılan dosyayı ayrıştırmak ve ardından da verileri veri modeline bağlamak için kullanılması gereken biçim eşlemesi hakkında ek sorular içermediğini unutmayın. Bunun nedeni şu anda bu modeli kullanan, veri içeri aktarmayı desteklemek için tasarlanmış olarak işaretli tek bir biçim bulunmasıdır.  
    
    El ile girilmiş veya içeri aktarılmış olabilecek diğer hareketlerden içeri aktarılan hareketleri ayırt etmek için fiş kodunu tanımlayın.  

24. Fiş kodunu girin alanına, "IMPORT-001" yazın.

    "1099entries.xml" dosyasını almak için Gözat'a tıklayın.  

25. Tamam'a tıklayın.

    Oluşturulan uyarılar listesi; yanlış satıcı hesapları, yanlış vergi 1099 kutusu kodu, eksik ülke kodları vs. hakkında bilgileri sağlar. Bu uyarılar listesini, yürütme XML dosyasında bulunan içerikle karşılaştırın.  

26. Sayfayı kapatın.
27. Sayfayı kapatın.
28. Sayfayı kapatın.
29. Sayfayı kapatın.
30. Borç hesapları > Periyodik görevler > Vergi 1099 > 1099 formlarına ilişkin satıcı kapatması'na gidin.

    Bu form, içeri aktarılan hareketlere göre oluşturulan Tax1099Summary tablosundaki toplam hareketleri gösterir.  

31. Form tarihi alanında, tarihi '01-01-2000' olarak ayarlayın.
32. El ile 1099 hareket'e tıklayın.

    Bu form, el ile eklenen ve içeri aktardığımız hareketlerin listesini içerir.  

33. Fiş sütunu filtresini açın.
34. "Fiş" alanına "ile başlar" filtre işlecini kullanarak "IMPORT-001" filtre değerini yazın.

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Model ve biçim eşlemeleri arasındaki ilişkiyi gözden geçirme
1. Sayfayı kapatın.
2. Sayfayı kapatın.
3. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
4. Raporlama konfigürasyonları'na tıklayın.
5. Ağaçta, "1099 Ödemeleri modeli" öğesini seçin.

    Aynı verilerin bir .TXT dosya biçiminden içeri aktarılmasını desteklemek istediğinizi varsayalım.   

6. İletişim kutusunu açmak için Yapılandırma oluştur'a tıklayın. 
7. Yeni alanına, "1099 Ödemeler modeli veri modelini temel alan biçim" yazın.
8. Ad alanına, "TXT dosyasından veri içe aktarma' yazın.
9. Veri içe aktarmayı destekler alanında Evet'i seçin.
10. Konfigürasyon oluştur'u tıklatın.
11. Tasarımcı'yı tıklatın.
12. Biçimi modelle eşle'ye tıklayın.
13. Yeni'ye tıklayın.
14. Tanım alanına bir değer girin veya buradan bir değer seçin.

    "1099-MISC" seçeneğini belirleyin.  

15. Ad alanına, "TXT dosyasından veri içe aktarma' yazın.
16. Açıklama alanına, "TXT dosyasından veri içe aktarma" yazın.
17. Kaydet'e tıklayın.
18. Sayfayı kapatın.
19. Sayfayı kapatın.
20. Düzenle'ye tıklayın.

    "KB 4012871 Ayrı yapılandırmalarda GER model eşlemeleri desteği ve bunları farklı Dynamics 365 Finance sürümlerinde dağıtmak için farklı ön koşulları belirleyebilme" düzeltmesini ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871))yüklediyseniz girilen biçim yapılandırması için bir sonraki adım olan "'Model eşleme için varsayılan' bayrağını açma" adımını yürütün. Aksi durumda, bir sonraki adımı atlayın.  

21. Model eşleme için varsayılan alanında Evet'i seçin.
22. Ağaçta, "1099 Ödemeleri modeli" öğesini seçin.
23. Tasarımcı'ya tıklayın.
24. Modeli veri kaynağına eşle'yi tıklayın.
25. Çalıştır öğesine tıklayın.

    "KB 4012871 Ayrı yapılandırmalarda GER model eşlemeleri desteği ve bunları farklı sürümlerde dağıtmak için farklı önkoşulları belirleyebilme" ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)) düzeltmesini yüklediyseniz arama alanında tercih edilen model eşlemesini seçin. Düzeltmeyi henüz yüklemediyseniz, eşleme varsayılan biçim yapılandırmasının tanımı tarafından zaten seçildiğinden bir sonraki adımı atlayın.  
    
    KB 4012871 düzeltmesini yüklemediyseniz iletişim kutusunun içeri aktarmakta olduğunuz dosyayı ayrıştırmak için kullanılan ek bir model eşleme sorusu içerdiğine dikkat edin. Ardından veriler, iletişim kutusundan veri modeline taşınır. Şu anda, içe aktarmayı planladığınız dosya türüne bağlı olarak hangi biçim eşlemesinin kullanılması gerektiğini seçebilirsiniz.  
    
    Bu model eşlemesini eylem için özel olarak tasarlanan bir uygulama noktasından çağırmayı planlıyorsanız ER hedefinin ve biçim eşlemesinin, tümleştirmenin bir parçası olarak işaretlenmesi gerekir.  

26. İptal'e tıklayın.
27. Sayfayı kapatın.
28. Sayfayı kapatın.

