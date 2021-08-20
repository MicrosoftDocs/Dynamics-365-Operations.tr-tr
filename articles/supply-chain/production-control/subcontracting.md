---
title: Alt sözleşme
description: Bu konu, Dynamics 365 Supply Chain Management içinde üretimde taşeron kullanımın için bir inceleme rehberi yapmanıza olanak sağlar.
author: christophernread
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 678256a301a34f354a1fbf7844f5e3de0ad7e882b5d68c5d0310abcdea4a97de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778615"
---
# <a name="subcontracting"></a>Alt sözleşme

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta üretimde alt sözleşme için bir kılavuz yapmanıza yardımcı olur. Bu konunun ilk bölümü veri kurulumunu açıklar. İkinci bölüm, gözden geçirme adımlarını anlatır.

## <a name="target-audience"></a>Hedef kitle

Bu konu, üretimde alt sözleşme oluşturmayı öğreneceksiniz. Bir taşeron etkinlik akışı temel kurulumu yapmak için HQUS tüzel içinde varolan verileri kullanacaksınız. HQUS tüzel varlığındaki demo verisi, gözden geçirmedeki adımları desteklemek üzere önceden ayarlanmış kurulum parametrelerine sahiptir. Gözden geçirme, çeşitli roller için sorunlu noktaları ve zorlukları ele alsa da, bu sistem yöneticisi tarafından tamamlanabilir.

## <a name="demo-scenario"></a>Gösteri senaryosu

HQUS tüzel varlığında, yüksek kaliteli hoparlörler üretilmektedir. Üretim işlemi sırasında, hoparlörler aşağıdaki üç işlemden geçer.

- **Ön montaj** – hoparlörü kabini birleştirilir. Kabin için malzemeler, işlem başlamadan önce malzeme deposundan çekilir.
- **Kaplama** – hoparlörü kabini birleştirildikten sonra kaplanması gerekir. Bu işlem bir bir satıcı (alt yüklenici) tarafından gerçekleştirilir. Önceden oluşturulmuş hoparlör kabini ile birlikte iki malzeme kaplama alt yüklenici çoğuyla birlikte gelmektedir.
- **Sonlandırma** – önceden birleştirilmiş hoparlörü kabininin alt yüklenici tarafından kaplanmasından sonra montajın tamamlanması için hoparlörü kabinini alt yüklenici tarafından HQUS tüzel varlığına döndürülür.

Aşağıda, tüketim malzemelerini ve üç işlemi gösterir.

