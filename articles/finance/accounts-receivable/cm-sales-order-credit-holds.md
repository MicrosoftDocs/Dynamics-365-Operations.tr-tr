---
title: Satış siparişleri için askıda krediler
description: Bu konuda, bir satış siparişini kredi bekletmeye sokmak için kullanılan kuralların kurulumu açıklanmaktadır.
author: JodiChristiansen
ms.date: 07/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 14cafa69e75d7e8a0f08fb385a8c364c0162da1ec609a4e0b3cad6178ec3f716
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723979"
---
# <a name="credit-holds-for-sales-orders"></a>Satış siparişleri için askıda krediler
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, bir satış siparişini kredi bekletmeye sokmak için kullanılan kuralların kurulumu açıklanmaktadır. Kredi yönetimi durdurma kuralları tek bir müşteriye veya bir müşteri grubuna uygulanabilir. Durdurma kuralları, aşağıdaki durumlara yanıtları tanımlar:

1. Vade sonrası gün sayısı
2. Hesapların durumu
3. Ödeme koşulları
4. Alacak limiti süresi sona erdi
5. Vadesi geçen tutar
6. Satış siparişi tutarı
7. Kullanılabilir kredinin kullanılan bölümü

Ek olarak, bir satış siparişini durduracak ek senaryoları denetleyen iki parametre vardır.

1. Ödeme koşullarında değişiklik
2. Kapatma iskontolarında değişiklik

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Durdurma kurallarını ve hariç tutma kurallarını ayarlama

Bir müşteri bir satış hareketi başlattığında, satış siparişindeki bilgiler, kredinin müşteriye genişletilip genişletilmeyeceği ve satışın ileriye doğru hareket etmesine izin verilip verilmeyeceği kararına kılavuzluk yapan bir engelleme kuralları kümesine göre incelenir. Ayrıca, durdurma kurallarını geçersiz kılacak ve satış siparişinin işlenmesine izin verecek hariç tutmalar da tanımlayabilirsiniz. Durdurma kurallarını ve hariç tutma kurallarını **Kredi yönetimi > Kurulum > Kredi yönetimi kurulumu > Durdurma kuralları** sayfasında ayarlayabilirsiniz.

Sürüm 10.0.21 itibarıyla Kredi yönetimindeki durdurma kuralları, daha fazla esneklik sağlamak için aşağıdaki şekillerde yeniden tasarlandı:

- Genişletilebilirlik istekleri etkinleştirildi, böylece kendi durdurma kurallarınızı oluşturabilirsiniz.
- **Satış siparişini serbest bırak** onay kutusu artık tüm durdurma kuralları için kullanılabilir. Daha önce, bu yalnızca Satış siparişi durdurma kuralı için kullanılabiliyordu. Bu onay kutusu seçilirse hariç tutma kuralı, satış siparişlerini engelleyebilecek diğer kurallar dikkate alınmaksızın satış siparişini serbest bırakır. Bu onay kutusu yalnızca **Hariç tutma** kural türü için kullanılabilir.

### <a name="days-overdue"></a>Aşılan gün sayısı

Vadesi belirli bir gün sayısını geçmiş bir veya daha fazla faturası olan müşteriye durdurma kuralı uygulanıyorsa, **Vade sonrası gün sayısı** sekmesini açın.
1. Bu kuralın **Geçerli** olduğu müşteri aralığını seçin.
   - Kural belirli bir müşteriye uygulanıyorsa **Tablo**'yu seçin.
   - Kural müşteri grubu düzeyinde uygulanıyorsa **Grup**'u seçin. 
   - Kural tüm müşterilere uygulanıyorsa **Tümü**'nü seçin.
2. Aralığı belirtirken, aralıkta kullanılacak **Hesabı/grubu** belirtmeniz gerekir.
   - **Tablo** aralığı için, arama, seçilecek müşterilerin listesini sağlayacaktır. 
   - Kural bir müşteri kredi grubuna uygulanıyorsa, bir **Grup** seçin.
   - Kural tüm müşterilere uygulanıyorsa **Tümü**'nü seçin. 
