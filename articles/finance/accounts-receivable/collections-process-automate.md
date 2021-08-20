---
title: Tahsilat işlemi otomasyonu
description: Bu konuda, e-posta anımsatıcısı, tahsilat faaliyeti veya müşteriye gönderilecek bir tahsilat mektubu gerektiren müşteri faturalarını otomatik olarak tanımlayan tahsilat işlem stratejilerinin ayarlanma işlemi açıklanmaktadır.
author: panolte
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0afc56ecea72e281d689930cc91cf6048426d3127ab10c8c284b2eea0f3933d6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723907"
---
# <a name="collections-process-automation"></a>Tahsilat işlemi otomasyonu

[!include [banner](../includes/banner.md)]

Bu konuda, e-posta anımsatıcısı, tahsilat faaliyeti (telefon görüşmesi gibi) veya müşteriye gönderilecek bir tahsilat mektubu gerektiren müşteri faturalarını otomatik olarak tanımlayan tahsilat işlem stratejilerinin ayarlanma işlemi açıklanmaktadır. 

Kuruluşlar, açık olan bir fatura veya hesap bakiyesi hakkında hangi müşterilerle bağlantı kurulması gerektiğini öğrenmek amacıyla, eski bakiye raporlarını, müşteri hesaplarını ve açık faturaları araştırmak için önemli miktarda zaman harcar. Bu araştırma, vadesi geçmiş bakiyeleri toplamak için müşterilerle iletişim kurmak veya fatura anlaşmazlıklarını çözmek için tahsilat görevlisi tarafından harcanan zamanı ortadan kaldırır. Tahsilat işlem otomasyonu, tahsilat işleminiz için strateji tabanlı bir yaklaşım ayarlamanıza olanak sağlar. Bu, özelleştirilmiş e-posta anımsatıcıları veya tahsilat mektuplarını göndermek için programlanmış işlem sağlayarak, tahsilat etkinliklerini sürekli olarak uygulamanıza yardımcı olur. 

## <a name="collections-process-setup"></a>Tahsilat işlemi kurulumu
Etkinlikleri planlayacak, e-posta mesajları gönderecek ve müşteri tahsilat mektuplarını oluşturup gönderecek otomatik tahsilat işlemini oluşturmak için, **Tahsilat işlem ayarı** sayfasını (**Krediler ve tahsilatlar > Kurulum > Tahsilat süreç ayarı**) kullanabilirsiniz. İşlem adımları, yol açan veya en eski açık faturaya göre yapılır. Her adım, belirli bir müşteriyle hangi iletişimin veya etkinliğin gerçekleşmesi gerektiğini belirlemek için bu faturayı kullanır.  

Tahsilat ekipleri genellikle, bekleyen her faturayla ilgili önceden bir bildirim göndererek, fatura ödemesinin yaklaştığı konusunda müşterinin bilgilendirilmesini sağlar. Her fatura için işlem hiyerarşisindeki adımların sırayla atılmasını sağlamak için **Ön hatırlatma** seçeneği ayarlanabilir.

### <a name="process-hierarchy"></a>İşlem hiyerarşisi
Her müşteri havuzu yalnızca bir işlem hiyerarşisine atanabilir. Bu adımın hiyerarşi derecesi, bir müşteri işlem hiyerarşisi atanmış birden fazla havuza dahil edildiğinde hangi işlemin öncelikli olduğunu tanımlar. Havuz kimliği, hangi müşterilerin işleme atanacağını belirler. 

Faaliyetsiz günler, bir müşteriyle otomatikleştirilmiş süreç tarafından çok sık bağlantı kurulmamasını sağlamak için kullanılır.  Örneğin, faaliyetsiz günler iki olarak ayarlanmışsa, orijinal yol açan fatura tam olarak kapatılmış olsa bile, müşteriyle otomatik işlem tarafından en az iki gün süreyle iletişim kurulmaz. 

Hesap bakiyesi veya fatura bakiyesi tanımlı bir değerden azsa, müşterileri işlem otomasyonunun dışında tutmak için, **Sürecin dışında tut** alanını **Evet** olarak ayarlayın ve tutar değerini girin.

## <a name="process-details"></a>İşlem ayrıntıları
**Açıklama**, hiyerarşideki adımın amacını veya adını tanımlamak için kullanılır.

**Eylem türü**, adımın bir etkinlik oluşturmak mı, bir e-posta göndermek mi, yoksa bir tahsilat mektubu oluşturmak mı olduğunu tanımlar.

**İş belgesi**, eylem türünü oluşturmak için kullanılan şablonu tanımlar.  Bu, her müşteri için bir faaliyet şablonu, bir e-posta şablonu veya bir tahsilat mektubu olabilir. 

Eylem türleri **Fatura vadesine ilişkin gün** sütununda görüntülenen ayara göre fatura vade tarihinden önce veya sonra oluşturulabilir.

