---
title: Folyoları yönetme
description: Bu konu, folyolarla nasıl çalışılacağını açıklamaktadır. Folyo genellikle sevkiyat başına bir varlık veya şirket için bir satıcının mallarından oluşur. Bir folyodaki mallar bir konteynerde olabilir veya birden fazla konteynere yayılabilir.
author: sherry-zheng
manager: tfehr
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2205ad8da1987130e97054b3f20749bce61198dd
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500850"
---
# <a name="manage-folios"></a>Folyoları yönetme

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Folyo genellikle gümrük yönetmelikleri tarafından belirlenir. Sevkiyat başına bir tüzel kişilik veya şirket için bir satıcının mallarından oluşabilir. Bir folyodaki mallar bir konteynerde olabilir veya birden fazla konteynere yayılabilir.

**Tüm folyolar** sayfasını açmak için **Varış yeri maliyeti \> Folyolar \> Tüm folyolar** sayfasına gidin. Bu sayfada tüm geçerli folyoların listesi göstermektedir. Folyo oluşturmak, silmek ve onlarla çalışmak için Eylem Bölmesindeki düğmeleri kullanabilirsiniz. Ayrıntılarını **Folyolar** sayfasında görüntülemek için listedeki herhangi bir folyo seçin.

## <a name="action-pane"></a>Eylem Bölmesi

**Tüm folyolar** ve **Folyolar** sayfalarındaki Eylem Bölmesi, seçili bir folyoyla çalışmanıza olanak sağlayan düğmeler sunar. Her düğme tek bir eylem gerçekleştirir. Eylem Bölmesi, her biri sırayla bir dizi ilgili düğme sağlayan sekmeler de içerir. Belirtilen durumlar dışında, aşağıdaki alt bölümlerde açıklanan tüm düğmeler ve sekmeler hem liste görünümünde (yani **Tüm folyolar** sayfasında) hem de ayrıntılı görünümde (yani **Folyolar** sayfasında) kullanılabilir.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Doğrudan Eylem Bölmesinde görünen düğmeler

Aşağıdaki tabloda, doğrudan Eylem Bölmesinde bulunan düğmeler açıklanmaktadır.

| Düğme | Tanım |
|---|---|
| Yeni | Folyo oluştur. |
| Delete | Açık veya seçili folyoyu silin. |
| Seyahat maliyetleri | Seyahatteki tüm malları görüntüleyebileceğiniz ve bunlara folyo düzeyinde maliyetler ekleyebileceğiniz **Seyahat maliyetleri** sayfasını açın. Folyo maliyetleri seyahate el ile eklendiğinde, maliyet sorgulama sayfasına otomatik olarak eklenir ve **Seyahat maliyetleri** sayfasında belirtilen yönteme göre her mala tahsis edilir. |

### <a name="buttons-on-the-manage-tab"></a>Yönet sekmesindeki düğmeler

Aşağıdaki tabloda, doğrudan Eylem Bölmesinde bulunan **Yönet** sekmesindeki düğmeler açıklanmaktadır.

| Düğme | Tanım |
|---|---|
| Girişler listesini deftere naklet | Folyodaki tüm satın alma siparişi satırları için bir giriş listesini deftere nakledin. Çok şirketli sevkiyatlar kullanılırsa her şirket için yeni bir giriş listesi deftere nakil iletişim kutusu açılır. |
| Ürün girişini deftere naklet | Folyodaki tüm satın alma siparişi satırları için bir ürün girişini deftere nakledin. Çok şirketli seyahatler kullanılırsa her şirket için yeni bir ürün girişi deftere nakil iletişim kutusu açılır. |
| Faturayı deftere naklet | Folyodaki tüm satın alma siparişi satırları için bir faturayı deftere nakledin. Çok şirketli seyahatler kullanılırsa her şirket için yeni bir fatura deftere nakil iletişim kutusu açılır. |
| Sevk transfer emri | İlgili sevkiyattaki geçerli folyoyla ilişkili tüm transfer emri satırları için bir transfer emrini deftere nakledin. |
| Transfer emrini al | İlgili sevkiyattaki geçerli folyoyla ilişkili tüm transfer emri satırları için transfer emri girişini deftere nakledin. |
| Transitteki malları al | Folyodaki transitteki tüm sipariş satırlarını alın. |
| Belgeler alındı | **Alınan belgeler** seçeneğinin ayarını *Evet* olarak güncelleştirin. Daha fazla güncelleştirilmemesi için maddeyi ve/veya satın alma satırını kilitlemek için bu düğmeyi kullanabilirsiniz. |
| Otomatik maliyetleri bul | İlgili seyahat maliyetlerini bulun. Bu maliyetler zaten bulunduysa veya güncelleştirildiyse aşağıdaki iletiyi alırsınız: "Faturalanmamış maliyet satırları mevcut. Üzerine yazılmasını ister misiniz?" Folyoya eklenen ve faturalanan seyahat maliyetlerinin üzerine yazılmayacağını unutmayın. |
| Varış günlüğü oluştur | Gelişmiş ambar özelliklerini kullanarak kuruluşlar için bir varış günlüğü oluşturun. **Miktarı başlat** (önerilir), **Transitteki mallardan oluştur** ve/veya **Satın alma siparişlerinden oluştur**'u seçebilirsiniz. Son seçenek, transitteki malların işlemesinin kullanılıp kullanılmadığına bağlıdır. |
| Tahakkuk eden maliyetler | Maliyet türünün borç için belirtilen bir genel muhasebe hesabına sahip olduğu maliyetleri tahakkuk edin. Bu düğme genellikle stok transitteyken veya mallar teslim alındığında ve faturalandığında kullanılır. |

