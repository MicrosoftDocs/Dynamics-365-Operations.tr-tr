---
title: Seyahat konteynerlerini yönetme
description: Bu konu, seyahat konteynerleriyle nasıl çalışılacağını açıklamaktadır. Sevkiyat konteynerleri, fiziksel olarak gruplanmış malları bir araya getirmek için kullanılır. Ayrıca, genellikle fiziksel olarak birlikte oldukları için maliyetlerin yalnızca bu mallar arasında paylaşılması gereken durumlarda da kullanılırlar.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9b42292194d40f6b0cc6203130bedc1fbb45eec8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833821"
---
# <a name="manage-shipping-containers"></a>Seyahat konteynerlerini yönetme

[!include [banner](../../includes/banner.md)]

Sevkiyat konteynerleri, fiziksel olarak gruplanmış malları bir araya getirmek için kullanılır. Ayrıca, genellikle fiziksel olarak birlikte oldukları için maliyetlerin yalnızca bu mallar arasında paylaşılması gereken durumlarda da kullanılırlar.

Malları sevkiyat konteyneri sayfasından görüntülemek ve işlemek için **Varış yeri maliyeti \> Sevkiyat konteynerleri \> Tüm sevkiyat konteynerleri**'ne gidin. **Tüm sevkiyat konteynerleri** sayfasında mevcut tüm sevkiyat konteynerlerinin listesi gösterilir. Sevkiyat konteynerleri oluşturmak, silmek ve onlarla çalışmak için Eylem Bölmesindeki düğmeleri kullanabilirsiniz. Ayrıntılarını **Sevkiyat konteynerleri** sayfasında görüntülemek için listeden herhangi bir sevkiyat konteynerini seçin.

Sevkiyat konteyneri ayrıntıları sayfasının üst bölümünde sevkiyat konteyneri ve maliyet bilgileri gösterilir. **Satırlar** bölümünde, konteynere eklenmiş folyolar, maddeler ve satın alma siparişleri veya transfer emirleri gösterilir.

## <a name="action-pane"></a>Eylem Bölmesi

**Tüm sevkiyat konteynerleri** ve **Sevkiyat konteynerleri** sayfalarındaki Eylem Bölmesi, seçili bir sevkiyat konteyneriyle çalışmanıza olanak sağlayan düğmeler sağlar. Her düğme tek bir eylem gerçekleştirir. Eylem Bölmesi, her biri sırayla bir dizi ilgili düğme sağlayan sekmeler de içerir. Belirtilen durumlar dışında, aşağıdaki alt bölümlerde açıklanan tüm düğmeler ve sekmeler hem liste görünümünde (yani **Tüm sevkiyat konteynerleri** sayfasında) hem de ayrıntılı görünümde (yani **Sevkiyat konteynerleri** sayfasında) kullanılabilir.

### <a name="buttons-on-the-manage-tab"></a>Yönet sekmesindeki düğmeler

Aşağıdaki tabloda, doğrudan Eylem Bölmesinde bulunan **Yönet** sekmesindeki düğmeler açıklanmaktadır.

