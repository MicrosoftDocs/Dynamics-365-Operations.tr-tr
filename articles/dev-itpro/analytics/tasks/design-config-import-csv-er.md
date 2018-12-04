--- 
title: "CSV dosyalarından veri almak için ER yapılandırmaları tasarlama"
description: "Dynamics 365 for Finance and Operations'a CSV biçimindeki bir dış dosyadan veri aktarmak üzere Elektronik raporlama (ER) yapılandırmalarını tasarlamak için bu yordamı kullanın."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8d3ea3d797de154979eae112658cf05d1914feeb
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-configurations-to-import-data-from-external-csv-files"></a>CSV dosyalarından veri almak için ER yapılandırmaları tasarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dynamics 365 for Finance and Operations'a CSV biçimindeki bir dış dosyadan veri aktarmak üzere Elektronik raporlama (ER) yapılandırmalarını tasarlamak için bu yordamı kullanın. Bu yordamda, Litware, Inc. adlı örnek şirket için gerekli ER yapılandırmalarını oluşturacaksınız. Bu adımları tamamlamak için ilk olarak "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir. 

Bu yordam, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur. Bu adımlar USMF veri kümesi kullanılarak tamamlanabilir. 

Şu dosyaları yerel olarak indirmeniz ve kaydetmeniz gerekir: (https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Dynamics 365 for Finance and Operations'da tablolara XML, TXT veya CSV biçimindeki harici dosyaları içe aktarmak için bir işlem yapılandırabilirsiniz. İlk olarak iş açısından, içe aktarılan verileri temsil etmek üzere bir soyut veri modeli oluşturmanız gerekir. Bunun için bir ER veri modeli yapılandırması oluşturulur. Sonra, dosyadaki verileri soyut veri modeliyle bağlamanın bir yolu olarak tasarlanan veri modeliyle eşleşen içe aktarılmış dosya yapısını tanımlayın. Bunun için bir ER biçim yapılandırması oluşturulur. Ardından, ER veri modeli yapılandırmasının içe aktarılan dosyadaki verilerin ve soyut veri modelindeki kalıcı verilerin uygulama tablolarını veya veri varlığını güncelleştirmek için nasıl kullanıldığını açıklayan yeni bir model eşlemesi ile genişletilmesi gerekir.  
    * Aşağıdaki adımlar harici olarak izlenen satıcı hareketlerinin daha sonra 1099 formlarındaki satıcı kapatmaları için kullanılmak üzere harici bir CSV dosyasından nasıl içe aktarılacağını göstermektedir.   
    * Örnek şirket Litware, Inc. için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlendiğini doğrulayın. Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.  
2. Raporlama konfigürasyonları'na tıklayın.
3. '1099 Ödemeleri modeli' filtresini uygulayın. ”ER Elektronik raporlama için harici bir dosyadan verileri içe aktarmak üzere gerekli yapılandırmaları oluşturma” yordamını tamamladıysanız ve ‘1099 Ödemeleri model’ yapılandırması yapılandırma ağacında varsa, sonraki alt görevde bu adımların tümünü atlayın.   

## <a name="add-a-new-er-model-configuration"></a>Yeni bir ER model yapılandırması ekleme
1. Veri içeri aktarmayı desteklemek için yeni bir model oluşturmak yerine, daha önce indirdiğiniz 1099model.xml dosyasını yükleyin. Bu dosya, satıcıların hareketlerinin özel veri modelini içerir. Bu veri modeli gerekli veri bileşenleriyle zaten eşlendi.  
2. Değiştir seçeneğine tıklayın.
3. XML dosyasından yükle'ye tıklayın.
4. Gözat düğmesine tıklayın ve önceden indirdiğiniz 1099model.xml dosyasına gidin.  
5. Tamam'a tıklayın.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Veri içe aktarmayı destekleyen yeni bir ER biçim yapılandırması ekleme
1. Ağaçta, "1099 Ödemeleri modeli" öğesini seçin.
2. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
3. Yeni alanına, "1099 Ödemeler modeli veri modelini temel alan biçim" yazın.
4. Veri içe aktarmayı destekler alanında Evet'i seçin.
5. Bu sayfayı kapatmak için ESC tuşuna basın.
    * Veri içeri aktarma işlemini desteklemek için yeni bir ER biçimi oluşturmak yerine daha önce indirdiğiniz 1099formatcsv.xml dosyasını yükleyin. Bu dosya, gelen CSV dosyasının yapısını tanımlayan gerekli ER biçimini ve bu yapının satıcı hareketlerinin veri modeliyle eşleşmesini içerir.   
6. Değiştir seçeneğine tıklayın.
7. XML dosyasından yükle'ye tıklayın.
    * Gözat düğmesine tıklayın ve önceden indirdiğiniz 1099formatcsv.xml dosyasına gidin.  
8. Tamam'a tıklayın.
9. Ağaçta, "1099 Ödemeleri modeli" öğesini genişletin.
10. Ağaçta, '1099 Ödeme modeli\Satıcı hareketlerini içe aktarmak için (CSV)' öğesini seçin.

## <a name="review-format-settings"></a>Biçim ayarlarını gözden geçirme
1. Tasarımcı'yı tıklatın.
2. Genişlet/daralt'a tıklayın.
3. 'Ayrıntıları göster' öğesini açın.
    * Tasarlanan biçim, harici dosyanın CSV biçimindeki beklenen yapısını gösterir.  
4. Ağaçta, 'Gelen: Dosya\Kök: Sıra' öğesini seçin.
    * SIRA türündeki Kök öğe için, ‘Yeni satır - Windows (CR LF)’ seçeneği ‘Özel karakterler’ alanında seçilmiştir. Bu ayarı temel alarak, ayrıştırma dosyasındaki her satır ayrı bir kayıt olarak ele alınmalıdır.   
5. Ağaçta, 'Gelen: Dosya\Kök: Sıra\Satır: Sıra 1..*' öğesini seçin.
    * SIRA türünün Kök\Satır öğesi için, ‘Çok katlılık’ alanında ‘Bir çok’ seçeneği seçilmiştir. Bu ayara bağlı olarak, ayrıştırma dosyasında en az bir satır sunulacaktır.   
6. Ağaçta, 'Gelen: Dosya\Kök: Sıra\Satır: Sıra 1..* \Türler: Servis Talebi' öğesini seçin.
    * SERVİS TALEBİ türünün Kök\Satır\Türler öğesinin Kök\Satır sırasının iç içe geçmiş öğesi olarak eklenmiş olduğuna dikkat edin. Bu SERVİS TALEBİ öğesi 3 iç içe geçmiş sıra öğesi içerdiğinden, bu ayar ayrıştırma dosyasında 3 farklı türde satır göreceğimizi varsayar.   
7. Ağaçta, 'Gelen: Dosya\Kök: Sıra\Satır: Sıra 1..* \Türler: Servis Talebi\Başlık: Sıra 1..1' öğesini seçin.
    * SIRA türünün Kök\Satır\Türler\Başlık öğesi iç içe geçmiş DİZE öğesi içerir; bunun değeri sabit dize değeri olarak tanımlanmıştır. Bu sıra ayrıştırma dosyasının başlık satırını ayrıştıracaktır.   
8. Ağaçta, 'Gelen: Dosya\Kök: Sıra\Satır: Sıra 1..* \Türler: Servis Talebi\Kayıt: Sıra 1..1 (,)' öğesini seçin.
    * SIRA türünün Kök\Satır\Türler\Kayıt öğesi hareket satırlarını ayrıştıracak şekilde yapılandırılmıştır. 'Özel ayırıcı' karakter seçeneğinin virgül olarak yapılandırıldığını unutmayın. Bu, ayrıştırma dosyasında bu satır türü için alan ayırıcı olarak virgül kullanılacağı anlamına gelmektedir.   
    * Kök\Satır\Türler\Kayıt öğesi için hareket satırlarını ayrı alanlar olarak ayrıştırmak üzere farklı veri türlerinde çeşitli iç içe geçmiş öğelerin eklendiğine dikkat edin. 'Teklif uygulama' seçeneğinin 'Hiçbiri' olarak yapılandırılmış olduğunu unutmayın. Bu, ayrıştırma dosyasında bu türdeki tüm alanların iliştirilmiş hiçbir karaktere sahip olmadığının kabul edileceği anlamına gelir.   
9. Ağaçta, 'Gelen: Dosya\Kök: Sıra\Satır: Sıra 1..* \Türler: Servis Talebi\Kayıt: Sıra 1..1 (,)\TransactionDate: DateTime' öğesini seçin.
    * Örneğin, DATETIME türünün Kök\Satır\Türler\Kayıt\TransactionDate öğesinin hareket tarihi ve saati değerini ayrıştırma dosyasından 'A/g/yyyy' biçiminde alacak şekilde yapılandırılmıştır.   
10. Ağaçta, 'Gelen: Dosya\Kök: Sıra\Satır: Sıra 1..* \Türler: Servis Talebi\Kayıt: Sıra 1..1 (,)\CountryCode: Dize 0..1' öğesini seçin.
    * DİZE türünün Kök\Satır\Türler\Kayıt\CountryCode öğesinin 'Çok katlılık' alanında 'Sıfır bir' seçeneği bulunacak şekilde yapılandırıldığına dikkat edin. Bu ayar, ayrıştırma satırındaki CountryCode alanının değerini isteğe bağlı olarak kabul eder.   
11. Ağaçta, 'Gelen: Dosya\Kök: Sıra\Satır: Sıra 1..* \Türler: Servis Talebi\Kayıt: Sıra 1..1 (,)\Açıklama: Sıra 1..1 (,)' öğesini seçin.
    * SIRA türünün Kök\Satır\Türler\Kayıt\Açıklama öğesinin ‘Teklif uygulaması’ alanında 'Tümü' seçeneği ve ‘Teklif işareti’ alanında çift tırnak karakteri olacak şekilde yapılandırıldığına dikkat edin. Bu, ayrıştırma dosyasında bulunan bu türdeki tüm satırlar içeren tüm alanların (iç içe geçmiş öğeler tarafından tanımlanan: DİZE türü metni) çift tırnak karakteri içine alınmış olarak değerlendirileceği anlamına gelir.  
12. Ağaçta, 'Gelen: Dosya\Kök: Sıra\Satır: Sıra 1..* \Türler: Servis Talebi\Ayrıştırılmamış: Sıra 1..1' öğesini seçin.
    * SIRA türünün Kök\Satır\Türler\Ayrıştırılmamış öğesi, hareket satırlarını ana SERVİS TALEBİ öğesi için yukarıda açıklanan yapıyla eşleşmeyen bir yapı için ayrıştırmak üzere yapılandırılmıştır.   

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>Veri modeline biçim eşlemesi ayarını gözden geçirme
1. Biçimi modelle eşle'ye tıklayın.
    * ‘CSV biçimindeki modele eşleme’ model eşlemesi gelen CSV dosyasından veri modeline veri aktarımının veri akışını açıklar.   
2. Tasarımcı'yı tıklatın.
3. Ağaçta, 'biçim' metnini genişletin.
    * Tasarlanan biçimin, burada bir veri kaynağı bileşeni olarak sunulduğuna dikkat edin.  
4. Ağaçta, 'biçim\Gelen: Dosya(Gelen)' öğesini genişletin.
5. Ağaçta, 'biçim\Gelen: Dosya(Gelen)\Kök: Sıra(Kök)' öğesini genişletin.
6. Ağaçta, 'biçim\Gelen: Dosya(Gelen)\Kök: Sıra(Kök)\Satır: Sıra 1..* (Satır)' öğesini genişletin.
7. Ağaçta, 'biçim\Gelen: Dosya(Gelen)\Kök: Sıra(Kök)\Satır: Sıra 1..* (Satır)\Türler: Servis Talebi(Türler)' öğesini genişletin.
8. Ağaçta, 'biçim\Gelen: Dosya(Gelen)\Kök: Sıra(Kök)\Satır: Sıra 1..* (Satır)\Türler: Servis Talebi(Türler)\Kayıt: Sıra 1.. 1(,)(Kayıt)' öğesini genişletin.
9. Ağaçta, 'biçim\Gelen: Dosya(Gelen)\Kök: Sıra(Kök)\Satır: Sıra 1..* (Satır)\Türler: Servis Talebi(Türler)\Kayıt: Sıra 1.. 1(,)(Kayıt)\Veri' öğesini genişletin.
10. Ağaçta, 'biçim\Gelen: Dosya(Gelen)\Kök: Sıra(Kök)\Satır: Sıra 1..* (Satır)\Türler: Servis Talebi(Türler)\Kayıt: Sıra 1.. 1(,)(Kayıt)\Veri\CountryCode: Dize 0.. 1 (CountryCode)' öğesini genişletin.
11. Ağaçta, 'biçim\Gelen: Dosya(Gelen)\Kök: Sıra(Kök)\Satır: Sıra 1..* (Satır)\Türler: Servis Talebi(Türler)\Kayıt: Sıra 1.. 1(,)(Kayıt)\Veri\TransactionDate: DateTime(TransactionDate)' öğesini seçin.
    * TransactionDate ve CountryCode gibi gerekli ve isteğe bağlı biçim öğelerinin önceden tanımlanmış 'biçim' veri kaynağı bileşeninde farklı göründüğünü unutmayın.   
12. Ağaçta 'Hareketler = '$her ikisi'' öğesini genişletin.
    * İçeri aktarılan dosyanın yapısını tanımlayan biçim öğelerinin veri modeli öğelerine bağlı olduğuna dikkat edin. Bu bağlamalara göre, içeri aktarılan CSV dosyasının içeriği, mevcut veri modelinin çalışma zamanında saklanır. CountryRegion öğesinin bağlamasına dikkat edin. Gelen dosyada belirtilmiş bir ülke kodu değeri bulunmayan her hareket öğesi için, veri modelinde varsayılan ülke kodu olarak "ABD" kullanılır.   
13. 'Ayrıntıları göster' öğesini açın.
14. Doğrulamalar sekmesine tıklayın.
15. Ara'ya tıklayın.
16. Bul alanına, 'satıcı' yazın.
17. Sonrakini bul'a tıklayın.
    * Bu biçim eşlemesi, iş açısından ele alınan içeri aktarılan verilerin kesinliğini doğrulamak için kullanıcı tanımlı mantık içerebilir. Örneğin, bu ayar temel alındığında, içe aktarma dosyasındaki herhangi bir satır için ne başlık satırı ne de hareket satırı yapısıyla eşleşmeyen yapı için, Bilgi günlüğünde kullanıcıyı bu durum hakkında bilgilendiren ve dosyadaki hareket sırası numarasını belirten bir uyarı iletisi yapılandırılacaktır.   
18. Sayfayı kapatın.

## <a name="run-the-format-mapping"></a>Biçim eşlemeyi çalıştırma
Sınama amacıyla, daha önce yüklediğiniz 1099entriescsv.csv dosyasını kullanarak biçim eşlemesi yürütün. Oluşturulan çıktı, seçilen CSV dosyasından içeri aktarılacak verileri gösterir ve gerçek içe aktarmada özel veri modelini doldurur.   
1. Çalıştır öğesine tıklayın.
    * Gözat düğmesine tıklayın ve önceden indirdiğiniz 1099entriescsv.csv dosyasına gidin.  
2. Tamam'a tıklayın.
    * Kabul edilmeyen satırlarla ilgili uyarı iletilerini not edin. Satır 4 kabul edilmeyen biçimde sunulan bir gelir değerini içerirken satır 7 çift tırnak içine alınmış hareket açıklaması metninini içermemektedir.   
    * Seçili dosyadan içeri aktarılan ve veri modeline taşınan verileri temsil eden XML biçimindeki çıktıyı gözden geçirin. İçe aktarılan CSV dosyasındaki tüm 7 satırın da işlendiğini unutmayın. Alan başlıklarını içeren satır 1 atlandı, 4 hareket doğru şekilde ayrıştırıldı ve 2 hareket geçerli olarak tanındı.   
3. Sayfayı kapatın.
4. Sayfayı kapatın.