Bir e-posta eylem türü seçtiğinizde; alıcı, bir müşteri, satış grubu veya tahsilat görevlisi olup olmayacağını tanımlamak için kullanılır. Daha sonra **İş amaçlı ilgili kişi** alanındaki değer, o müşterinin hesabından hangi ilgili kişiyle iletişim kurulacağını belirler.

## <a name="business-document-details"></a>İş belgesi ayrıntıları
İş belgesi ayrıntıları, işlem ayrıntılarında seçilen eylem türüne göre değişir.  Eylem türü etkinlik olduğunda, etkinlik şablonu ayrıntıları gösterilir.  Bu ayrıntılar arasında etkinlik şablonu adı, oluşturulacak etkinliğin türü, etkinliğin amacı, etkinliğin tamamlanması için planlanan gün sayısı ve etkinliğin ayrıntıları sayılabilir.  Bu etkinlik daha sonra, etkinliği tamamlamak için gereken eylemi alıcıya bildiren yol açan faturaya bağlantı sağlar.

Eylem türü işlem ayrıntılarında bir e-posta ise, bu bölümde iki hızlı sekme bulunur.  İlki, şablon kimliğini, e-posta açıklamasını, varsayılan dili, otomatik olarak gönderilen e-posta iletilerine atanacak kullanıcı adını ve ilişkili gönderici e-posta adresini tanımlamak için kullanılır. İkincisi, **Düzenle** seçilerek, **Dil** ve **Konu** alanlarındaki değerler kaydedildikten sonra oluşturulacak e-posta gövdesinin oluşturulmasına olanak tanır.  Bu, HTML içeriğinin karşıya yüklenmesini sağlayan bir pencere açar. Pencerenin sol alt kutusuna el ile oluşturulan iletiyi de yazabilirsiniz.  

> [!Note]
> Outlook e-postaları, HTML biçimindeki istenen iletişim gövdesiyle kaydedilebilir. Bu daha sonra şablonu uygulamak için karşıya yüklenebilir. <br> <br> Tahsilat mektubu için eylem türü seçilirse kurulum formunda iş belgesi ayrıntı bölümü olmaz.


## <a name="fasttab-reference"></a>Hızlı sekme referansı
Aşağıdaki tablolarda, belirtilen hızlı sekmelerin erişilebileceği sayfalar ve alanlar ile ilgili sekmedeki bilgilerin açıklaması birlikte verilmektedir. 

### <a name="process-hierarchy"></a>İşlem hiyerarşisi

|     Sayfa                                                  |     Alan                         |     Tanım                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Tahsilat işlemi kurulumu <br> İşlem otomasyonu       |                                   |     Müşteri havuzu atamalarını temel alan tahsilat işlemlerini oluşturun ve yönetin.                                                                                                                             |
|     Tahsilat işlemi kurulumu <br> İşlem otomasyonu       |     Hiyerarşi                     |     Birden çok havuza ait olan bir müşteriyi atamak üzere işlem otomasyonu önceliğini tanımlar.                                                                                                   |
|     Tahsilat işlemi kurulumu <br> İşlem otomasyonu       |     Havuz kimliği                       |     Müşteri kayıtlarına ait bir grubu tanımlayan sorgulardır.                                                                                                                                                        |
|     Tahsilat işlemi kurulumu <br> İşlem otomasyonu       |     Faaliyetsiz günler                    |     İşlem adımının ne sıklıkta tamamlanacağını sınırlayın. Örneğin, iki faaliyetsiz gün ayarlandıysa, yol açan fatura değişirse, sonraki işlem adımı en az iki gün boyunca gerçekleşmeyecektir.     |
|     Tahsilat işlemi kurulumu <br> İşlem otomasyonu       |     İşlemin dışında tut        |     **Müşterinin eski bakiyesi şundan küçüktür:** veya **Fatura tutarı şundan küçüktür:** seçilirse değer ölçütü karşılanmadığında, bir müşteri işlem otomasyonunun dışında bırakılır.                                   |

### <a name="process-details"></a>İşlem ayrıntıları
|     Sayfa                                                  |     Alan                                         |      Tanım                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Tahsilat işlemi kurulumu <br> İşlem otomasyonu       |                                                   |     Yol açan faturaya göre alınan adımları tanımlayın.                                                                                                |
|                                                           |     Tanım                                   |     Adımın adını ve/veya açıklamasını sağlamak için kullanılan serbest metin alanı.                                                                           |
|                                                           |     Eylem türü                                   |     İşlem adımı tarafından oluşturulacak etkinlik, eposta veya tahsilat mektubu.                                                                     |
|                                                           |     İş belgesi                           |     İşlem adımı sırasında kullanılan etkinliği veya e-posta şablonunu tanımlar.                                                                        |
|                                                           |     Ne zaman                                          |     İşlem adımının, **Fatura vade tarihi ile ilişkili gün sayısı** alanının yanı sıra yol açan faturanın vade tarihinden önce mi, yoksa sonra mı işlemin gerçekleşeceğini tanımlar.        |
|                                                           |     Fatura vade tarihiyle ilişkili gün sayısı        |     **Ne zaman** alanıyla birlikte işlem adımının zamanlamasını tanımlar.                                                                          |
|                                                           |     Ön hatırlatma                                   |     Bu seçim, her bir işlem hiyerarşisinde tek bir adımın ayarlanmasını ve zamanlama ölçütlerine ulaşıldığında her faturaya için çalıştırılmasını sağlar.                                                |
|                                                           |     Siparişi alan                                     |     Müşteriye, satış grubuna veya tahsilat görevlisi ilgili kişisine e-posta gönderilip gönderilmeyeceğini tanımlar.                                                   |
|                                                           |     İş amacı ilgili kişisi                    |     E-posta iletişimlerinde hangi alıcının e-posta adresinin kullanılacağını belirler.                                                                                 |

