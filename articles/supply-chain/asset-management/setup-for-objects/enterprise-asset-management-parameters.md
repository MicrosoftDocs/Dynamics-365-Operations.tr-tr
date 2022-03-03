---
title: Kıymet Yönetimi parametreleri
description: Kıymet Yönetimi'nde kıymetler, iş emirleri ve iş emri zamanlamasıyla ilgili genel parametrelerin ayarlanması gerekir.
author: johanhoffmann
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1659fd3b4c173ffe09f245631309d329bba5b1bd
ms.sourcegitcommit: f2a78e0d7d461ca843ac2f9abff7690275db9196
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/09/2022
ms.locfileid: "8105501"
---
# <a name="asset-management-parameters"></a>Kıymet Yönetimi parametreleri

[!include [banner](../../includes/banner.md)]

Kıymet Yönetimi'nde kıymetler, iş emirleri ve iş emri zamanlamasıyla ilgili genel parametrelerin ayarlanması gerekir. Bu konuda bu öğelerin nasıl ayarlanacağı açıklanmaktadır. Formu açmak için **Kıymet yönetimi** > **Kurulum** > **Kıymet yönetimi parametreleri**'ni seçin.

> [!NOTE]
> Kıymet yönetimi özelliklerini sınamak için demo verileri içeren bir sistem kurmak istiyorsanız, talimatlar için bkz. [Demo ortamı oluştur](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).

## <a name="the-assets-tab"></a>Kıymetler sekmesi

**Kıymetler** sekmesi aşağıdaki ayarları sağlar:

- **Varsayılan işlem yapılacak yerleşim** yeni kıymetler oluşturduğunuzda kıymetlerde otomatik olarak seçilen standart işlem yapılacak yerleşimdir.  
- **Standart takvim** alanında kıymet üzerinde hiçbir kaynak seçilmediyse kıymet KPI'larını hesaplamada kullanılacak takvimi seçin.  
- **Görünüm** alanında **Kıymet görünümü** formunu açtığınızda gösterilen standart görünümü seçin (**Kıymet yönetimi** > **Ortak** > **Kıymetler** > **Kıymet görünümü**).
- **Varsayılan talep türü** yeni bir talep oluşturduğunuzda otomatik olarak seçilen standart bakım talebi türüdür.  
- İş türlerine ilişkin tahminler **Tahmin projesi** alanında seçili olan projede depolanır. Her iş türü için tahmin projesinde yeni bir etkinlik otomatik olarak oluşturulur. İş türüne ilişkin tahminler daha sonra tahmin projesinde kaydedilir.  
- **Model** alanında, iş türü ve iş emri tahminlerinde kullanılan tahmin modelini seçin.

## <a name="the-work-orders-tab"></a>İş emirleri sekmesi

**İş emirleri** sekmesi aşağıdaki ayarları sağlar:

- **Varsayılan iş emri türü** bir iş emri oluştururken standart ayarları tanımlar.  
- **Önleyici iş emri türü** bakım planlarından iş emri oluştururken kullanılan iş emri türünü tanımlar. Bu alan boş bırakılırsa **Varsayılan iş emri türü** alanındaki iş emri türü kullanılır.  
- **İlgili iş emri maskesi** alanında bir iş emriyle ilgili olabilecek iş emirlerinin maksimum sayısını tanımlayın. Örneğin, ## ile ilgili 99'a kadar iş emriniz olabilir. Bir maskeyi burada açıklandığı şekilde tanımlarsanız ilgili iş emirleri [bir iş emrinin ilgili olduğu iş emrinin iş emri kimliği]-01, -02, -03 vs. olarak numaralandırılır. Bu alanda bir maske tanımlamazsanız ilgili bir iş emri sonraki sıralı iş emri kimliğini alır.  
- Bakım taleplerinde kayıtlı hataları ilgili iş emirlerine otomatik olarak kopyalamak istiyorsanız **Hataları kopyala** için **Evet** seçeneğini belirleyin. 
- Tüm ilgili iş emri işleri aynı işlem yapılacak yerleşime başvuruyorsa **Düzey** alanında iş emrine otomatik olarak eklenen işlem yapılacak yerleşim düzeyini tanımlayın. İş emri işlerinin tümü tanımlanan düzeyde aynı işlem yapılacak yerleşime başvurmuyorsa iş emrinde **İşlem yapılacak yerleşim** alanı boş bırakılır. Örneğin, Bu alana "1" sayısını yazarsanız bu bir işlem yapılacak yerleşim yapısının en üst düzeyi olur. Bu alana "0" sayısını yazarsanız belirli bir işlem yapılacak yerleşim tanımlamamış olursunuz ve işlem yapılacak yerleşimin iş emrine eklenebilmesi için yalnızca bir iş emrindeki tüm iş emri işlerinin aynı işlem yapılacak yerleşimle ilgili olması gerekir.  
- Bir iş emrindeki tüketimi deftere naklederken kullanılan günlükler **Saat**, **Madde** ve **Gider** alanlarının **Genel** hızlı sekmesinden seçilebilir.  
- **Ürün dili kaynağı** alanında Kıymet yönetimi raporlarında ürün adları için kullanılacak dili seçin. Şirket hesabında dil ayarını veya oturum açmış olan kullanıcı için dil ayarını seçebilirsiniz.  
- İş türü varsayılanlarında, bakım planlarında ve bakım sıralarındaki değişiklikleri otomatik olarak güncelleştirmek istiyorsanız **Gerçek zamanlı güncelleştirme** geçiş düğmesinde **Evet** seçeneğini belirleyin.
  - **Hayır** seçeneğini belirlerseniz iş türü varsayılanları, bakım planları ve bakım sıralarında yapılan değişiklikler Kıymet Yönetimi'nde otomatik olarak güncelleştirilmez.
  - Bakım planları veya bakım sıraları üzerinde pek çok kıymet veya işlem yapılacak yerleşim ayarı ya da pek çok bakım planı veya sırası gibi çok fazla miktarda veriyi eşitliyorsanız **Hayır** seçeneğini belirleyin.  
  - İş türü varsayılanları veya bakım planları ya da bakım sıralarında değişiklik yaparsanız ve gerçek zamanlı güncelleştirme için **Hayır** seçeneğini belirlediyseniz değişikliklerin aşağıdakileri etkilemesi durumunda bir uyarı gösterilmeyebilir:
    - Bakım planları veya sıralarında ayarlanan işlem yapılacak yerleşimler  
    - Bakım planları veya sıralarında ayarlanan nesneler  
    - Bakım planları ayarları  
    - Bakım sıraları ayarları  
