---
title: "Operasyon planlama çizelgeleme seçenekleri"
description: "Bu konu, Operasyon planlama çizelgelemesi seçeneklerini açıklar. Operasyon planlama çizelgelemesini zaman içinde üretim süresine dair genel bir tahmin yapmak için kullanabilirsiniz."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 56eeb2b56261dc3e576192c0ede405996d82b2b7
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="operations-scheduling-options"></a>Operasyon planlama çizelgeleme seçenekleri

[!INCLUDE [banner](../includes/banner.md)]

Bu konu, Operasyon planlama çizelgelemesi seçeneklerini açıklar. Operasyon planlama çizelgelemesini zaman içinde üretim süresine dair genel bir tahmin yapmak için kullanabilirsiniz.

Operasyon planlama çizelgeleme, bir üretim emri için aşağıdaki bilgileri hesaplar:

-   Üretim emri ve her operasyon için başlangıç ve bitiş tarihleri ayarlanır.
-   Kaynaklar operasyonlara atanır.

Üretim iş planlama çizelgelerinin nasıl hesaplanacağını çeşitli ayarlar belirler. Bu ayarlar, **Operasyon planlama çizelgeleme** sayfasında tanımlanır. Aşağıdaki bilgiler planlama seçeneklerini açıklar.

## <a name="operations-scheduling"></a>Operasyon planlama çizelgeleme
### <a name="scheduling-direction"></a>İş planlama çizelgeleme yönü

Planlama yönü, planlama süreci bakımından temel niteliğindedir. Üretim, zamanlama ve planlama gereksinimlerine bağlı olarak herhangi bir tarihten geriye veya ileriye doğru planlanabilir.

-   **İleriye doğru planlama**: Üretimi olabildiğince erken başlatmak için planlayabilirsiniz. Üretime bugün, yarın veya gelecekte belirli bir tarihte başlanabilir. Üretim mümkün olan en erken tarihte başlayacak şekilde planlanır ve mümkün olan en erken son tarihe, ileriye doğru planlanır.
-   **Geriye doğru planlama**: Üretimi, olabildiğince geç başlatmak için planlayabilirsiniz. Planlamada üretimin tamamlanması gereken tarih temel alınır ve hedeflenen bitiş tarihi aşılmadan üretimin bağlayabileceği en geç tarihe kadar geriye doğru sayılır.

Aşağıdaki seçenekler bulunur:

-   **Bugünden sonrası**: Geçerli tarihten sonrası için planlama. (Geçerli tarih, sistem tarihidir.)
-   **Planlanan başlangıçtan ileri doğru**: Daha erken bir başlangıç tarihinden ileriye doğru planlama. Önceden planlama yapılmadıysa, zamanlama yönü geçerli tarihten sonraya doğrudur.
-   **İş planlama çizelgeleme tarihinden ileriye doğru**: **Planlama tarihi** alanında belirtilen tarihten ileriye doğru planlama. İş planlama çizelgeleme tarihi belirtmediyseniz zamanlama yönü geçerli tarihten ileriye doğrudur.
-   **Teslimat tarihinden geriye doğru**: Üretim emri için belirtilen teslimat tarihinden geriye doğru planlama. Bu seçeneği belirlediyseniz ancak herhangi bir teslimat tarihi belirtilmemişse teslimat tarihi geçerli tarihtir.
-   **Planlanan bitişten geriye doğru**: Daha önce hesaplanan bitiş tarihinden geriye doğru planlama. Önceden planlama yapılmadıysa bitiş tarihi geçerli tarihtir.
-   **İş planlama çizelgeleme tarihinden geriye doğru**: **Planlama tarihi** alanında belirtilen tarihten öncesi için planlama. İş planlama çizelgeleme tarihi belirtmediyseniz, geçerli tarih kullanılır. İş planlama çizelgeleme tarihinden geriye doğru, bir gereksinimin son kez hesaplandığı üretim emri için yapılır. Üretim emri için tarih belirtilmezse geçerli sistem tarihi kullanılır.
-   **Vadeli mesaj tarihinden geriye**: En son bir gereksinim hesaplandığında üretim siparişi için hesaplanan vadeli mesaj tarihinden geriye doğru planlama. Üretim emri için vadeli mesaj tarihi belirtilmezse geçerli sistem tarihi kullanılır.
-   **Son iş planlama çizelgeleme olarak**: Operasyon planlama çizelgelemesi ve iş planlama çizelgelemesi için seçili planlama yönü ve tarihi kaydedilir. Bu nedenle, izleyen planlama için bu seçeneği belirleyebilirsiniz. Üretim emrinde önceden hiçbir planlama yapılmamışsa planlama geçerli sistem tarihinden geriye doğru yapılır.
-   **Yarından itibaren gönder**: Geçerli güne bir gün ekleyerek ileriye doğru planlama.
-   **Önceki işten ileriye doğru**: Bu seçenek yalnızca iş planlama çizelgelemesi için geçerlidir. Operasyon planlama çizelgelemesi için bu planlama yönünü seçerseniz üretim emri geçerli tarihten ileriye doğru planlanır. İş planlama çizelgelemesinde, planlama bir iş için yapılır ve üretime yönelik tüm diğer işler bu iş temel alınarak planlanır.
-   **Önceki işten geriye doğru**: Bu seçenek yalnızca iş planlama çizelgelemesi için geçerlidir. Operasyon planlama çizelgelemesi için bu planlama yönünü seçerseniz planlı siparişler mevcut tarihten geriye doğru planlanır. İş planlama çizelgelemesinde, planlama bir iş için yapılır ve üretime yönelik tüm diğer işler bu iş temel alınarak planlanır.