3. Bir ortak faktör kümesiyle (örneğin, Dun ve Bradstreet derecelendirmesi, sektörde bulundukları yıl sayısı, müşteriniz oldukları süre vb.) gruplanan müşterilere bir kredi yönetimi bekletme uygulama ölçütlerini kullanmak için **Risk grubu**'nu seçin.  
4. Ayarladığınız kuralın türünü seçin. **Durdurma** seçeneği, siparişi durduran bir kural oluşturur. **Hariç tutma** seçeneği, bir siparişi durdurma işleminden bir diğer kuralı hariç tutacak bir kural oluşturur. 
5. Bir **Değer türü** seçin. Varsayılan giriş, sabit bir gün sayısıdır. Bir hariç tutma oluşturuyorsanız, sabit bir gün sayısı veya bir tutar belirtebilirsiniz. 
6. Bir sipariş incelenmek üzere kredi yönetimi bekletme işlemine koyulmadan önce, seçilen durdurma kuralı için izin verilecek **Vadesi sonrası** gün sayısını girin. Vade sonrası gün sayısı, faturanın vadesi geçmiş olarak kabul edilmeden önce sahip olabileceği, ödeme vade tarihinden sonraki gün sayısına eklenen ek mehil gün sayısını temsil eder. Hariç tutma için **Değer türünü** bir tutar olarak belirttiyseniz, o tutar için bir tutar ve para birimi girin.

### <a name="account-status"></a>Hesap durumu

Durdurma kuralı, seçili hesap durumunu taşıyan bir müşteriye uygulanıyorsa **Hesap durumu** sekmesini açın.
1. Ayarladığınız kuralın türünü seçin.  **Durdurma** bir siparişi durduran bir kural oluşturur. **Hariç tutma**, bir siparişi durdurma işleminden bir kuralı hariç tutacak bir kural oluşturur. 
2. Kuralın bir satış siparişini beklemeye almasını veya hariç tutmasını sağlayacak **Hesap durumu**'nu seçin.

### <a name="terms-of-payment"></a>Ödeme koşulları

Durdurma kuralı, seçilen bir ödeme koşuluna uygulanıyorsa, **Ödeme koşulları**'nı seçin.
1. Ayarladığınız kuralın türünü seçin.  **Durdurma** bir siparişi durduran bir kural oluşturur. **Hariç tutma**, bir siparişi durdurma işleminden bir kuralı hariç tutacak bir kural oluşturur. 
2. Kuralın bir satış siparişini beklemeye almasını veya hariç tutmasını sağlayacak **Ödeme koşulları**'nı seçin.

### <a name="credit-limit-expired"></a>Alacak limiti süresi sona erdi

Durdurma kuralı, süresi geçmiş kredi limitli müşterilere uygulanıyorsa **Kredi limiti süresi doldu** sekmesini açın.
1. Bu kuralın **Geçerli** olduğu müşteri aralığını seçin.
   - Kural belirli bir müşteriye uygulanıyorsa **Tablo**'yu seçin.
   - Kural Müşteri grubu düzeyinde uygulanıyorsa **Grup**'u seçin. 
   - Kural tüm müşterilere uygulanıyorsa **Tümü**'nü seçin.
2. Aralığı belirttikten sonra, aralıkta kullanılan **Hesabı/grubu** belirtmeniz gerekir.
   - **Tablo** aralığı için, arama, içinden seçim yapılacak müşteri listesini sağlayacaktır. 
   - Kural bir müşteri kredi yönetimi grubuna uygulanıyorsa, bir **Grup** seçin.
   - Kural tüm müşterilere uygulanıyorsa **Tümü**'nü seçin. 
3. Kredi yönetimi bekletme işlemine koyulacak müşterilerin listesini daha fazla sınırlandırmak için bir **Risk grubu** seçin. 
4. Ayarladığınız kuralın türünü seçin. 
   - Bir siparişi durduran bir kural oluşturmak için **Durdurma**'yı seçin. 
   - Bir siparişi durdurma işleminden bir diğer kuralı hariç tutacak bir kural oluşturmak için **Hariç tutma**'yı seçin. 