- **Kategori** hızlı sekmesinde iş emirlerinde tüketimle ilgili varsayılan kategoriler tanımlanabilir.  

## <a name="the-work-order-scheduling-tab"></a>İş emri zamanlaması sekmesi

**İş emri zamanlaması** sekmesi, **Genel** hızlı sekmesinde aşağıdaki ayarları sağlar.

- **Zamanlama zaman dilimi** iş emri işlerinin planlanması boyunca iş emrinin başlangıç tarihinden itibaren hesaplanan süreyi gün cinsinden tanımlar.  
- **Master plan** **Kuruluş yönetimi** modülündeki kaynaklarla ilgilidir. Bu alanda bir master plan seçerseniz iş emirleriyle ilgili kapasite rezervasyonlarını **Kapasite rezervasyonları** içinde görebilirsiniz (**Kuruluş yönetimi** > **Kaynaklar** > **Kaynaklar** > kaynak seç > **Kaynak** sekmesi > **Kapasite rezervasyonları** düğmesi). Bu alanı boş bırakırsanız iş emirleriyle ilgili kapasite yükünü **Kapasite yükü** içinde görebilirsiniz (**Kuruluş yönetimi** \> **Kaynaklar** \> **Kaynaklar** \> kaynak seç \> **Kaynak** sekmesi \> **Kapasite yükü** düğmesi).  

>[!NOTE]
>**Varlık yönetimi** modülünde bir master plan kullanılıp kullanılmayacağına ilişkin seçim ve kapasite rezervasyonlarına veya kapasite yüküne genel bakış almak için kullanılan ilgili form standart ayardır. **Master plan** alanındaki ayarınıza bağlı olarak kapasite bilgilerine **Kuruluş yönetimi** modülündeki **Kapasite rezervasyonları** veya **Kapasite yükü** öğesinden ulaşabilirsiniz. Kapasite rezervasyonlarının iki görünümde de gösterildiği bir ayar oluşturmak mümkün değildir.  

Aşağıdaki listesinde açıklanan alanların tümü iş emri planlaması sırasında iş emri önceliğini hesaplamak için kullanılan, hesaplanan derecelendirme puanlarıyla ilgilidir.