| Düğme | Açıklamalar |
|---|---|
| Girişler listesini deftere naklet | Giriş listesini deftere nakledin veya sevkiyat konteynerindeki tüm satın alma siparişi satırları için ürün girişi listelerini görüntüleyin. Çok şirketli sevkiyatlar kullanılırsa her şirket için yeni bir giriş listesi deftere nakil iletişim kutusu açılır. |
| Ürün girişini deftere naklet | Sevkiyat konteynerindeki tüm satın alma siparişi satırları için bir ürün girişini deftere nakledin. |
| Faturayı deftere naklet | Sevkiyat konteynerindeki tüm satın alma siparişi satırları için bir faturayı deftere nakledin. Çok şirketli sevkiyatlar kullanılırsa her şirket için yeni bir fatura deftere nakil iletişim kutusu açılır. |
| Sevk transfer emri | Sevkiyat konteynerindeki tüm transfer emri satırları için bir transfer emri sevkiyatını deftere nakledin. İletişim kutusunda yalnızca sevkiyat konteynerinde transfer emri türü olan satırlar görünür. |
| Transfer emrini al | Sevkiyat konteynerindeki tüm transfer emri satırları için transfer emri sevkiyatını deftere nakledin. Teslim alma iletişim kutusu, bir sevkiyat konteynerinde veya seyahatteki malları almanın en basit yoludur ve mevcut üç seçeneklerden biridir. Varış günlükleri veya mobil cihaz işlemesi yoluyla da alabilirsiniz. |
| Varış günlüğü oluştur | Gelişmiş ambar özelliklerini kullanarak kuruluşlar için bir varış günlüğü oluşturabilirsiniz. Seçenekler _Miktarı başlat_ (önerilir) ve _Transitteki mallar_ veya _Satın alma siparişlerinden oluştur_'dur. Son iki seçenek, transitteki malların işlemesinin kullanılıp kullanılmadığına bağlıdır. |
| Yeniden Adlandır | Seçili sevkiyat konteynerini yeniden adlandırabileceğiniz bir iletişim kutusu açar. |
| Seyahat şablonunu değiştir | Yolculuk şablonunu değiştirin. Yolculuk şablonunu değiştirdikten sonra, sevkiyat maliyetleri silineceğinden **Otomatik maliyetleri bul**'u seçmeniz veya maliyetleri el ile yeniden eklemeniz gerekebilir. |
| Kiralamaya dönüştür | Seçili bir sevkiyat konteynerini kiralama sevkiyat konteynerine dönüştürün. |

### <a name="buttons-on-the-general-tab"></a>Genel sekmesindeki düğmeler

Aşağıdaki tabloda, doğrudan Eylem Bölmesinde bulunan **Genel** sekmesinde açıklanmaktadır.

| Düğme | Açıklamalar |
|---|---|
| Giriş listesi | Sevkiyat konteynerindeki tüm satın alma siparişi satırları için bir giriş listesini deftere nakledin. Çok şirketli seyahatler kullanılırsa her şirket için yeni bir giriş listesi deftere nakil iletişim kutusu açılır. |
| Ürün Girişi | Kullanılıyorsa ürün girişi kaydını görüntüleyin. Ürün giriş işlemi yalnızca mallar transitteki mallar işlevini kullanmazsa kullanılır. |
| Madde varışı | Bu günlük kullanılıyorsa sevkiyat konteyneri için madde varış günlüğünü görüntüleyin. |
| Duraklar | Duraklar bir yolculuğun ayrı kısımlarını tanımlamak için kullanılır. Sevkiyat izlemeye yardımcı olmak için sağlama süreleri her durakla ilişkilendirilebilir. Daha fazla bilgi için bkz. [Çok duraklı yolculuk kurulumu](multi-leg-journey-setup.md). |
| İzleme | Sevkiyat izlemeyi görüntüleyin veya güncelleştirin. |
| Transitteki mal siparişleri | **Transitteki mallar** sayfasını doğrudan konteynerden açabilirsiniz. Bu sayfa, yalnızca seçili sevkiyat konteyneri için transitteki mal kayıtlarını gösterir. |

## <a name="header-view"></a>Başlık görünümü

**Başlık** görünümünü açmak için bir sevkiyat konteyneri açın ve sevkiyat konteyneri başlığının sağ üst sekmesindeki **Başlık** sekmesini seçin.

### <a name="settings-on-the-general-fasttab"></a>Genel hızlı sekmesindeki ayarlar