5. Bir siparişi kredi yönetimi durdurmaya koymadan önce, seçili durdurma kuralı için, **Kredi limiti süresi dolduktan sonraki gün sayısı**'nı girin. Vade sonrası gün sayısı, kredi limiti süresinin dolduğu gün sayısına eklenen ek mehil süresini temsil eder.

### <a name="overdue-amount"></a>Vadesi geçen tutar

Durdurma kuralı, vadesi geçmiş tutarları olan müşterilere uygulanıyorsa **Vadesi geçen tutar** sekmesini açın.
1. Bu kuralın **Geçerli** olduğu müşteri aralığını seçin.
   - Kural belirli bir müşteriye uygulanıyorsa **Tablo**'yu seçin.
   - Kural Müşteri grubu düzeyinde uygulanıyorsa **Grup**'u seçin. 
   - Kural tüm müşterilere uygulanıyorsa **Tümü**'nü seçin.
2. Aralığı belirttikten sonra, aralıkta kullanılan **Hesabı/grubu** belirtmeniz gerekir.
   - **Tablo** aralığı için, arama, bir müşteri arama işlevi sağlayacaktır. 
   - Kural bir müşteri kredi yönetimi grubuna uygulanıyorsa, bir **Grup** seçin.
   - Kural tüm müşterilere uygulanıyorsa **Tümü**'nü seçin. 
3. Kredi yönetimi bekletme işlemine koyulacak müşterilerin listesini daha fazla sınırlandırmak istiyorsanız bir **Risk grubu** seçin. 
4. Ayarladığınız kuralın türünü seçin. 
   - Bir siparişi durduran bir kural oluşturmak için **Durdurma**'yı seçin. 
   - Bir siparişi durdurma işleminden bir diğer kuralı hariç tutacak bir kural oluşturmak için **Hariç tutma**'yı seçin. 
5. Bir siparişi incelenmek üzere kredi yönetimi durdurmaya koymadan önce, seçili durdurma kuralı için **Vadesi geçen tutar**'ı girin. 
6. Kredi limitinin ne kadarının kullanıldığını test etmek için kullanılacak değer türünü tanımlayan **Değer türü**'nü seçin. Durdurma kuralları ve hariç tutma kuralları yalnızca **Vadesi geçen tutar** için yüzdeye izin verir. Eşik, kredi limitiyle ilgilidir.
7. Bir müşteri kredi yönetimi bekletme işlemine koyulmadan önce, seçili kural için **Kredi limiti eşiği** değerini girin. Bu, değer türünde seçilecek değer türüne göre bir tutar veya yüzde değeri olabilir.
8. Kural, **Vadesi geçen tutarın** ve **Kredi limiti eşiğinin** aşılıp aşılmadığını denetler. 

### <a name="sales-order"></a>Satış siparişi 

Durdurma kuralı satış siparişinin değerine uygulanıyorsa **Satış siparişi**'ni seçin.
1. Bu kuralın **Geçerli** olduğu müşteri aralığını seçin.
   - Kural belirli bir müşteriye uygulanıyorsa **Tablo**'yu seçin.
   - Kural Müşteri grubu düzeyinde uygulanıyorsa **Grup**'u seçin. 
   - Kural tüm müşterilere uygulanıyorsa **Tümü**'nü seçin.
2. Aralığı belirttikten sonra, aralıkta kullanılan **Hesabı/grubu** belirtmeniz gerekir.
   - **Tablo** aralığı için, arama, bir müşteri arama işlevi sağlayacaktır. 
   - Kural bir müşteri kredi yönetimi grubuna uygulanıyorsa, bir **Grup** seçin.
   - Kural tüm müşterilere uygulanıyorsa **Tümü**'nü seçin. 