### <a name="business-process-activity-template-details"></a>İş süreci etkinlik şablonu ayrıntıları 
|     Sayfa                                                  |     Alan                     |      Tanım                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Tahsilat işlemi kurulumu <br> İşlem otomasyonu       |                               |     Kurulum işleminin, faaliyet şablonunun ayrıntılarını tanımlayan bölümü.                                                                      |
|     Tahsilat işlemi kurulumu <br> İşlem otomasyonu       |     Etkinlik şablonu       |     Tür, amaç, tamamlanması gereken gün sayısını tanımlar ve etkinlik işlemi adımı sırasında oluşturulacak etkinlikle ilgili ayrıntıları sağlar.       |

### <a name="business-document-email-template-details"></a>İş belgesi e-posta şablonu ayrıntıları 
|     Sayfa                                                  |     Alan     |      Tanım                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Tahsilat işlemi kurulumu <br> İşlem otomasyonu       |               |     E-posta işlem adımı sırasında oluşturulacak e-posta açıklaması, varsayılan dil, gönderen adı ve e-posta adreslerini tanımlar.        |


### <a name="collections-history"></a>Tahsilatlar geçmişi 
|     Sayfa                              |     Alan     |      Tanım                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Tahsilat işlemi kurulumu       |               |     Seçili işlem hiyerarşisi için en son geçmişi görüntüleyin.       |

### <a name="collection-process-assignment"></a>Tahsilat işlem ataması
|     Sayfa                              |     Alan     |      Tanım                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Tahsilat işlemi kurulumu       |               |     Bir tahsilat işlemine atanan müşterileri görüntüleyin.  
|     El ile atama               |               |     Bir işleme el ile atanan veya bir işleme atanacak müşterileri seçebileceğiniz müşterileri görüntüleyin. |
|     İşlem atamasını önizle      |               |     Çalıştırıldığında bir stratejiye atanacak müşterileri önizleyin.   |
|     Müşteri atamasını önizle     |               |     Belirli bir müşterinin atandığı stratejiyi görüntüleyin.    |
 
 ### <a name="process-simulation"></a>İşlem simülasyonu
|     Sayfa                              |     Alan     |      Tanım                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|    İşlem simülasyonu                 |               |     Seçili işlem otomasyonu Şu anda çalıştırıldığında oluşturulacak eylemleri önizleyin. |

### <a name="parameters"></a>Parametreler
|     Sayfa                                                                  |     Alan                                             |      Tanım                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Alacak hesapları parametreleri > Tahsilat işlemi otomasyonu     |     Toplu iş görevi başına müşteri yüzdesi          |     Otomasyon işlemi başına toplu iş görev sayısını belirleyen ayar.                                          |
|     Alacak hesapları parametreleri > Tahsilat işlemi otomasyonu     |     Tahsilat mektuplarını otomatik olarak gönder           |     Tahsilat mektubu eylem türleri, otomasyon sırasında mektubu gönderir.                                      |
|     Alacak hesapları parametreleri > Tahsilat işlemi otomasyonu     |     Otomasyon için etkinlikleri oluşturma                |     Bir hesapta alınan tüm otomatik adımları görüntülemek için etkinlik dışı eylem türlerine ait etkinlikler oluşturun ve kapatın.        |
|     Alacak hesapları parametreleri > Tahsilat işlemi otomasyonu     |     Tahsilat işlemi otomasyon geçmişinin tutulacağı gün sayısı     |     Tahsilat geçmişinin saklanacağı gün sayısını tanımlar.                                                       |
|     Alacak hesapları parametreleri > Tahsilat işlemi otomasyonu     |     Son işlem adımını etkinleştirdikten sonra faturayı hariç tut    |     Tahsilat işleminin son adımına ulaşan bir fatura, gelecekteki işlem otomasyonu eylem türlerini oluşturmak için kullanılmaz. Sonraki en eski fatura, tahsilat işlemi Otomasyon eylemlerinin devam etmesini sağlamak için sonraki işlem otomasyonu adımını belirleyecektir.                                                        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
