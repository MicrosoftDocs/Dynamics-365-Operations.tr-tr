---
title: Tahsilat işlemi otomasyonu
description: Bu konuda, e-posta anımsatıcısı, tahsilat faaliyeti veya müşteriye gönderilecek bir tahsilat mektubu gerektiren müşteri faturalarını otomatik olarak tanımlayan tahsilat işlem stratejilerinin ayarlanma işlemi açıklanmaktadır.
author: JodiChristiansen
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
ms.openlocfilehash: 59db852024faf457db7ac145b67619b31555aaf2
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/10/2021
ms.locfileid: "7486881"
---
# <a name="collections-process-automation"></a>Tahsilat işlemi otomasyonu

[!include [banner](../includes/banner.md)]

Bu konuda, e-posta anımsatıcısı, tahsilat faaliyeti (telefon görüşmesi gibi) veya müşteriye gönderilecek bir tahsilat mektubu gerektiren müşteri faturalarını otomatik olarak tanımlayan tahsilat işlem stratejilerinin ayarlanma işlemi açıklanmaktadır. 

Kuruluşlar, açık olan bir fatura veya hesap bakiyesi hakkında hangi müşterilerle bağlantı kurulması gerektiğini öğrenmek amacıyla, eski bakiye raporlarını, müşteri hesaplarını ve açık faturaları araştırmak için genellikle önemli miktarda zaman harcar. Bu araştırma, vadesi geçmiş bakiyeleri toplamak için müşterilerle iletişim kurmak veya fatura anlaşmazlıklarını çözmek için tahsilat görevlisi tarafından harcanan zamanı ortadan kaldırır. Tahsilat işlem otomasyonu, tahsilat işleminiz için strateji tabanlı bir yaklaşım ayarlamanıza olanak sağlar. Bu, özelleştirilmiş e-posta anımsatıcıları veya tahsilat mektuplarını göndermek için programlanmış işlem sağlayarak, tahsilat etkinliklerini sürekli olarak uygulamanıza yardımcı olur. 

## <a name="collections-process-setup"></a>Tahsilat işlemi kurulumu
Etkinlikleri planlayacak, e-posta mesajları gönderecek ve müşteri tahsilat mektuplarını oluşturup gönderecek otomatik tahsilat işlemini oluşturmak için, **Tahsilat işlem ayarı** sayfasını (**Krediler ve tahsilatlar > Kurulum > Tahsilat süreç ayarı**) kullanabilirsiniz. İşlem adımları, yol açan veya en eski açık faturaya göre yapılır. Her adım, belirli bir müşteriyle hangi iletişimin veya etkinliğin gerçekleşmesi gerektiğini belirlemek için bu faturayı kullanır.  

Tahsilat ekipleri genellikle, bekleyen her faturayla ilgili önceden bir bildirim göndererek, fatura ödemesinin yaklaştığı konusunda müşterinin bilgilendirilmesini sağlar. Her fatura için işlem hiyerarşisindeki adımların sırayla atılmasını sağlamak için **Ön hatırlatma** seçeneği ayarlanabilir.

### <a name="process-hierarchy"></a>İşlem hiyerarşisi
Her müşteri havuzu yalnızca bir işlem hiyerarşisine atanabilir. Bu adımın hiyerarşi derecesi, bir müşteri işlem hiyerarşisi atanmış birden fazla havuza dahil edildiğinde hangi işlemin öncelikli olduğunu tanımlar. Havuz kimliği, hangi müşterilerin işleme atanacağını belirler. Ayarlanan her hiyerarşi yalnızca bir işlem otomasyonuna atanabilir.

Faaliyetsiz günler, bir müşteriyle otomatik işlem tarafından çok sık bağlantı kurulmamasını sağlamak için kullanılır. Örneğin, faaliyetsiz günler iki olarak ayarlanmışsa, orijinal yol açan fatura tam olarak kapatılmış olsa bile, müşteriyle otomatik işlem tarafından en az iki gün süreyle iletişim kurulmaz. 

Müşterinin eski bakiyesi veya fatura tutarı tanımlı bir değerden azsa müşterileri işlem otomasyonunun dışında tutmak için **Sürecin dışında tut** alanında **Müşterinin eski bakiyesi şundan küçüktür:** ya da **Fatura tutarı şundan küçüktür:** seçeneğini belirleyin ve tutar değerini girin.

Müşteri ödeme tahminlerini kullanarak tahsilat faaliyetleri oluşturmak için **Tahmini kullan**'ı işaretleyin. Oluşturulan faaliyetler, **Alacak hesapları parametreleri** sayfasında, **Tahsilat işlemi otomasyonu** sekmesinde **Ödeme tahminleri**'ndeki Faaliyet şablonunu kullanır. 