3. Kredi yönetimi bekletme işlemine koyulacak müşterilerin listesini daha fazla sınırlandırmak istiyorsanız bir **Risk grubu** seçin. 
4. Ayarladığınız kuralın türünü seçin.  
   - Bir siparişi durduran bir kural oluşturmak için **Durdurma**'yı seçin. 
   - Bir siparişi durdurma işleminden bir diğer kuralı hariç tutacak bir kural oluşturmak için **Hariç tutma**'yı seçin. 
5. Bir siparişi kredi yönetimi durdurmaya koymadan önce, seçili durdurma kuralı için **Satış siparişi tutarı**'nı girin. 

### <a name="credit-limit-used"></a>Kullanılan alacak limiti

Durdurma kuralı müşterinin kullanılan kredi limiti tutarına uygulanıyorsa **Kullanılan kredi limiti** ni seçin.
1. Bu kuralın **Geçerli** olduğu müşteri aralığını seçin.
   - Kural belirli bir müşteriye uygulanıyorsa **Tablo**'yu seçin.
   - Kural Müşteri grubu düzeyinde uygulanıyorsa **Grup**'u seçin. 
   - Kural tüm müşterilere uygulanıyorsa **Tümü**'nü seçin.
2. Aralığı belirttikten sonra, aralıkta kullanılan **Hesabı/grubu** belirtmeniz gerekir.
   - **Tablo** aralığı için, arama, bir müşteri arama işlevi sağlayacaktır. 
   - Kural bir müşteri kredi yönetimi grubuna uygulanıyorsa, bir **Grup** seçin.
   - Kural tüm müşterilere uygulanıyorsa **Tümü**'nü seçin. 
3. Kredi yönetimi bekletme işlemine koyulacak müşterilerin listesini daha fazla sınırlandırmak istiyorsanız bir **Risk grubu** seçin. 
4. Ayarladığınız kuralın türünü seçin.
   - Bir siparişi durduran bir kural oluşturmak için **Durdurma**'yı seçin. 
   - Bir siparişi durdurma işleminden bir diğer kuralı hariç tutacak bir kural oluşturmak için **Hariç tutma**'yı seçin. 
5. Satış siparişini durduracak kredi limiti yüzdesini tanımlayan **Eşik kalan değer**'i seçin. Bir siparişin değeri, kullanılan kredi limiti tutarını yüzde değerinin üstüne çıkarırsa sipariş beklemeye alınır. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Bir satış siparişini diğer ölçütlere göre beklemeye alma
  
### <a name="rank-payment-terms"></a>Ödeme koşullarını sırala  

Ödeme koşulları değişince kredi denetim kurallarını zorla uygulayabilirsiniz. Ödeme koşullarına sıra vermeli ve bir sıralama değeri atamalısınız. Siparişteki ödeme koşullarını, eski ödeme koşullarından daha yüksek sıralamada ödeme koşullarına değiştirirseniz sipariş kredi yönetimine gönderilir ve onay gerektirir.

Ödeme koşulları sıralamalarını **Kredi yönetimi > Kurulum > Kredi yönetimi kurulumu > Ödeme koşullarını sırala** sayfasında ayarlayabilirsiniz.

1. **Ödeme koşulları** alanında sıralanacak ödeme koşullarını seçin; bir koşul seçtiğiniz zaman **Açıklama** alanında açıklama görüntülenecektir.
2. **Sıra** alanında koşulun sırasını seçin. Değerlerin hepsi birbirine göreli olduğu için 1, 2, 3 veya 10, 20, 30 kullanabilirsiniz. Ayrıca, ödeme koşullarının yalnızca bir veya ikisinin kredi denetimini tetiklemesini sağlamak için ödeme koşullarının çoğu için aynı değeri kullanabilirsiniz.

### <a name="rank-settlement-discounts"></a>Kapatma iskontolarını sırala   

Kapatma iskontoları değişince kredi denetim kurallarını zorla uygulayabilirsiniz. Kapatma iskontolarına sıra vermeli ve bir sıralama değeri atamalısınız. Siparişteki kapatma iskontolarını, eski kapatma iskontolarından daha yüksek sıralamada kapatma iskontolarına değiştirirseniz sipariş kredi yönetimine gönderilir ve onay gerektirir.