### <a name="buttons-on-the-general-tab"></a>Genel sekmesindeki düğmeler

Aşağıdaki tabloda, doğrudan Eylem Bölmesinde bulunan **Genel** sekmesinde açıklanmaktadır.

| Düğme | Tanım |
|---|---|
| Giriş listesi | Folyodaki tüm satın alma siparişi satırları için bir giriş listesini deftere nakledin. Çok şirketli seyahatler kullanılırsa her şirket için yeni bir giriş listesi deftere nakil iletişim kutusu açılır. |
| Ürün girişi | Kullanılıyorsa ürün girişi kaydını görüntüleyin. |
| Madde varışı | Kullanılıyorsa madde varış günlüğünü görüntüleyin. |
| Maliyetlerin sorgusu | Sevkiyat konteyneri, folyo ve satın alma siparişi de dahil olmak üzere bir yolculuğun tüm maliyetlerini görüntülemek için maliyet sorgulama sayfasını açın. Görünüm eylemini kullanarak sayfanın tam görünümünü ayarlayabilirsiniz. Maliyet sorgulama sayfasında, alanlardan herhangi birini, madde ve maliyet türü kodunu görüntüleyebilirsiniz. Bu öğeleri kaldırarak maliyetleri gruplandırarak sayfayı ayarlayabilirsiniz. Boyut ve renk kullanıyorsanız bu özellik yararlı olabilir. Sayfada gösterilen boyutları değiştirebilirsiniz. **Maliyetler** sayfasında yalnızca **Deftere Nakil** sekmesindeki **Dr** girişinin *Madde* olarak ayarlandığı maliyet türü kodları gösterilir. |

## <a name="header-view"></a>Başlık görünümü

**Başlık** görünümünü açmak için bir folyo açın ve folyo başlığının sağ üst sekmesindeki **Başlık** sekmesini seçin.

### <a name="settings-on-the-general-fasttab"></a>Genel hızlı sekmesindeki ayarlar