- **Öncelik**: **Kritiklik** ve **Başlangıç tarihi** alanlarındaki derecelendirme puanıyla birlikte hesaplanan derecelendirme puanıdır. Bu alandaki sayı iş emrinin **Öncelik** alanındaki sayıya bölünür. Örneğin bu alana "5,00" değeri girilirse ve iş emrinin önceliği "20" ise, önceliğin derecelendirme puanı 0,25'tir.  
- **Kritiklik**: **Öncelik** ve **Başlangıç tarihi** alanlarındaki derecelendirme puanıyla birlikte hesaplanan derecelendirme puanıdır. Bu alandaki sayı iş emrinin **Kritiklik** alanındaki sayıyla çarpılır. Örneğin bu alana "10,00" değeri girilirse ve iş emrinin kritikliği "5" ise, kritikliğin derecelendirme puanı 50'dir.  
- **Başlangıç tarihi**: **Öncelik** ve **Kritiklik** alanlarındaki derecelendirme puanıyla birlikte hesaplanan derecelendirme puanıdır. Bu alan günlük puanı negatif değer olarak gösterir ve iş emrindeki **Beklenen başlangıç** alanıyla karşılaştırılır. Örneğin bu alana "10,00" değeri girilirse ve iş emrinin beklenen başlangıç tarihi bugünden itibaren üç günse derecelendirme sonucu eksi 30,00'dur. Yukarıda açıklanan **Öncelik** ve **Kritiklik** alanlarındaki örneklerin 0,25 ve 50 sonuçları eklendiğinde toplam artı 20,25 elde edilir. Bu sayı iş emri planlaması boyunca elde edilen diğer tüm iş emri derecelendirme puanlarıyla karşılaştırılır ve en yüksek derecelendirme puanları önce planlanır.  
- **Sorumlu çalışan**: **Sorumlu çalışan**, **Tercih edilen çalışan**, **Tercih edilen çalışan grubu**, **Kıymet yerleşimi** ve **Başlangıç tarihi** derecelendirme puanı değerleriyle birlikte hesaplanan derecelendirme puanıdır. Bu alana "50,00" değeri girilirse ve bir iş emrinde sorumlu çalışan seçilmişse çalışan iş emri planlaması boyunca genel çalışan hesaplamasından 50 puan alır.  
- **Sorumlu çalışan grubu**: **Sorumlu çalışan**, **Tercih edilen çalışan**, **Tercih edilen çalışan**, **Kıymet yerleşimi** ve **Başlangıç tarihi** derecelendirme puanı değerleriyle birlikte hesaplanan derecelendirme puanıdır. Bu alana "50,00" değeri girilirse ve bir iş emrinde sorumlu çalışan seçilmişse çalışan iş emri planlaması boyunca genel çalışan hesaplamasından 50 puan alır.  
- **Sorumlu olanla sınırla** - Bu, iş emri planlamasında kullanılabilen çalışanların sayısını sınırlar. Tüm çalışanlar için bir puan hesaplamak isterseniz sorumlu çalışan veya sorumlu çalışan grubunun parçası olarak ayarlanmalarından bağımsız olarak, **Hayır** seçeneğini belirleyin. İş emrinde sorumlu çalışan olarak ayarlanan ve/veya iş emrinde seçili sorumlu iş grubuna dahil edilmiş çalışanlar için puan hesaplamak isterseniz **Evet** seçeneğini belirleyin.  
- **Tercih edilen çalışan**: **Sorumlu çalışan**, **Tercih edilen çalışan**, **Tercih edilen çalışan grubu**, **Kıymet yerleşimi** ve **Başlangıç tarihi** derecelendirme puanı değerleriyle birlikte hesaplanan derecelendirme puanıdır. Dört derecelendirme puanı hesaplanır ve bu puanlar, iş emri planlaması sırasında hangi çalışanın hangi iş emrine atanacağını belirlemek için kullanılan puanı elde etmek üzere toplanır. Bu alana "10,00" değeri girilirse ve bir iş emrinde tercih edilen çalışan seçilmişse bu çalışan iş emri planlaması boyunca genel çalışan hesaplamasından 10 puan alır.  
- **Tercih edilen çalışan grubu**: **Sorumlu çalışan**, **Tercih edilen çalışan**, **Tercih edilen çalışan grubu**, **Kıymet yerleşimi** ve **Başlangıç tarihi** derecelendirme puanı değerleriyle birlikte hesaplanan derecelendirme puanıdır. Bu alana "10,00" değeri girilirse ve bir çalışan iş emrinde seçili tercih edilen çalışan grubuna atanmışsa, bu çalışan iş emri planlaması boyunca genel çalışan hesaplamasından 10 puan alır.  
- **Tercih edilene sınırla** - Bu, iş emri planlamasında kullanılabilen çalışanların sayısını sınırlar. Tüm çalışanlar için bir puan hesaplamak isterseniz tercih edilen çalışan veya tercih edilen çalışan grubunun parçası olarak ayarlanmış olsa da olmasa da **Hayır** seçeneğini belirleyin. Yalnızca tercih edilen çalışanlar ayarlanmış ve/veya tercih edilen çalışan grubuna dahil edilmiş çalışanlar için bir puan hesaplamak isterseniz **Evet** seçeneğini belirleyin.  
- **Yerleşim**: **Sorumlu çalışan**, **Tercih edilen çalışan**, **Tercih edilen çalışan grubu**, **Kıymet yerleşimi** ve **Başlangıç tarihi** derecelendirme puanı değerleriyle birlikte hesaplanan derecelendirme puanıdır. Bu alana "3.000,00" değeri girilirse, çalışan bir işin planlanacağı kıymetle aynı fabrika veya tesiste bulunuyorsa hesaplamada bu çalışan 3.000 puan alır.  
  - Şirketiniz işlem yapılacak yerleşimleri kullanıyorsa çalışanlar kıymetle ilgili işlem yapılacak yerleşimde bulunuyorsa tam puan alırlar. Kıymetin işlem yapılacak yerleşiminin üst kıymeti varsa bu işlem yapılacak yerleşimdeki çalışanlar 1/2 puan alır. Bu yerleşimin bir üst öğesi varsa bu yerleşimdeki çalışanlar 1/3 puan alır. Bu yerleşimin bir üst öğesi varsa bu yerleşimdeki çalışanlar 1/4 puan alır ve hesaplama bu şekilde devam eder.  
  - Şirketiniz kıymet yerleşimini kullanıyorsa yerleşim puanlarını hesaplamak için yerleşim, alan ve bölge kullanılır. Bu ayarın kullanılmasını önermeyiz. Çalışanlar kıymetle ilgili yerleşim ve alan ve bölgede bulunuyorsa tam puan alır. Çalışan yerleşimi yalnızca yerleşim ve alanla eşleşiyorsa bu çalışanın derecelendirme puanı tam puanın 2/3'ü olur. Çalışan yerleşimi yalnızca yerleşimle eşleşiyorsa bu çalışanın derecelendirme puanı tam puanın 1/3'ü olur.  