Ödeme koşulları sıralamalarını **Kredi yönetimi > Kurulum > Kredi yönetimi kurulumu > Kapatma iskontolarını sırala** sayfasında ayarlayabilirsiniz.

1. Sıralamak istediğiniz **Nakit iskontosu**'nu seçin. Kapatma iskontosunun **Açıklaması** görüntülenir.
2. **Sıra** değerini seçin. Değerlerin hepsi birbirine göreli olduğu için 1, 2, 3 veya 10, 20, 30 kullanabilirsiniz. Ayrıca, kapatma iskontolarının yalnızca bir veya ikisinin kredi denetimini tetiklemesini sağlamak için kapatma iskontolarının çoğu için aynı değeri kullanabilirsiniz.

## <a name="sequence-the-application-of-rules"></a>Uygulama kurallarını sıraya alma

Kurallar, kuruluşunuzun gereksinimlerine uyacak şekilde değiştirdiğiniz belirli bir sırada çalıştırılır. 

- Satış siparişi yürütme kurallarının bir örneği, bir satış siparişini durdurabilen tüm kuralları geçersiz kılmanızı sağlar. Bir satış siparişi hariç tutma kuralı oluşturun ve **Satış siparişini serbest bırak** seçeneğini işaretleyin. Bu hariç tutma kuralı doğru ise, sipariş beklemeye koyulmaz ve başka hiçbir kural denetlenmez.
- Durdurma kuralları siparişi beklemeye alabilir.
- Hariç tutma kuralları, durdurma kurallarından sonra çalıştırılır. Hariç tutma kuralları yalnızca tanımlandıkları kuralı etkiler. 
- Durdurma ve hariç tutma kuralları önce Tablo, sonra Grup ve sonra Tümü sırasıyla çalıştırılır. Bu işlem sırası sayesinde, Tablo veya Grup düzeyindeki bir hariç tutma kuralı çalıştırılacağı için Tümü düzeyinde çalıştırılmayacak olan bir engelleme kuralı oluşturulabilir.
- Hariç tutmalar, aynı düzeyde oldukları engelleme kuralını geçersiz kılmaz. Örneğin, grup düzeyindeki bir hariç tutma kuralı, grup düzeyindeki engelleme kuralını geçersiz kılmaz. Yukarıda belirtildiği gibi, satış siparişi hariç tutma kuralının bir örneği dışında, Tümü düzeyinde hariç tutmalar ayarlamanız gerekmez. 

**Kullanılan kredi limiti** kuralının davranışı, Alacak ve Tahsilatlar parametre formunda bulunan **Satış siparişi için kredi limitini denetle** parametresinin ayarlarına göre değişecektir.
- Parametre Hayır olarak ayarlanırsa, Kullanılan kredi limiti kuralı çalıştırılmaz.
- Parametre Evet olarak ve **Kredi limiti aşıldığında alınan ileti** Uyarı olarak ayarlanırsa, kredi limiti aşıldığı zaman bir uyarı alırsınız. Çalıştırmak istediğiniz kurallarınız olup olmadığını görmek için **Kullanılan kredi limiti** kuralları çalıştırılır. Ancak, bu senaryo için normalde hiçbir kural eklemezdiniz.
- Parametre Evet olarak ve **Kredi limiti aşıldığında alınan ileti** Hata olarak ayarlanırsa, kredi limiti kontrol edilir ve kredi limiti aşılmışsa sipariş beklemeye alınır. Ek olarak, çalıştırılacak ek kurallar olup olmadığını görmek için **Kullanılan kredi limiti** kuralları çalıştırılır. Bir hata iletisi görüntülenmez ama **Kredi limiti aşıldı** durdurma nedeni gösterilir. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Bir siparişin beklemeye alınma yolunu değiştirecek ayarlar

Siparişler, belirlenmiş kurallar olsa bile, kredi yönetiminden hariç tutulabilir. 