Aşağıdaki tabloda, folyonun **Başlık** görünümünün **Genel** hızlı sekmesinde bulunan alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Folyo | Folyonun adı. Folyo oluşturulduğunda bu ad otomatik olarak oluşturulur.|
| Seyahat | Folyoyla ilişkilendirilen seyahat. |
| Gümrük müşaviri | Folyo için gümrük müşaviri seçin. Gümrük komisyoncuları satıcıda tanımlanır. Oluşturulan maliyetlerin otomatik olarak belirlenmesini sağlarlar. |
| Ara irsaliye/Konşimento | Folyo için geçerli olan ara irsaliyeyi veya konşimentoyu belirtinin. |
| Şirket | Folyo ile ilişkili tüzel kişilik (şirket). |
| Kargo kontrol numarası | Bu alan bazı ülke veya bölgelerdeki gümrük departmanları tarafından kullanılmaktadır. |
| Ölçüm | Bu alan, bir ölçümün **Varış yeri maliyeti** modülünde belirtilmesini sağlar. Ölçümler genellikle malların tek tek hacmini veya ağırlığını bilmeyen ancak tutarın veya miktarın sağladığından daha doğru bir onay gerektiren kuruluşlar tarafından kullanılır. Navlun ileticisi ağırlık veya kübik ölçümü sağlar ve bunu bir madde veya satın alma siparişi düzeyine yerleştirebilirsiniz. Parametre seçilirse veya el ile girilirse otomatik olarak güncellenebilir. |
| Ölçüm birimi | Belirtilen ölçüm için geçerli olan birim. |
| Karton sayısı | Folyodaki kartonların sayısı. Bu alan, parametre seçimine bağlı olarak otomatik olarak güncelleştirilebilir. |
| Satıcı hesabı | Folyoyla ilişkilendirilen satıcıyı seçin. Bu alan yalnızca bilgi amaçlıdır. İşlevselliği etkilemez. |
| Kuruluş adı | Seçili satıcı hesabının adı. |
| Açıklamalar | Folyo ile ilgili ek bilgileri girin. |
| Malların açıklaması | Folyoyu tanımlamaya yardımcı olmak için bir mal açıklaması seçin. Daha fazla bilgi için bkz. [Malların açıklaması](shipping-information-setup.md#description-of-goods). |
| Değerleme tarihi | Bu alan görev girişi sayfasıyla ilgilidir. **Varış yeri maliyeti** modülü, burada belirlediğiniz tarih için gümrük döviz kurunu kullanır. Varsayılan değer, vergi girişi sayfasındaki tarihtir. |
| Gümrük Kimliği | Gümrük kimliğini girin. Ülke veya bölgelerdeki gümrük departmanları bu kimliği sağlar. |
| Tarife kodu | Folyo ile ilişkilendirmek için bir tarife kodu girin. Bu kod genellikle sevkiyat yaptığınız ülke veya bölge tarafından gereklidir (ve tanımlanır). |

### <a name="settings-on-the-delivery-fasttab"></a>Teslimat hızlı sekmesindeki Ayarlar

Aşağıdaki tabloda, folyonun **Başlık** görünümünün **Teslimat** hızlı sekmesinde bulunan ayarlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Folyo tarihi | Folyo ile ilişkilendirilecek bir tarih seçin. Varsayılan değer, seyahatin oluşturulma tarihidir. |
| Sevkiyat limanındaki ETA | Varış limanındaki ("varış" limanı) tahmini varış saati (ETA) tarihi. |
| Tahmini teslim tarihi | Genellikle, malların ambara varması gereken tarih. Bu alan, tahmini teslim tarihi hesaplandığında kullanılmaz. (Bunun yerine izleme denetimi tahmini teslim tarihi kullanılır.) Bu alanı, değerin izleme denetimi tahmini teslim tarihiyle eşleşecek şekilde ayarlamak için [İzleme denetim merkezi](delivery-information-setup.md#tracking-control-center)'ni kullanın. |
| Alınan orijinal belgeler | Orijinal belgelerin alındığı tarih. |
| Aracı tarafından önerilir | Aracının önerildiği tarih. |
| Gönderilen orijinal konşimento | Orijinal konşimentonun gönderildiği tarih. |
| Piyasaya sürülen mallar | Malların serbest bırakıldığı tarih. |
| Müşteri randevusu | Müşteri randevusu tarihi. |
| Ambara teslim edildi | Malların ambara teslim edildiği tarih. |
| Doğrulama tarihi | Doğrulama tarihi. |
| Teslimat talimatları | Teslimat talimatlarının alındığı tarih. |
| Çıkış limanı | Seyahatin çıktığı liman. |
| Varış limanı | Seyahatin varış limanı. Gemi birden fazla limanda durabileceğinden, sevkiyat konteynerinin farklı bir limanı olabilir. |

### <a name="settings-on-the-export-fasttab"></a>İhracat hızlı sekmesindeki ayarlar

Aşağıdaki tabloda, folyonun **Başlık** görünümünün **İhracat** hızlı sekmesinde bulunan ayarlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| İhracatçı | İhracatçı folyo üzerinde saklanabilir. Uluslararası ticarette, bir şirkete satın alma siparişi gönderebilir ancak malları başka bir şirketten alabilirsiniz. Gümrük, izlemeyi ve belgeleri gerekli kılar. İhracatçının adı ve adresi burada saklanabilir. |
| Kuruluş adı | Seçilen ihracatçının adı. |

## <a name="lines-view"></a>Satırlar görünümü

**Satırlar** görünümünü açmak için bir folyo açın ve folyo başlığının sağ üst sekmesindeki **Satırlar** sekmesini seçin.

### <a name="information-on-the-folio-fasttab"></a>Folyo hızlı sekmesi hakkında bilgi

**Satırlar** görünümündeki **Folyo** hızlı sekmesi, folyo hakkındaki bilgileri gösterir. Bu bilgilerin çoğu, bu konuda daha önce açıklandığı gibi **Başlık** görünümünde de görünür.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Satırlar hızlı sekmesindeki bilgiler ve düğmeler

**Satırlar** görünümündeki **Satırlar** hızlı sekmesi, geçerli folyoya dahil edilen her tam veya kısmi satın alma siparişi satırıyla ilgili ayrıntıları gösterir.

Aşağıdaki tabloda, **Satırlar** görünümündeki **Satırlar** hızlı sekmesinde yer alan düğmeler açıklanmaktadır.

| Düğme | Tanım |
|---|---|
| Kaldır | Seçili satın alma siparişi satırını seyahatten kaldırın. |
| Stok \> Hareketler | Seçili satın alma siparişi satırı için stok hareketlerini görüntüleyin. Transitteki malları kullanıyorsanız orijinal siparişin ve transitteki malların da gösterildiğini unutmayın. |
| Stok \> Görüntüleme boyutları | Görüntülediğiniz hareketler için görünen stok boyutlarını seçebileceğiniz bir iletişim kutusu açar. |
| Yenile | Seçili satın alma siparişi satırının satır tutarı, ağırlığı veya hacmiyle ilgili bilgileri güncelleştirin. |

### <a name="information-on-the-lines-details-fasttab"></a>Satır ayrıntıları hızlı sekmesi hakkında bilgi

**Satırlar** görünümündeki **Satır ayrıntıları** hızlı sekmesi, **Satırlar** hızlı sekmesinde seçili olan satın alma siparişi satırıyla ilgili ayrıntıları gösterir.
