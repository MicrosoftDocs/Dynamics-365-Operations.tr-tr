---
title: Gizli üretimle ilgili sorunları giderme
description: Bu konuda, gizli üretim ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b0073cb2c3e3d6b9218caf20c394c8c0ca67b796
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966217"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Gizli üretimle ilgili sorunları giderme

Bu konuda, gizli üretim ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Şu hata iletisini alıyorum: "Ambar yönetim süreçleri şu anda kullanılmaktadır. Çalışma satırları henüz kaydedilmemişse, oluşturulan çalışmayı ve herhangi bir yük veya sevkiyat satırını iptal edebilir ve ardından malzeme çekme veya sevkiyat sürecine devam edebilirsiniz."

### <a name="issue-description"></a>Sorun açıklaması

Bu sorun, bir satır için çalışmayı ayırmaya veya serbest bırakmaya çalışırsanız oluşur ancak stok hareketinin, malzemenin alındığını gösteren *Teslim Alındı* durumu vardır.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorunu düzeltmek için şu adımlardan birini izleyin.

- Üretim siparişinin durumunu *Tahmini* veya *Serbest Bırakılmış* olarak değiştirin.
- İlgili üretim emrinin ayrıntılar sayfasını açın. Eylem bölmesinde, **Ambar** sekmesinde, **Durdurma** grubunda, tüm teslim alınmış hareketlerin çekme işlemini iptal etmek için **Durdur ve çekmeyi iptal et**'i seçin. Ardından, üretim emrini işlemek için **Durdurmayı kaldır**'ı seçin.

Burada *Çekmeyi iptal et* ve *Durdur* işlevlerinin açıklaması verilmiştir:

- **Çekmeyi iptal et**: Bu işlev, sipariş üzerine *Teslim Alındı*'dan *Siparişte*'ye kadar durumu olan ürün reçetesi satırları ve formül satırları için stok hareketlerinin durumunu tersine çevirir. Ham madde teslim alma işi tamamlandığında, satırların durumu *Teslim Alındı* olarak ayarlanır. Bu durum, üretim emrinin *Oluşturuldu* durumuna sıfırlanmasını önler. Bu durumda, *Teslim Alındı* durumdaki hareketleri geri almak ve ardından üretim emrini *Oluşturuldu* durumuna sıfırlamak için *Çekmeyi İptal Et* işlevini kullanabilirsiniz.
- **Durdur**: Bu işlev, siparişte herhangi bir durum güncelleştirmesini önlemek için üretim emrinde **Durduruldu** işareti ayarlar. Üretim emri ayrıntıları sayfasının **Ambar** hızlı sekmesinde **Durduruldu** işaretini bulabilirsiniz.

> [!NOTE]
>
> - Düğmeler yalnızca ambar işlemleri için etkinleştirilen maddeler için üretim emri oluşturulduğunda görünür.
> - **Durdur** grubu yalnızca üretim sırası ayrıntıları sayfasının Eylem bölmesindeki **Ambar** sekmesinde görünür. **Üretim emirleri** listesi sayfasının **Ambar** hızlı sekmesinde görünmez.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>Genel adres defterinde bir çalışan adını değiştirdikten sonra eşleşen kaynak adı güncelleştirilmiyor.

### <a name="issue-description"></a>Sorun açıklaması

Genel adres defterinde bir çalışan adını değiştirirseniz eşleşen kaynak adı, ana kaynak grubunda güncelleştirilmez.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu senaryo şu anda desteklenmiyor. Sorunu gidermek için kaynak adını el ile güncelleştirmeniz gerekir.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Yeni bir üretim emri oluşturduğumda, şu iletiyi almıyorum: "Ürün reçetesi ve rotanın etkin sürümünü ekleyin?"

### <a name="issue-description"></a>Sorun açıklaması

Yeni bir üretim emri oluşturduğunuzda, madde numarasını girdikten sonra **Tesis** ve **Ambar** alanları, otomatik olarak tamamlanan mallar için **Varsayılan sipariş ayarları** sayfasında tanımlanan varsayılan tesis ve ambara ayarlanır. Ayrıca, etkin ürün reçetesi ve rota numarası otomatik olarak girilir. Bu değerler için sizi uyaran şu iletiyi almazsınız:

> Ürün reçetesi ve rotanın etkin sürümünü ekleyin?

### <a name="issue-resolution"></a>Sorunun çözümü

**Varsayılan sipariş ayarları** sayfasında bir tesis ve ambarın tanımlandığı bir ürün seçerseniz ürün reçetesi ve rota numaralarını eklemeniz istenmez. Yalnızca bu değerler seçili ürün için tanımlanmamışsa istenir.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Üretim emirleri İşaretleme sayfasında gösterilmiyor.

### <a name="issue-description"></a>Sorun açıklaması

Bazı üretim emirleri **İşaretleme** sayfasında gösterilmez.

### <a name="issue-resolution"></a>Sorunun çözümü

Aşağıdaki yapılandırmaya sahip ürünler işaretleme için kullanılamaz. Bu nedenle, **İşaretleme** sayfasında gösterilmez:

- Ürünler, *fiili ağırlık* tipi ürünler olarak tanımlanır.
- Bunlar gelişmiş ambar işlemleri için etkinleştirilir.
- *Standart maliyet* ilkesi tarafından denetlenecek şekilde yapılandırılırlar.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Üretim emrini sona erdirmeye çalıştığımda, aşağıdaki hata iletisini alıyorum: "Ürün reçetesinin consumptionCost değerinin hesaplanması, stoktan çıkıştan sonra negatif olmalıdır."