### <a name="scheduling-date"></a>İş planlama çizelgeleme tarihi

Bu tarih, **İş planlama çizelgeleme tarihinden ileriye doğru** ve **İş planlama çizelgeleme tarihinden geriye doğru** planlama yönleri için kullanılır. Planlama bu tarihten geriye veya ileriye doğru yapılır. Daha fazla bilgi için bir önceki "Planlama yönü" bölümüne bakın.

### <a name="recalculate-bom-levels"></a>Ürün reçetesi düzeylerini yeniden hesapla

**Ürün reçetesi düzeylerini yeniden hesapla**'yı seçtiğinizde, doğru planlama sırasının sağlanmasını garanti altına almak için seçilen ürün reçeteleri (BOM) düzeyleri yeniden hesaplanır.

## <a name="limitations"></a>Sınırlamalar
### <a name="finite-capacity"></a>Sınırlı kapasite

Planlama, işi tamamlamak için gereken kaynakların kullanılabilirliğine bağlıdır. Yeterli kapasite yoksa, üretim emirleri gecikebilir ve hatta durabilir. Operasyon planlama çizelgelemesine sonlu kapasite uygulanırsa kaynaklarda yapılan mevcut kapasite rezervasyonları değerlendirilir ve bu kapasite kullanılamaz olarak görünür. Üretim emri, gereken kaynaklardaki kapasite kullanılabilirliğini temel alarak planlanır. Operasyon planlama çizelgelemesi, üretim rotasındaki operasyon sırasını belirlemek için belirtilen operasyon sırasını kullanır. Operasyon planlama çizelgelemesi, kaynak gruplarındaki kapasiteyi üretim rotasında tanımlanan işlem sürelerini temel alarak ayırır. Kaynak gruplarının kapasitesi, kaynak gruplarındaki tüm kaynakların kullanılabilir kapasitesinin toplamıdır.

### <a name="finite-material"></a>Sınırlı malzeme

İş planlama çizelgeleme, ayrıca üretim için gereken malzemelerin kullanılabilirliğini de temel alır. Yetersiz bileşen kullanılabilirliği de üretim gecikmelerine neden olabilir. İş planlama çizelgeleme, malzemelerin kullanımını da temel alabilir. Kritik olmayan malzemeler yerine yalnızca üretim için kullanılabilir olması gereken malzemeleri belirtin. Bu tür bir planlama çizelgelemesi, sınırlı malzeme ile planlama çizelgelemesi olarak bilinir. Sınırlı malzemeleri belirtiyorsanız üretim, malzemelerin kullanılabilir olup olmamasına göre planlanır. **Not:** Hem kapasiteye hem de malzemelere göre en iyi duruma getirirken üretim her iki kısıtlamayı da karşılayacak şekilde hesaplanır. Kapasitenin ve malzemelerin kullanılabilirliği değerlendirilir ve üretim emrinin operasyonları, kapasite ve malzemeler aynı zamanda ve gerekli miktarlarda kullanılabilir olana kadar başlaması için planlanamaz. Planlama çizelgelemesi sırasında malzemelerin sınırlı olarak değerlendirilmesi gerekiyorsa bu onay kutusunu seçin. Malzemeler sınırlıysa, malzemenin söz konusu zamana yönelik tedarik planı dikkate alınır. Diğer bir deyişle, planlama maddeler için hesaplanan vadeli mesaj tarihlerini dikkate alır. Planlamada hammaddeler rezerve edilir ve geçerli üretimin açılımı yapılır. Planlama çizelgelemesi birkaç kez yapılırsa yalnızca ilk planlama çizelgelemesi bir açılım çalıştırır ve rezervasyonlar yapar. Üretim ürün reçetesinde veya rotasında değişiklik yaparsanız sonraki planlama çizelgesi bir açılım çalıştırır. Açılım için, malzemelerin aynı gün gerektiği varsayılır. Üretim, master planlama çizelgesi açılımı sırasında planlanmadığından geçerli tarih, maddelerin kullanılabilir olacağı tahmin edilen en iyi zamandır. Ardından, açılım maddelerin bulunup bulunmadığını denetler. Maddeler kullanılabilirse üretim gereksinimi karşılanabilir. Maddeler geçerli tarihe kadar kullanılabilir olmazsa planlı bir sipariş oluşturulur ve planlı sipariş için mahsup seçimi yapılır. Planlı sipariş için otomatik kesinleştirme ayarlanmışsa planlı sipariş satınalma veya üretim için otomatik olarak kesinleştirilir. Üretim durumu otomatik olarak **Karşılama grupları** iletişim kutusundaki **İstenen üretim durumu** alanında belirtilen duruma değişir. Onay kutusu temizlenmişse malzemeler her zaman kullanılabilir olarak değerlendirilir. Bu nedenle, planlama çizelgelemesi gereksinim zamanında malzemelerin bulunup bulunmadığını dikkate almaz.