### <a name="process-details"></a>İşlem ayrıntıları
Hiyerarşiye yeni bir işlem ayrıntısı eklemek için **Yeni**'ye tıklayın. **Açıklama**, hiyerarşideki adımın amacını veya adını tanımlamak için kullanılır. Etkinlik oluşturan, e-posta gönderen veya tahsilat mektubu oluşturan adımı tanımlamak için **Eylem türü**'nü seçin. 

- **İş belgesi**, eylem türünü oluşturmak için kullanılan şablonu tanımlar. Bu belge bir faaliyet şablonu, bir e-posta şablonu veya her müşteriye gönderilen bir tahsilat mektubu olabilir. Tahsilat işlemi otomasyonu, diğer tahsilat parametrelerinin nasıl ayarlandığı dikkate alınmaksızın yalnızca müşteri başına tahsilat mektupları oluşturur.
- **Zaman**, baştaki (en eski) fatura vade tarihinden önce veya sonra gerçekleşecek işlem tanımını tanımlar ve **Fatura vade tarihiyle ilişkili gün sayısı** sütununda görüntülenen sayıyla birlikte kullanılır. 
- İşlem hiyerarşisinde bir adımda her fatura için bir eylem oluşturmak üzere **Ön hatırlatma** seçeneğini işaretleyin. Ön hatırlatma eylemleri genellikle bekleyen faturalarla ilgili önceden bir bildirimdir, böylece müşteri fatura ödemesinin yaklaştığı konusunda bilgilendirilebilir. Ön hatırlatma yalnızca hiyerarşi başına bir faaliyet için işaretlenebilir. Bir e-posta eylem türü seçtiğinizde alıcı, e-postanın bir müşteri, satış grubu veya tahsilat temsilcisine gönderilip gönderilmeyeceğini tanımlamak için kullanılır. 
- Daha sonra **İş amaçlı ilgili kişi** alanındaki değer, o müşterinin hesabından hangi ilgili kişiyle iletişim kurulacağını belirler.

### <a name="business-document-details"></a>İş belgesi ayrıntıları
İş belgesi ayrıntıları, işlem ayrıntılarında seçilen eylem türüne göre değişir. Eylem türü etkinlik olduğunda, etkinlik şablonu ayrıntıları gösterilir. Bu ayrıntılar arasında etkinlik şablonu adı, oluşturulacak etkinliğin türü, etkinliğin amacı, etkinliğin tamamlanması için planlanan gün sayısı ve etkinliğin ayrıntıları sayılabilir. Bu etkinlik daha sonra, etkinliği tamamlamak için gereken eylemi alıcıya bildiren yol açan faturaya bağlantı sağlar.

Eylem türü işlem ayrıntılarında bir e-posta ise, bu bölümde iki hızlı sekme bulunur. İlki, şablon kimliğini, e-posta açıklamasını, varsayılan dili, otomatik olarak gönderilen e-posta iletilerine atanacak kullanıcı adını ve ilişkili gönderici e-posta adresini tanımlamak için kullanılır. İkincisi, **Düzenle** seçilerek, **Dil** ve **Konu** alanlarındaki değerler kaydedildikten sonra oluşturulacak e-posta gövdesinin oluşturulmasına olanak tanır. Bu, HTML içeriğinin karşıya yüklenmesini sağlayan bir pencere açar. 

> [!Note]
> İletişimin gövde metnini HTML biçiminde içeren bir Outlook e-posta iletisi kaydedebilirsiniz. Ardından şablonu uygulamak için ileti içeriğini yükleyebilirsiniz. <br> <br> Tahsilat mektubu için eylem türü seçilirse kurulum sayfasında iş belgesi ayrıntı bölümü olmaz.

Seçili işlem hiyerarşisi için en son geçmişi görüntülemek üzere **Tahsilat işlemi geçmişi** düğmesini kullanın. 

Bir tahsilat işlemine atanan müşterileri görüntülemek için **Tahsilat işlemi ataması** eylemine tıklayın. Belirli bir müşterinin atandığı hiyerarşiyi görüntülemek için **Müşteri atamasını önizle** seçeneğini kullanın. Çalıştırıldığında hiyerarşiye atanacak müşterileri önizlemek için **İşlem atamasını önizle** seçeneğini kullanın. Bir işleme el ile atanan müşterileri görüntülemek veya bir işleme atanacak müşterileri seçmek için **El ile atama**'ya tıklayın.

Seçili işlem otomasyonu şu anda çalıştırıldığında oluşturulacak eylemleri önizlemek için **İşlem simülasyonu** eylemine tıklayın. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