Bu sorun 10.0.15 sürümünde giderilmiştir.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Üretim emrinin durumu Bildirildi'den Bitiş'e değiştirildiğinde, aşağıdaki hata iletilerini alıyorum: "Çakışmayı güncelleştirin. Standart maliyet, güncelleştirmeden sonra finansal stok değeriyle eşleşmiyor" ve "InventCostMovement.checkVariance işlevinde kritik bir hata oluştu."

Bu sorun, temel veriler başka bir işlem tarafından değiştirildiğinde oluşur. İşlem, verileri en fazla beş kez güncelleştirmeyi deneyecektir. Çakışma beş denemeden sonra hala varsa, aşağıdaki hata iletilerini alırsınız:

> Çakışmayı güncelleştirin. Standart maliyet, güncelleştirmeden sonraki mali stok değeriyle eşleşmez.

> InventCostMovement.checkVariance işlevinde kritik bir hata oluşur.

Bu davranış tasarımdan kaynaklanır. Sorunu gidermek için toplu işi sürdürün. Çalıştırmayı sonlandırmalıdır.

Toplu iş, siz devam ettikten sonra sürekli olarak başarısız olursa, kayıt defterinin varsayılan para biriminin yuvarlama hassasiyetinin InventSum tablosundaki değerlere uygulanan yuvarlama ile uyumlu olduğunu doğrulayın. Yuvarlama hassasiyeti uyumlu olmayan bir değere değiştirildiyse büyük olasılıkla uyumlu bir değere değiştirmeniz gerekir. **ModifiedDateTime** değerini arayın. Bu durumda, değer genellikle yuvarlama hassasiyetinin son zamanlarda değiştirildiğini gösterir.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Bir ambara serbest bırakma işlemi yaptığımda, aşağıdaki hata iletisini alıyorum: "RM maddesi tam olarak ayrılmadı. Tam miktarın kullanılabilir olduğundan emin olun veya ürün reçetesi satırındaki Ayırma alanı El İle veya Başlatıldı olarak ayarlanmışsa maddeleri el ile ayırın. Bazı malzemeler rezerve edilemediğinden sipariş ambara serbest bırakılamadı." Ancak durum Serbest Bırakıldı olarak güncelleştiriliyor.

### <a name="issue-description"></a>Sorun açıklaması

Bir üretim emri serbest bırakıldığında tüm ürün reçetesi satır öğeleri fiziksel olarak kullanılamıyorsa ve **Ambara serbest bırakma** ilkesi üretim emrinde *Tam ayırma gerektir* olarak ayarlanmışsa, aşağıdaki hata iletisini alırsınız:

> RM maddesi tam olarak ayrılmadı. Tam miktarın kullanılabilir olduğundan emin olun veya ürün reçetesi satırındaki Ayırma alanı El İle veya Başlatıldı olarak ayarlanmışsa maddeleri el ile ayırın. Bazı malzemeler rezerve edilemediğinden sipariş ambara serbest bırakılamadı.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış tasarım gereğidir ve beklendiği gibi çalışmaktadır.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Bir üretim siparişini sona erdirmeye ve tamamlanmış olarak bildirmeye çalıştığımda, aşağıdaki hata iletisini alıyorum: "Üretimde mamul olarak rapor edilen toplam sağlam miktar %1 olacak. Son işlem için geri bildirim toplamı 0,00'dır."

### <a name="issue-description"></a>Sorun açıklaması

Bir raporu üretim emrinde tamamlanmış günlük olarak deftere nakletmeye çalıştığınızda, aşağıdaki hata iletisini alırsınız:

> Üretimde mamul olarak rapor edilen toplam sağlam miktar %1 olacak. Son işlem için geri bildirim toplamı 0,00'dır.

### <a name="possible-cause"></a>Olası neden

Bu sorun, son işlemlerde deftere nakledilen miktarlar yanlışsa oluşur. Örneğin, üretim başlatıldıysa ancak başlatılması gereken miktar tahsis edilmediyse rota kartı günlüğü herhangi bir satır olmadan deftere nakledilir. Durumu onaylamak için üretim emrini açın ve ardından Eylem Bölmesi'nde, **Görünüm** sekmesinde **Rota kartı**'nı seçin.

### <a name="workaround"></a>Geçici çözüm

Bu sorunu, günlüklerin deftere doğru şekilde nakledilmediği işlemler için ek günlükler göndererek düzeltebilirsiniz. Üretim emrini yeniden başlatın ve ek günlükleri deftere nakletmeyi seçin. Bu eylem üretim emrini başlatmaz ancak günlükleri deftere nakleder. Rota kartı deftere nakledilen miktarları göstermelidir ve üretim emirlerini başarıyla sonlandırabilirsiniz.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Hata miktarını raporlarken bir üretim emrini bitmiş olarak bildirebilir fakat süreyi veya malzeme miktarını raporlarken bildiremez miyim?

İyi miktarı da bildirmediğiniz sürece hata miktarını üretim emrinde bildiremezsiniz. Bu senaryo **desteklenmez**. Tamamlanmış güncelleştirme olarak bildir, üretim emrini sona erdirmeye çalıştığınızda başarısız olur ve aşağıdaki hata iletisini alırsınız:

> Eksik tamamlandı bildirimi miktarı.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Bitmiş malların seri numaralarını tüketilen malların seri numaralarıyla karşılaştırıp takip edebilir miyim?

Bitmiş malların seri numaralarını, bir üretim emrinin bu bitmiş malları yapmak için tükettiği malzemenin seri numaralarıyla karşılaştırarak izleyebilirsiniz. Bu senaryo şu anda desteklenmiyor. Geçici çözüm, 1 miktarı için üretim emirleri oluşturmaktır.