### <a name="finite-property"></a>Sınırlı kaynak

İş planlama çizelgelemesinin özellik gereksinimlerini içermesi gerekiyorsa bu onay kutusunu seçin.

### <a name="keep-production-unit"></a>Üretim birimini tut

İş planlama çizelgeleme altyapısının yalnızca üretim biriminde önceden belirtilmiş kaynakları planlaması gerekip gerekmediğini seçin.

### <a name="keep-warehouse-from-resource"></a>Ambarı kaynaktan koru

İş planlama çizelgeleme altyapısının yalnızca kaynakta belirtilen giriş ambarıyla ilişkili kaynakları planlaması gerekip gerekmediğini seçin.

## <a name="references"></a>Referanslar
### <a name="schedule-references"></a>Referansları planla

Referanslar, üretim emirlerini temel aldığında alt üretimler olarak da bilinir. Alt üretimler, bir üretim emri planlama çizelgesinin parçası olarak planlanabilir. Alt üretimlerin planlanma çizelgesinin ana üretimin planlanma çizelgesini temel alması gerekiyorsa bu onay kutusunu seçin. Ana üretimle ilişkili olarak üstteki üretimler ileriye doğru, alttaki üretimler ise geriye doğru planlanır. Üretim emri referanslarını **Üretim emirleri** sayfasında **Referans düzeyi** alanında görüntüleyebilirsiniz.

### <a name="synchronize-references"></a>Referansları eşitle

Ayrıca referansları üretim emriyle eşitleyebilirsiniz. Bu seçenek tercih edilirse üretim emri planlamasında değişiklik yapıldığında alt üretimlerdeki tarihler taşınır ve hizalanır. Üretim siparişinde bir veya daha fazla alt üretim varsa alt üretimleri ana üretimle birlikte planlamak isteyebilirsiniz. Bu durumda, ilgili alt üretim tamamlanana kadar ana üretim başlatılamaz. Bu nedenle alt üretimlerin planlanmasının seçilen üretimin başlangıç ve bitiş zamanlarına göre yapılması gerekiyorsa bu onay kutusunu seçin. Bu onay kutusunu yalnızca **Referansları planla** onay kutusu da seçilirse seçebilirsiniz.

## <a name="cancellation"></a>İptal
### <a name="cancel-queue-time"></a>Kuyruk süresini iptal et

Kuyruk süresini planlama çizelgelemesinden hariç tutmak için bu onay kutusunu seçin.

### <a name="cancel-setup"></a>Kurulumu iptal et

Hazırlık süresini planlama çizelgelemesinden hariç tutmak için bu onay kutusunu seçin.

### <a name="cancel-process"></a>İşlemi iptal et

Çalıştırma süresini planlama çizelgelemesinden hariç tutmak için bu onay kutusunu seçin.

### <a name="cancel-overlap"></a>Çakışmayı iptal et

Çakışma süresini planlama çizelgelemesinden hariç tutmak için bu onay kutusunu seçin.

### <a name="cancel-transport"></a>Taşımayı iptal et

Taşıma süresini planlama çizelgelemesinden hariç tutmak için bu onay kutusunu seçin.

## <a name="set-default"></a>Varsayılanı ayarla
Geçerli değerleri, varsayılan değerler olarak kaydedebilirsiniz. İki seçenek bulunur:

-   Varsayılanım olarak ayarla
-   Herkes için varsayılan olarak ayarla


<a name="see-also"></a>Ayrıca bkz.
--------

[Operasyon planlama çizelgeleme](operations-scheduling.md)