- **Tüm müşteriler > Müşteri seçin > Alacak ve tahsilatlar hızlı sekmesi**'nde **Müşteriyi kredi yönetiminden hariç tut** ayarını değiştirip **Evet** yaparsanız, o müşteriye ilişkin hiçbir sipariş işleme koyulmaz
- **Kredi yönetimi hızlı sekmesindeki** **Satış siparişleri üst bilgisinde** **Kredi yönetiminden hariç tut** değerini değiştirip **Evet** yaparsanız kredi yönetimi kuralları işleme koyulmaz. Bu ayar yalnızca kredi memuru veya kredi yöneticisi tarafından yapılabilir.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Bekletilen siparişleri kredi yönetimi bekletme listesini kullanarak işleme

Kredi yönetimi bekletme listesi, kredi yöneticilerinin, beklemeye alınmış tüm satış siparişlerini görüntüleyebilmelerine ve alacak sorunları giderilince bu siparişlerin bekletme durumlarını kaldırmalarına olanak sağlar. **Kredi yönetimi bekletme listesi** sayfası beklemeye alınmış tüm satış siparişlerini gösterir. **Tüm kredi bekletme işlemleri** sayfasındaki bekletme listesini görüntüleyebilirsiniz (**Kredi yönetimi > Kredi yönetimi bekletme listesi > Tüm kredi bekletme işlemleri**).
Tüm tüzel kişiliklerden gelen satış siparişleri aynı kredi yönetimi bekletme listesine gönderilerek, ilgilenilmesi gereken tüm hareketlerin bir merkezden görülmesi sağlanır. Kullanıcılar yalnızca erişim iznine sahip oldukları tüzel kişiliklerin bilgilerini görür.

Bir satış siparişi bekletme listesine aşağıdaki nedenlerle alınabilir:
1. Müşterinin vadesi belirli bir gün sayısını geçmiş bir faturası vardır. 
2. Siparişte belirli bir hesap durumu vardır.
3. Siparişte belirli ödeme koşulları vardır.
4. Müşterinin sona ermiş bir kredi limiti vardır.
5. Müşterinin vadesi geçmiş bir tutarı vardır ve kredi limitinin belirli bir yüzdesini kullanmıştır.
6. Satış siparişi belirli bir tutarı aşmaktadır.
7. Müşteri, kredi limitinin belirli bir yüzdesini aşmıştır.
8. Ödeme koşulları, müşterinin varsayılan ödeme koşullarından farklıdır.
9. Kapatma iskontoları, müşteri için varsayılan kapatma iskontosundan farklıdır.

Bekletme listesindeki her bir satış siparişi için durdurma nedeni görüntülenir. Bekletme için birden fazla neden varsa, neden **Çoklu** olarak görünür. Satış siparişinin beklemeye alınma nedenlerinin tümünü görmek için eylem bölmesindeki **Durdurma nedenleri** menüsünü kullanabilirsiniz. **Durdurma nedenlerini** bir bilgi kutusunda da görüntüleyebilirsiniz.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Siparişleri işlem için bekletme listesinden çıkarma

Bekletme nedenlerini araştırdıysanız ve bunları giderdiyseniz, işlemlere devam etmek için satış siparişlerini serbest bırakabilirsiniz.

1) Bekletme listesinde bir satır seçin. Birden fazla satır seçerek birden fazla siparişi serbest bırakabilirsiniz.
2) Serbest bırakmak üzere seçilmiş sipariş için bir **Serbest bırakma nedeni** seçin.  
3) Serbest bırakmak üzere seçilen her sipariş için **İnceleme tarihi** girin.  
4) Bir siparişi serbest bırakmak için eylem bölmesindeki **Serbest bırak** menüsünü seçin. Bu menü ancak hareketler seçildikten sonra kullanılabilir. Kullanıcıya iki seçenek sunulur:
   - Bekletmeyi kaldırmak ve belgeyi beklemeye alındığı zaman kullanılan deftere nakil işlemini kullanarak deftere nakletmek için **Deftere nakil ile**'yi seçin. Örneğin satış siparişi onayı beklemeye alındıysa, satış siparişi onayı serbest bırakma işleminden sonra tamamlanır. Kullanıcının onayı deftere nakletmesine izin veren satış siparişi deftere nakil formu görüntülenir.
   - Bekletmeyi başka bir işlem yapmadan kaldırmak için **Deftere nakletmeden**'i seçin. Satış siparişi deftere el ile nakledilebilir.