Aşağıdaki tabloda, sevkiyat konteynerinin **Başlık** görünümünün **Genel** hızlı sekmesinde bulunan ayarlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Sevkiyat konteyneri | Sevkiyat konteynerinin adı. |
| Seyahat | Sevkiyat konteyneriyle ilişkilendirilen seyahat. |
| Sevkiyat konteyneri türü | Sevkiyat konteyneri türünü girin. Bu alan ayarlanmalıdır. Örneğin, sevkiyat konteyneri türüyle ilişkili otomatik maliyeti seçerek navlun maliyetini belirlemek için kullanabilirsiniz. |
| Tekne | Gemiyi girin veya seçin. Gemi bir değer olarak listelenmiyorsa, gemi kimliğini serbest metin olarak girebilirsiniz. Bu durumda, ana tablo güncelleştirilmez, böylece gemi kimliği daha sonra bu alanda seçilebilir. Daha fazla bilgi için bkz. [Gemiler](shipping-information-setup.md#vessels). |
| Birim türü | Birim tipleri, sevkiyat konteynerlerini gruplandırmak ve tanımlamak için ek bir araç olarak kullanılır. Sevkiyat konteyneri sayfasında gösterilir ve seçilir. Daha fazla bilgi için bkz. [Birim türlerini ayarlama](shipping-container-setup.md#unit-types). |
| Soğutma türü | Soğutma türleri, genellikle soğutmalı konteynerler olan sevkiyat konteynerlerini gruplandırmak ve tanımlamak için ek bir araç olarak kullanılır. Sevkiyat konteyneri sayfasında gösterilir ve seçilir. Daha fazla bilgi için bkz. [Soğutma türlerini ayarlama](shipping-container-setup.md#refrigeration-types). |
| Ölçüm | Bu alan, bir ölçümün **Varış yeri maliyeti** modülünde belirtilmesini sağlar. Ölçümler genellikle malların tek tek hacmini veya ağırlığını bilmeyen ancak tutarın veya miktarın sağladığından daha doğru bir onay gerektiren kuruluşlar tarafından kullanılır. Navlun ileticisi kilogram cinsinden ağırlık veya kübik ölçümü sağlar ve bunu bir madde veya satın alma siparişi düzeyine yerleştirebilirsiniz. Parametre seçilirse veya el ile girilirse otomatik olarak güncelleştirilebilir. |
| Ölçüm birimi | **Ölçüm** alanındaki sayı için geçerli ölçü birimi. |
| Gerçek ağırlık | Kartonun veya konteynerin gerçek ağırlığını kaydedebilirsiniz. Bu değer, bir sevkiyat konteynerinin kurulumunda izin verilen maksimum ağırlığa karşı doğrulama için kullanılabilir. |
| Karton sayısı | Parametre seçilirse karton sayısı otomatik olarak güncelleştirilir. |
| Malların açıklaması | Sevkiyat konteynerinde veya folyo başlığında malların açıklaması seçilebilir. Bir seyahatin, sevkiyat konteynerinin veya mal folyosunun tanımlanmasına yardımcı olmak için kullanılır. Daha fazla bilgi için bkz. [Malların açıklaması](shipping-information-setup.md#description-of-goods). |
| Ara irsaliye/Konşimento | Sevkiyat konteyneri için ara irsaliye veya konşimento belirtebilirsiniz. |
| Açıklamalar | Sevkiyat konteyneri ile ilgili ek bilgiler. |
| İade edilebilir | Sevkiyat konteynerinin seyahatten sonra iade edilip edilmeyeceğini gösteren bir değer. |
| Seyahat durumu | Sevkiyat konteyneri ile ilişkili yolculuğun durumu. |
| Satın alma siparişi durumu | Sevkiyat konteyneriyle ilişkili satın alma siparişinin durumu. |

### <a name="settings-on-the-delivery-fasttab"></a>Teslimat hızlı sekmesindeki Ayarlar

Aşağıdaki tabloda, sevkiyat konteynerinin **Başlık** görünümünün **Teslimat** hızlı sekmesinde bulunan ayarlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Oluşturulma tarihi ve saati | Konteynerin oluşturulduğu tarih ve saat. |
| Fabrikadan çıkış tarihi | Bu tarih genellikle malların tesislerinden ne zaman çıkmasını beklediğinizi belirtmek için fabrikaya/satıcıya sağlanır. Asya'daki bir fabrikayla çalışırken, malları beklediğiniz tarih yerine genellikle bu tarih gereklidir. (Bunun aksine, yerel bir teslimat için malları beklediğiniz tarih gereklidir.) Bu alan, sevkiyat konteyneri listesindeki satın alma siparişi satırlarından doldurulabilir. Buraya el ile de girebilirsiniz. |
| Sevk tarihi | Bu tarih satın alma siparişi belgesine yazdırılabilir. Genellikle fabrikayı/satıcıyı malların limana teslim edilmesi gereken tarih hakkında bilgilendirir. Bu alan yalnızca bilgi amaçlıdır. Sevkiyat konteynerinde malların beklenen teslimat tarihini tahmin etmek için kullanılmaz. Bu alan, izleme denetimi sayfası güncelleştirildiğinde otomatik olarak güncelleştirilecek şekilde ayarlanabilir. |
| Depoya giriş tarihi | Seyahate bağlı satın alma siparişlerinden malların satışa sunulacağı en erken tarih.|
| Tahmini teslim tarihi | Genellikle, malların ambara varması gereken tarih. Bu alan yalnızca bilgi amaçlıdır. Sevkiyat konteynerindeki satın alma siparişi satırlarındaki master planlamayı hesaplamak için kullanılmaz. Satın alma siparişi satırlarında beklenen teslimat tarihi izleme denetimi aracılığıyla güncelleştirilir. Bu alan, izleme denetimi sayfası güncelleştirildiğinde güncelleştirilecek şekilde ayarlanabilir. |
| Yola çıkış tarihi | Genellikle, uçağın veya geminin denizaşırı limandan ayrıldığı tarih. |
| Sevkiyat limanındaki ETA | Hedef limana ("varış" limanı) tahmini varış tarihi. |
| Alınan orijinal belgeler | İsteğe bağlı: Orijinal belgelerin alındığı tarihi güncelleştirin. |
| Aracı tarafından önerilir | İsteğe bağlı: Aracının tavsiye edildiği tarihi güncelleştirin. |
| Gönderilen orijinal konşimento | İsteğe bağlı: Orijinal konşimentonun gönderildiği tarihi güncelleştirin. |
| Piyasaya sürülen mallar | İsteğe bağlı: Malların piyasaya sürüldüğü tarihi güncelleştirin. |
| Müşteri randevusu | İsteğe bağlı: Müşteri randevusu tarihini güncelleştirin. |
| Ambara teslim edildi | İsteğe bağlı: Malların ambara teslim edildiği tarihi güncelleştirin. |
| Doğrulama tarihi | İsteğe bağlı: Doğrulama tarihini güncelleştirin. |
| Teslimat talimatları | İsteğe bağlı: Teslimat talimatlarının tarihini güncelleştirin. |
| Çıkış limanı | Maddelerin sevk için alınacağı çıkış limanı. |
| Varış limanı | Maddelerin sevk edileceği varış limanı. |
| Yerel aracı | Bu alan yalnızca bilgi amaçlıdır. Yerel iletici satıcı tablosundan seçilebilir olmalıdır. |
| Yerel taşıma tarihi | Yerel taşımanın rezerve edildiği tarihi girin. Bu alan, ambarın planlamasını yapmasına yardımcı olabilir. |
| Yerel taşıma saati | Saat ve süreyi girin. Bu alan, ambarın planlamasını yapmasına yardımcı olabilir. |
| Yolculuk şablonu | Seyahat için belirtilen yolculuk şablonu. Yolculuk şablonu, "varış" ve "çıkış" limanlarının ayrıntılarını ve sevkiyat konteynerinin izleme denetimiyle ilişkili sağlama sürelerini sağlar. |

### <a name="settings-on-the-other-fasttab"></a>Diğer hızlı sekmedeki ayarlar

Aşağıdaki tabloda, sevkiyat konteynerinin **Başlık** görünümünün **Diğer** hızlı sekmesinde bulunan ayarlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Kiralık | Sevkiyat konteynerinin kiralık bir sevkiyat konteyneri olup olmadığını gösteren değer. Kiralama maliyetleri kiralık konteynerlerle ilişkili olabilir. |
| Kiralamaya dönüştürüldü | Sevkiyat konteynerinin kiralık bir sevkiyat konteynerine dönüştürülüp dönüştürülmediğini gösteren değer. Kiralama maliyetleri kiralık konteynerlerle ilişkili olabilir. |
| Orijinal seyahat | Sevkiyat konteyneri yeni bir seyahate taşındıysa orijinal yolculuk. |
| Kullanılan | Kiralık bir sevkiyat konteyneri kullanılıp kullanılmadığını kaydetmek için bunu kullanın. Bu, yalnızca bilgi amaçlıdır. |
| Beklenen yükleme tarihi | Sevkiyat konteynerine mal yüklenmesinin beklendiği tarih. |
| Seri numaramız | Şirketinizin sevkiyat konteyneri için dahili olarak kullandığı seri numarasını girin. |
| Sevkiyat şirketi seri numarası | Sevkiyat şirketinin veya acentesinin sevkiyat konteyneri için sağladığı seri numarasını girin. |
| Muayene belgesinin geçerli olduğu tarih | Sevkiyat konteyneri için inceleme talep edilen tarih. |
| Muayene belgesinin alınma tarihi | İnceleme sertifikasının alındığı tarih. |
| Muayene belgesinin sona erme tarihi | İnceleme sertifikasının sona ereceği tarih. |
| Muayene belgesi numarası | Bir inceleme yapıldıktan sonra verilen sertifikanın sertifika numarası. |

## <a name="lines-view"></a>Satırlar görünümü

**Satırlar** görünümünü açmak için bir sevkiyat konteyneri açın ve sevkiyat konteyneri başlığının sağ üst sekmesindeki **Satırlar** sekmesini seçin.

### <a name="information-on-the-shipping-container-fasttab"></a>Sevkiyat konteyneri hızlı sekmesi hakkında bilgi

**Satırlar** görünümündeki **Sevkiyat konteyneri** hızlı sekmesi, folyo hakkındaki bilgileri gösterir. Bu bilgilerin çoğu, bu konuda daha önce açıklandığı gibi **Başlık** görünümünde de görünür.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Satırlar hızlı sekmesindeki bilgiler ve düğmeler

**Satırlar** görünümündeki **Satırlar** hızlı sekmesi, geçerli sevkiyat konteynerine dahil edilen her tam veya kısmi satın alma siparişi satırıyla ilgili ayrıntıları gösterir.

Aşağıdaki tabloda, **Satırlar** görünümündeki **Satırlar** hızlı sekmesinde yer alan düğmeler açıklanmaktadır.

| Düğme | Tanım |
|---|---|
| Kaldır | Seçili satın alma siparişi satırını seyahatten kaldırın. |
| Stok \> Hareketler | Seçili satın alma siparişi satırı için stok hareketlerini görüntüleyin. Transitteki malları kullanıyorsanız orijinal siparişin ve transitteki malların da gösterildiğini unutmayın. |
| Stok \> Görüntüleme boyutları | Görüntülediğiniz hareketler için görünen stok boyutlarını seçebileceğiniz bir iletişim kutusu açar. |
| Yenile | Seçili satın alma siparişi satırının satır tutarı, ağırlığı veya hacmiyle ilgili bilgileri güncelleştirin. |

### <a name="information-on-the-lines-details-fasttab"></a>Satır ayrıntıları hızlı sekmesi hakkında bilgi

**Satırlar** görünümündeki **Satır ayrıntıları** hızlı sekmesi, **Satırlar** hızlı sekmesinde seçili olan satın alma siparişi satırıyla ilgili ayrıntıları gösterir.