![Ön montaj, Kaplama ve Bitiş işlemleri ve bunların tükettiği malzemeler.](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Ayar

Gözden geçirmeye başlamadan önce, verileri ayarlamanız gerekir.

### <a name="set-up-the-finished-product"></a>Tamamlanmış ürünü ayarlama

Bu yordam, serbest bırakılan ürün D8100'ün "Kaplamalı Kabin" kurulumunu ele alır.

1. **Serbest bırakılan ürün ayrıntıları** sayfasını açmak için **Ürün bilgi yönetimi \>Ürünler \> Serbest bırakılan ürünler**'i seçin.
2. Hızlı filtre alanına varolan serbest ürünü bulmak için **D8100** girin.

    ![Serbest bırakılan ürün ayrıntıları sayfasında serbest bırakılan ürün D8100'ü filtreleme.](./media/subcontract02_filtering-released-products.png)

3. Eylem Bölmesi üzerinde **Mühendis** sekmesinde, **Yol** sayfasını açmak için **Yol**'u seçin.

    **Yol** sayfası, serbest bırakılan ürün D8100 için sekiz rota sürümlerini gösterir. Sekiz rota sürümü, tesis 1 ve tesis 5 üzerinde bölünmüş dört rotayı gösterir. Rota 000400 kullanılan maliyetlendirme, rota 00041 kaplama operasyonun dahili bir işlemdir olması durumunda ve rota 00042 kullanılan kaplama operasyon harici bir işlemi olduğunda kullanılır.

    ![Rota sayfasında sekiz Rota sürümü.](./media/subcontract03_route-page.png)

4. Üst bölmede, **Sürümler** kılavuzunda, tesis **5** için rota versiyonunu **00042** seçin.
5. Alt bölmede, **Genel Bakış** sekmesinde, kılavuzda **20** (**Cbnt CtSc**) seçin.

    ![Tesis 5 için rota sürümü 00042 için operasyon 20 seçili.](./media/subcontract04_route-version-operation.png)

6. **Genel** sekmesini seçin.

    **Rota türü** alanının **Satıcı** olarak ayarlanmış olmasına dikkat edin. Bu değer operasyon 20'nin (Cbnt CtSc) bir taşeron operasyonu olduğunu gösterir.

    ![Rota türü alanı, Genel sekmesinde Satıcı olarak ayarlı.](./media/subcontract05_general-tab.png)

7. **Kaynak gereksinimleri** sekmesini seçin.

    Yeterlilikler, üretim iş planlama çizelgeleme sırasında geçerli bir kaynağı bulmak için kullanılır. Operasyon 20 için (Cbnt CtSc), kaynağın iki yeteneği olduğuna dikkat edin, **Kaplama** ve **Kaplanmış kabinler**, gereklidir.

    ![Kaynak gereksinimleri sekmesinde Kaplama ve Kaplamalı kabinler özellikleri.](./media/subcontract06_resource-requirements-tab.png)

8. **Uygun kaynaklar**'ı **Uygun kaynakları** iletişim kutusunu açmak için seçin.

    Operasyon için kaynak gereksinimleriyle eşleşen üç kaynak bulundu. Kaynaklar 8851 ve 8852'nin **Satıcı** türünde olduğunu unutmayın.

    ![Uygun kaynaklar iletişim kutusunda üç uygun kaynak.](./media/subcontract07_applicable-resources-dialog.png)

9. **Tamam**'ı seçin, kapatmak için **Uygun kaynaklar** iletişim kutusunu ve **Rota** sayfasına dönmek için.
10. **Serbest bırakılan ürün ayrıntıları** sayfasına dönmek için **Yol** sayfasını kapatın.

    ![Serbest bırakılan ürün ayrıntıları sayfası.](./media/subcontract08_released-product-details-page.png)

11. Eylem Bölmesi üzerinde **Mühendis** sekmesinde, **Ürün Reçetesi sürümleri** sayfasını açmak için **Ürün Reçetesi sürümleri**'ni seçin.

    **Ürün reçetesi sürümleri** sayfası serbest bırakılan ürün D8100 için dört ürün reçetesi (BOM) sürümlerini gösterir. Ürün reçetesi 000040 planlama ve maliyetlendirme, şirket içinde kaplama işlemi yapılıyorsa ürün reçetesi 000041 ve kaplama işlemi taşeron tarafından yapılıyorsa 000042 ve 000043 ürün reçeteleri kullanılır.

    Öğe S8050'ni bir **servis** öğesi türü olduğunu unutmayın. Bu madde, alt sözleşmeli işi temsil eder.

    ![Ürün reçetesi versiyonları sayfasında dört ürün reçetesi sürümü.](./media/subcontract09_bom-versions-page.png)

12. **Ürün reçetesi satırları** hızlı sekmesinde, **Düzenle ürün reçetesi satırı** iletişim kutusunu açmak için **Düzenle** üzerine tıklayın.

    Serbest bırakılan ürün D8100 için bir üretim emri oluşturulduğunda ve tahmini yapıldığında, bir satınalma emri otomatik olarak öğe S8050 için oluşturulur. Bu satınalma siparişi üretim emrine bağlanır. Otomatik olarak oluşturulacak, satınalma siparişleri için **Satır türü** alanının **Satıcı** olarak ayarlanması ve alt yüklenici için satıcı hesabının seçilmesi gerekir. Bu durumda, satıcı ABD-801 hesabıdır.

    Ürün reçetesi satırının operasyon numarası (Bu durumda, 20) aracılığıyla kaplama işlemi bağlı olduğu dikkat edin.

    ![Ürün reçetesi iletişim kutusunu düzenleme.](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Ambar çalışanları için bir parola oluşturun

El cihazı kullanan ambar çalışanları için bir parola tanımlamalısınız.

1. **Çalışma kullanıcıları** sayfasını açmak için **Ambar yönetimi \>Kurulum \> Çalışan** seçin.
2. **Kullanıcılar** hızlı sekmesinde, kullanıcı **51** için satırı seçin.

    ![İş kullanıcıları sayfası.](./media/subcontract11_work-users-page.png)

3. **Parola sıfırlama**'yı seçin.
4. **Parola** ve **Parolayı onayla** alanlarına **1** girin.
5. **Parola ayarlama**'yı seçin.

## <a name="step-by-step-walkthrough"></a>Adım adım gözden geçirme

**Senaryo ve arka plan**

Ürün D8100 "Kaplamalı Kabin" için 10 adetlik bir üretim emri oluşturulur. Kabinlerin kaplaması, satıcı ABD-801 Mükemmel Kaplama Çözümleri'nde gerçekleştirilen bir alt sözleşmeli iştir. Üretim emri üç işlemden oluşur. İlk işlemde kabin şirket içi operasyon olarak önceden bir araya getirilir. Ön montaj için hammadde ambarında çekme için serbest bırakılır. Ön montaj işleminden sonra önceden oluşturulmuş kabin, Mükemmel Kaplama Çözümleri'nde kaplama çalışması için gerekli olan iki malzeme ile birlikte gönderilir. Kaplanmış kabin satıcıdan geri geldiğinde, tamamlanmış olarak raporlanmadan önce şirket içi son montaj işleminden geçer.

1. **Tüm üretim emirleri** sayfasını açmak için **Üretim kontrolü \> Üretim emirleri \> Tüm üretim emirlerini**'ni seçin.
2. Eylem bölmesinde, **Yeni üretim emri**'ni, **Üretim emri oluştur** iletişim kutusunu açmak için seçin.

    ![Üretim emri iletişim kutusu oluşturma.](./media/subcontract12_create-production-order-dialog.png)

3. **Öğe numarası** alanında, **D8100**'yi seçin.
4. Öğe numarasını seçtikten sonra, stok boyutları için alanlar belirir. **Renk** alanında, **Krom** seçin.

    Ürün reçetesi ve rota için etkin sürümlerin yerleştirilmesini soracak bir ileti kutusu görünür.

    ![İleti kutusu.](./media/subcontract13_message-box.png)

5. **Evet**'i seçin. 

    **Üretim emri oluştur** iletişim kutusunda, ürün D8100 için ürün reçetesi ve rota için etkin sürümler otomatik olarak **Ürün reçetesi numarası** ve **Rota numarası** alanlarında sırasıyla otomatik olarak seçilir. Bu durumda, ürün reçetesi **000040** ve rota **000040** seçilir.
    
    > [!NOTE]
    > Ürün reçetesi ve rota için sürüm 000040 planlama ve maliyetlendirme için kullanılır.

6. **Site** alanında, **5**'i seçin.
7. **Ambar** alanında **51**'i seçin.
8. **Ürün reçetesi numarası** ve **Rota numarası** alanlarında, otomatik olarak **000042** olarak seçilen değeri değiştirin.

    > [!NOTE]
    > Ürün reçetesi ve rota için sürüm 000042, kabinin kaplamasını satıcı ABD-801'e alt sözleşmeli vermek için kullanılır.

    ![Üretim emri oluştur iletişim kutusunda ayarlanan değerler.](./media/subcontract14_create-production-order-dialog-set.png)

9. Üretim emri oluşturmak ve **Tüm üretim emirleri** sayfasına dönmek için **Oluştur**'u seçin.

    ![Tüm üretim emirlerini sayfasında yeni üretim emri.](./media/subcontract15_new-production-order.png)

10. Eylem bölmesinde, **Üretim emri** sekmesinde, **Tahmin** iletişim kutusunu açmak için **Tahmin**'i seçin.

    ![Tahmin iletişim kutusu.](./media/subcontract16_estimate-dialog.png)

11. Tahmini onaylamak ve **Tüm üretim emirleri** sayfasına dönmek için **Tamam**'ı seçin.

    > [!NOTE]
    > Üretim emri tahmini yaptığınızda, servis maddesi S8050 için satınalma siparişi, satıcı ABD-801 için oluşturulur.

12. Eylem Bölmesi üzerinde, **Üretim emri** sekmesinde, üretim emri için Ürün Reçetesi satırlarını görüntüleyebileceğiniz **Ürün reçetesi** sayfasını açmak için **Ürün reçetesi**'ni seçin.

    Servis maddesi S8050 için üretim emri tahmini yapıldığında oluşturulan satınalma siparişi için bir referans olduğuna dikkat edin.

    ![Ürün reçetesi sayfasındaki Üretim emri Ürün reçetesi satırları.](./media/subcontract17_production-order-bom-lines.png)

13. **Tüm üretim emirleri** sayfasına dönmek için **Ürün reçetesi** sayfasını kapatın.
14. Eylem bölmesinde, **Planlama** sekmesinde, **İş planlama** iletişim kutusunu açmak için **Planlanan işler**'i seçin.
15. Aşağıdaki değerleri belirtin:

    - **İş planlama çizelgeleme yönü** alanında **Yarından ileriye doğru**'yu seçin.
    - **Sınırlı kapasite** seçeneğini **Evet** olarak ayarlayın.

    ![İş planlama iletişim kutusu.](./media/subcontract18_job-scheduling-dialog.png)

16. **Tamam**'ı seçin, kapatmak için **İş planlama** iletişim kutusunu ve **Tüm üretim emirleri** sayfasına dönmek için.
17. Eylem Bölmesinde, **Planlama** sekmesinde, **Gannt grafiği - kaynak görünümü**'nü açmak için **Gannt**'ı seçin.

    Gantt şeması, kaynaklar üzerinde üretim işlerinin nasıl zamanlandığına dair görsel bir bakış gösterir. Dış kaplama işleminin üç işi içerdiğine dikkat edin: bir işlem işi, bir nakliye işi ve bir kuyruk işi.

    ![Gannt şeması üzerindeki Gannt şeması - Kaynak görüntüleme sayfası.](./media/subcontract19_gantt-chart.png)

18. **Tüm üretim emirleri** sayfasına dönmek için **Gannt şeması - Kaynak görünümü** sayfasını kapatın.
19. Eylem bölmesinde, **Üretim emri** sekmesinde, **Serbest bırak** iletişim kutusunu açmak için **Serbest bırak**'ı seçin.

    ![Serbest bırak iletişim kutusu.](./media/subcontract20_release-dialog.png)

20. **Serbest bırak** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
21. **Üretim denetimi \> Periyodik görevler \> Ambara serbest bırak \> Ürün reçetesi ve formül satırlarının otomatik serbest bırakılması**'nı, **Ürün reçetesi ve formül satırlarının otomatik serbest bırakılması** iletişim kutusunu açmak için seçin.

    ![Ürün reçetesi ve formül satırlarını otomatik serbest bırakma iletişim kutusu.](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Ürün reçetesi ve formül satırlarının otomatik serbest bırakılması işini çalıştırmak için **Tamam**'ı seçin.

    Bu iş, ambardaki hammaddelerin çekilmesi işini serbest bırakır.

23. **Tüm üretim emirleri** sayfasını açmak için **Üretim kontrolü \> Üretim emirleri \> Tüm üretim emirlerini**'ni seçin.
24. Üzerinde çalışmakta olduğunu üretim emrini seçmek için hızlı filtreyi kullanın.
25. Eylem Bölmesi üzerinde **Ambar** sekmesinde, **İş** sayfasını açmak için **İş ayrıntıları**'u seçin.

    Sayfanın, hammadde seçmek için iki iş gösterdiğine dikkat edin. İlk iş, malzemeler M8100 ve M8101 için. Bu malzemeler, operasyon 10 tarafından tüketilir. İkinci iş, malzemeler M8202 ve M8250 için. Bu malzemeler, alt sözleşmeli bir operasyon olan operasyon 20 tarafından tüketilir.

    ![İş sayfasında hammadde seçimi için iki iş kümesi.](./media/subcontract22_work-page.png)

26. Operasyon 10 için ambar işini işlemek için Ambar Yönetimi mobil uygulamasını başlatın.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. **Tüm üretim emirleri** sayfasını açmak için **Üretim kontrolü \> Üretim emirleri \> Tüm üretim emirlerini**'ni seçin.
28. Üzerinde çalışmakta olduğunu üretim emrini seçmek için hızlı filtreyi kullanın.
29. Eylem bölmesinde, **Üretim emri** sekmesinde, **Başlat** iletişim kutusunu açmak için **Başlat**'ı seçin.
30. **Genel** sekmesinde, aşağıdaki değerleri belirtin:

    - **Operasyon Numarası**'da alan, seçin **10**.
    - **Operasyon Numarası'na** içerisinde alan, seçin **10**.

    ![Genel sekme 1'de ayarlanan değerler.](./media/subcontract23_start-dialog.png)

31. **Tamam**'ı seçin, kapatmak için **Başlat** iletişim kutusunu ve **Tüm üretim emirleri** sayfasına dönmek için.

    Üretim emrinin durumunun şimdi **Başlatıldı** olduğunu göz önünde bulundurun. Operasyon 10 için malzemeler, malzeme çekme listesi günlüğüne otomatik nakledilmesi tarafından tüketilmektedir. Operasyon 10 için zaman tüketimi, bir rota kartı günlüğünün otomatik nakli ile hesaplanır.

32. Operasyon 20 için ambar işini işlemek için Ambar Yönetimi mobil uygulamasını başlatın.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. Eylem bölmesinde, **Üretim emri** sekmesinde, **Başlat** iletişim kutusunu açmak için **Başlat**'ı seçin.
34. **Genel** sekmesinde, aşağıdaki değerleri belirtin:

    - **Operasyon Numarası**'da alan, seçin **20**.
    - **Operasyon Numarası'na** içerisinde alan, seçin **20**.
    - **Miktar** alanına **10** yazın.
    - **Malzeme çekme listesi** seçeneğini **Hayır** olarak ayarlayın.

    ![Genel sekme 2'de ayarlanan değerler.](./media/subcontract24_general-tab.png)

35. **Tamam**'ı seçin, kapatmak için **Başlat** iletişim kutusunu ve **Tüm üretim emirleri** sayfasına dönmek için.

    Bir malzeme çekme listesi, Kaplama operasyonunda kullanılan malzemeler ve servis maddesi için oluşturulmuştur. Servis maddesi, alt taşeron verilen operasyonun maliyetini temsil eder.

36. Eylem Bölmesinde, **Görüntüle** sekmesinde, **Malzeme çekme listesi**'ni açmak için **Malzeme çekme listesi**'ni seçin.
37. Deftere nakledilmemiş olan malzeme çekme listesini seçin, daha sonra günlük satırlarını görmek için günlük numarasını seçin.

    ![Malzeme çekme listesi sayfasındaki günlük satırları.](./media/subcontract25_picking-list.png)

38. Eylem bölmesinde **Yazdır** \> **Malzeme çekme listesi**'ni seçin ve **Malzeme çekme listesi raporu** iletişim kutusunu açın.
39. **Teslimat notu düzenini kullanın** seçeneğini **Evet** olarak ayarlayın.

    ![Malzeme çekme listesi raporu iletişim kutusu.](./media/subcontract26_picking-list-report-dialog.png)

40. **Tamam**'ı seçerek bir **Malzeme çekme listesi** raporu oluşturun.

    Bu durumda bir satıcı teslimat notu üretim malzeme çekme listesi günlüğünden yazdırılır. Teslimat notu, Kaplama operasonunu gerçekleştirecek satıcıya gönderilecek malzemeleri belirtir.

    ![Malzeme çekme listesi raporu.](./media/subcontract27_picking-list-report.png)

41. **Malzeme çekme listesi** sayfasına dönmek için **Malzeme çekme listesi**'ni kapatın.
42. Eylem Bölmesinde, **Günlüğü deftere naklet** iletişim kutusunu açmak için **Deftere naklet**'i seçin.

    ![Günlüğü deftere naklet iletişim kutusu.](./media/subcontract28_post-journal-dialog.png)

43. **Günlüğü deftere naklet** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
44. Satınalma siparişini açın.

    ![Satınalma siparişi sayfası.](./media/subcontract29_purchase-order-page.png)

45. Eylem Bölmesinde, **Satınal** sekmesinde, **Onayla**'yı seçin.
46. **Günlüğü deftere naklet** iletişim kutusunu açmak için **Deftere naklet**'i seçin.
47. **Tamam**'ı seçin, kapatmak için **Günlüğü deftere naklet** iletişim kutusunu ve **Satınalma siparişi** sayfasına dönmek için.
48. Birim fiyatı **33**'ten **40**'a değiştirin.

    ![Satınalma siparişi sayfasındaki birim fiyatı değiştirildi.](./media/subcontract30_unit-price.png)

49. Satınalma siparişini yeniden doğrulayın.
50. Ürün girişi.

    ![Ürün girişi naklediliyor iletişim kutusu.](./media/subcontract31_posting-product-receipt-dialog.png)

51. Satınalma faturası.
52. Eşleştirme durumunu güncelleştirin.

    ![Satıcı fatura sayfası.](./media/subcontract32_vendor-invoice-page.png)

53. Tamamlandı bildirimi.

    ![Tamamlandı olarak bildir iletişim kutusu.](./media/subcontract33_report-as-finished-dialog.png)

54. Bitiş.

    ![Bitiş iletişim kutusu.](./media/subcontract34_end-dialog.png)

55. Maliyet karşılaştırması.

    ![Maliyet karşılaştırması grafikleri.](./media/subcontract35_cost-comparison-charts.png)

Kurulumda veri eksik.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]