### <a name="rejecting-orders-in-the-hold-list"></a>Bekletme listesindeki siparişleri reddetme
Bir satış siparişini reddetmek için eylem bölmesindeki **Reddet** menüsünü kullanabilirsiniz
1. Bekletme listesinde bir satır seçin. Birden fazla satır seçerek birden fazla siparişi serbest bırakabilirsiniz.
2. Sipariş, bekletme listesinden kaldırılacak ve satış siparişi üst bilgisi güncellenerek siparişin reddedildiğini gösterecektir.

### <a name="automatically-releasing-credit-management-holds"></a>Kredi yönetimi bekletme işlemlerini otomatik olarak serbest bırakma
Satış siparişleri, bekletme listesine durdurma kurallarına dayanarak yerleştirilir. Ancak, satış siparişi, bekletme listesinde belirli bir süre kalırsa, bazı bekletme nedenleri zaman içinde değişebilir. Örneğin, bir müşteri faturasını ödeyerek kredi limitini açabilir. 

Bekletme listesindeki satış siparişlerini incelemek ve bekletme nedeni ortadan kalktıysa bu siparişleri otomatik olarak serbest bırakmak için **Serbest bırakma için değerlendir** menüsünü kullanabilirsiniz.
1.  **Serbest bırakma için değerlendir** menüsünü seçin
2.  Tüm satış siparişlerini incelemek için **Durdurma kurallarını uygula**'yı seçin. Yalnızca seçtiğiniz satırları incelemek için **Seçili satırlar için durdurma kurallarını uygula**'yı seçin.
3. Tek bir müşteri seçebilmeniz için bir kaydırıcı görüntülenir. Tüm müşteriler için müşteri açılır listesini boş bırakın. 
4. Tamam'a tıkladığınızda işlem arka planda çalıştırılır ve diğer görevler üzerinde çalışmaya devam edebilirsiniz. Tamam'a tıklamadan önce toplu işlemi seçerseniz, Tamam'a tıkladığınızda işlem toplu iş olarak çalışacaktır. Listede bekletilen siparişlerin işlenmesi biraz zaman alabileceğinden, siparişlerin durumunu güncelleştirmek için Yenile'yi kullanın. 
5.  Bir siparişin durdurulma nedeni geçerli değilse, durdurma nedeni artık geçersiz olarak değerlendirilir ve durdurma nedenlerini görüntülediğinizde neden yanında bir onay işareti görmezsiniz.
6.  Tüm durdurma nedenleri temizlendiği takdirde, durdurma nedenleri listesine yeni bir neden (**Serbest bırakmaya hazır**) eklenir. Satış siparişi otomatik olarak serbest bırakılabilir.
7.  **Alacak ve tahsilatlar > Kurulum > Alacak ve tahsilatlar parametreleri > Alacak > Otomatik serbest bırak** sekmesindeki **Otomatik olarak serbest bırak** parametresinin ayarı **Deftere nakil ile** ise, durdurulmuş belgenin naklini deftere nakil formunu kullanarak yapmanız istenir.
8.  **Alacak ve tahsilatlar > Kurulum > Alacak ve tahsilatlar parametreleri > Alacak > Otomatik serbest bırak** sekmesindeki **Otomatik olarak serbest bırak** parametresinin ayarı **Deftere nakletmeden** ise, deftere nakil işlemini el ile yapmanız gerekir.

### <a name="credit-management-approval-workflow"></a>Kredi yönetimi onay iş akışı