- **Konuma sınırla** - Bu, iş emri planlamasında kullanılabilen çalışanların sayısını sınırlar. Tüm işlem yapılacak yerleşimlerde tüm çalışanlar için bir puan hesaplamak isterseniz **Hayır** seçeneğini belirleyin. Yalnızca iş emrinin işlem yapılacak yerleşimiyle ilişkili çalışanlar için puan hesaplamak isterseniz **Evet** seçeneğini belirleyin.

>[!NOTE]
>Üç adet "... ile sınırla" çalışanlar için hesaplanan puanların sayısını sınırlayarak iş emri planlamasının hızını artırmak amacıyla eklenmiştir.

**Çalışanın başlangıç tarihi**: **Sorumlu çalışan**, **Tercih edilen çalışan**, **Tercih edilen çalışan grubu**, **Kıymet yerleşimi** ve **Başlangıç tarihi** derecelendirme puanı değerleriyle birlikte hesaplanan derecelendirme puanıdır. Bu alan günlük puanı negatif değer olarak gösterir ve iş emrindeki **Beklenen başlangıç** alanıyla karşılaştırılır. Bu alana "10,00" değeri girilirse ve iş emrinin beklenen başlangıç tarihi yarınsa derecelendirme sonucu eksi 10,00'dur.

  - Planlanacak iş emrinde sorumlu çalışan ve sorumlu çalışan grubu seçilmediği varsayımıyla, yukarıdaki **Tercih edilen çalışan**, **Tercih edilen çalışan grubu**, **Kıymet yerleşimi** ve **Başlangıç tarihi** alanlarına verilen örneklerin derecelendirme puanı değerlerini ekleyip çıkardığınızda toplam 3.010,00 elde edersiniz. Bu, tercih edilen çalışan seçilen ve iş emrinde tercih edilen çalışan grubuna dahil edilen çalışanın yüksek puan alacağı ve çalışanın planlanması gereken işe ilişkin kıymetle aynı tesiste bulunduğu anlamına gelir. Genel olarak da iş emri planlamasında işi tamamlamak için söz konusu çalışanın seçilme olasılığının yüksek olduğu anlamına gelir.  
  - Yukarıdaki sekiz alandan birine "0,00" değeri girilirse bu derecelendirme puanı iş emri planlaması sırasında kullanılmaz.  

## <a name="the-document-types-tab"></a>Belge türleri sekmesi

İş emri raporuyla ilgili ekleri yazdırmak için kullanılabilir olması gereken belge türlerini seçin. Bu işlem **Kullanılabilir** bölümünde bir belge türünü ve ardından ![ileri ok.](media/15-setup-for-objects.png) düğmesi seçilerek yapılır. Seçili belge türünü kaldırmak isterseniz **Seçili** bölümünde belge türünü seçin ve ![geri ok](media/16-setup-for-objects.png) düğmesine tıklayın.

## <a name="the-number-sequences-tab"></a>Numara serileri sekmesi

Gereken numara serilerini bu bölümde seçin. Kıymetler için iki numara sırası vardır: Biri el ile oluşturulan kıymetler ve diğeri de bekleyen kıymetler aracılığıyla oluşturulan kıymetler içindir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