Kredi bekletmelerini serbest bırakmayı denetlemek için **Kredi yönetimi iş akışları** da oluşturabilirsiniz. **Kredi yönetimi > Kurulum > Kredi yönetimi iş akışları** sayfasını kullanarak iş akışını ayarladıktan sonra, serbest bırakma veya reddetme işareti koyulmuş siparişler serbest bırakılmadan veya reddedilmeden önce onaylanmaları gereken iş akışına gönderilir. 

İş akışınıza deftere nakille veya deftere nakletmeden serbest bırakma görevlerini dahil ederseniz, iş akışı onayı satış siparişini de serbest bırakacaktır. Ancak, eksik kurulum bilgiler nedeniyle veya başka nedenlerle, serbest bırakma işleminde hata oluşursa, satış siparişini iş akışından geri çekmeniz, hataya neden olan sorunu düzeltmeniz ve sonra siparişi iş akışına yeniden göndermeniz gerekecektir.

İş akışınıza deftere nakille veya nakletmeden serbest bırakma görevleri dahil etmezseniz, iş akışı onay süreci, onay tamamlandıktan sonra satış siparişini el ile serbest bırakmanıza olanak sağlar.

### <a name="forced-credit-hold"></a>Zorunlu kredi bekletme  
  
Sipariş, durdurma kurallarının ölçütlerine uymasa da, satış siparişlerinin durdurulması gereken zamanlar olabilir. Örneğin bir kredi yöneticisine müşteri hakkında krediyle ilgili olmayan bir sorun bildirilebilir ve sorun çözülene kadar siparişleri el ile beklemeye almaya karar verebilirsiniz. Bu durumda bir satış siparişini el ile zorla beklemeye alabilirsiniz.

1. Beklemeye almak istediğiniz satış siparişini açın.  
2. **Kredi yönetimi** eylem bölmesindeki **Kredi yönetimi** sekmesinde **Zorunlu kredi bekletme**'yi seçin.
3. Bir **Zorunlu Bekletme Nedeni** seçin.
4. **Tamam**'a tıklayın. Satış siparişi, Kredi Yönetimi Bekletme listesine iade edilir.

**Kredi yönetimi > Periyodik görevler > Zorunlu Kredi Bekletme** sayfasını kullanarak birden fazla siparişi de beklemeye alınmaya zorlayabilirsiniz. Örneğin, belirli bir müşteriye ait satış siparişlerinin tümünü beklemeye alabilirsiniz.
1. **Zorunlu bekletme nedeni**'ni seçin. 
2. Beklemeye alınacak satış siparişlerini seçmek için **Eklenecek kayıtlar**'a tıklayın. 
3. Seçili satış siparişlerini işlemek için **Tamam**'a tıklayın.

Beklemeye zorla alınan satış siparişleri iş akışıyla işlenemez.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Kredi yönetimi bekletme listesine eklenen siparişleri zorunlu kredi bekletmeyle serbest bırakma
Zorunlu bekletme nedeni olan satış siparişleri otomatik olarak serbest bırakılamaz. Satış siparişi beklemeye zorla alındıysa ve satış siparişlerini otomatik olarak serbest bırakan bir işlem kullandıysanız, satış siparişi **Serbest bırakmaya hazır** olarak görünür ve bekletme listesinde kalır. Siparişi serbest bırakmak için **Serbest bırak** menüsünü kullanmanız gerekir.
 
## <a name="free-text-invoices-orders-and-project-invoice-support-in-credit-management"></a>Kredi yönetiminde serbest metin faturaları, siparişler ve proje faturası desteği 
Kredi yönetimi şu anda yalnızca satış siparişleri için kullanılabiliyor. Serbest metin faturaları, satış noktası siparişleri ve çağrı merkezi siparişleri, kredi limitini ayarlamak için eklediğiniz geçici kredi limitlerini ve sigortayı/garantileri kullanacaktır. Bunlar durdurma kurallarını kullanmayacak ve kredi limitiyle ilgili bir sorun varsa, bekletme listesine alınmayacaktır.

Kredi yönetiminde proje faturaları için destek yoktur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
