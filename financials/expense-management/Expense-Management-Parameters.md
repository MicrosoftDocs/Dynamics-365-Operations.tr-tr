---
title: "Gider yönetimi parametreleri"
description: "Aşağıdaki parametreler Gider yönetimi içindeki davranışı denetler."
author: knelson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5fd3a821719a3b4180cfcd4f26d0007accecee39
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="expense-management-parameters"></a>Gider yönetimi parametreleri
-----------------------------

Parametreler Gider yönetimi içindeki genel davranışı denetler.

### <a name="general"></a>Genel

| **Alan**                                                | **Açıklama**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standart mesafe oranı**                             | Mesafe giderleri için geri ödeme oranını girin. Oran, gider üzerinde girilen mesafe ile seyahat masrafı için yapılacak geri ödemenin tutarını hesaplamak için çarpılacaktır.                       |
|**Kişisel giderleri ödeyen:**                             | Kişisel olarak sınıflandırılmış kredi kartı hareketleri için kimin sorumlu olduğunu seçin.                                                                                                     |
|**Geri ayrıntılandırma sırasında tüm gider raporunu görüntüle**               | Belirli bir fiş için gider raporu deftere nakledildiğinde oluşturulan orijinal belgenin ayrıntılarını görüntülerken bir gider raporunun tüm giderlerini görüntülemek istiyorsanız bu seçeneği işaretleyin.              |
|**Seyahatin ön yetkilendirmesi zorunludur**                 | Bir personel bir gider raporu göndermeden önce seyahat talebinin gönderilmesini ve onaylanmasını şart koşmak istiyorsanız önce bu seçeneği işaretleyin.                                                                    |
|**Deftere nakletmeden önce dağıtımların düzenlenmesine izin ver**            | Bir gider raporunu dağıtımlarının deftere nakledilmeden önce düzenlenebilir olup olmadığını seçin.                                                                                                                 |
|**Gider yönetim ilkelerini değerlendir**                     | Bir gider ilkesinin ihlal edilip edilmediğini belirlemek için giderlerin ne zaman değerlendirileceğini seçin. Gider girişi girildiğinde veya kaydedildiğinde veya gider onaya gönderildiğinde giderler ihlaller için denetlenebilir. Girişler için gerekli ilke kuralları, gider satırı kaydedildiğinde denetlenir.                   |
|**Şirketlerarası gider satırlarına izin ver**                         | Bir gider raporunda diğer tüzel kişiler için giderlerin girilmesine izin verilip verilmeyeceğini seçin.                                                                                                          |
|**Kredi kartı giderleri için döviz kurunu düzenlemeye izin ver** | Kullanıcının içe aktarılan kredi kartı giderleri için döviz kurunu düzenlemesine izin vermek için bu seçeneği belirleyin.                                                                        |
|**Görüntülenecek çok düzeyli hiyerarşi alanları**                  | Gider raporu iş akışı atama türü hiyerarşi olarak ayarlandığında ve hiyerarşi seçimi Gider çok düzeyli onay hiyerarşisi kullanmak üzere ayarlandığında hangi onaylayıcı alanlarının görüntüleneceğini seçin. Çok düzeyli onay hiyerarşisi iş akışı için kullanıldığında, seçilen alanlar Gider raporunda görüntülenir ve düzenlenebilir olur. |
|**Personel kredi kartı numarasını girin (Temmuz 2017 güncelleştirmesi)**     | 15 veya 16 karakter sayısının girilebileceğini ve bir personelin **Kredi kartı** sayfasında **Kart Kodu** alanında kaydedilebileceğini seçin.                                                                          |

### <a name="financial"></a>Mali

| **Alan**                                                            | **Açıklama**     |
|----------------------------------------------------------------------|------------------------------------|
|**Günlük genel muhasebe günlüğü adı**                                         | Onaylanan gider raporlarının nakledileceği genel muhasebe günlüğünün adını seçin.            |
|**Giderlerden vergiden düşmeyi etkinleştir**                                  | Uygun giderler için gider vergiden düşmeyi etkinleştirmek için bu seçeneği seçin. ABD satış vergisi ve kullanım vergisi kuralları etkinleştirilmişse bu seçenek etkinleştirilemez.      |
|**Nakit avansları hemen deftere naklet**                                     | Öde ve aktar işlemi tamamladığında onaylanmış bir nakit avansını deftere nakletmek için bu seçeneği belirleyin. Bu seçenek seçildiğinde, Öde ve aktar işlemi deftere nakledilmemiş bir yevmiye defteri oluşturacaktır. |
|**Deftere nakil sırasında muhasebe tarihini düzelt**                             | Geçerli dönem beklemede veya kapalı ise giderleri deftere naklederken muhasebe tarihini güncelleştirmek için bu seçeneği seçin. Muhasebe tarihi bir sonraki açık döneme ayarlanır.   |
|**Hareketlerin ödeme yönteminde belirtilen mahsup hesaba göre gruplandırılmasına izin ver**      | Bir gider raporundaki, giderlerin ödeme yönteminde belirtilen mahsup hesap üzerine dayanan gider hareketlerini özetlemek için bu seçeneği seçin.   
|**Vergi dahil**                                                   | Varsayılan olarak satış vergisini gider tutarına dahil etmek için bu seçeneği seçin.             |
|**Seyahat taleplerinin kapatılması üzerinde yükümlülükleri serbest bırak**            | Onaylanan bir seyahat talebi kapatıldığında taahhüt edilen tutarları serbest bırakmak için bu seçeneği işaretleyin.                                                                                   |
|**Bütçe kaydı ve proje bütçesi için bütçe aşımında seyahat talebi göndermeye izin ver** | Personellerin bütçe kaydında izin verilen veya bir proje için izin verilen bütçelerini aşan seyahat taleplerini onaylama için göndermesine izin vermek için bu seçeneği işaretleyin.            |
|**Bütçe kaydı ve proje bütçesi için bütçe aşımında gider raporu göndermeye izin ver**    | Personellerin bütçe kaydında izin verilen veya bir proje için izin verilen bütçelerini aşan gider raporlarını onaylama için göndermesine izin vermek için bu seçeneği işaretleyin.                |
|**Yalnızca bütçe kaydı için bütçe aşımında gider raporu onayına izin ver**                | Onaylayıcıların, bütçe kaydında ayarlanmış olan izin verilen bütçelerini aşan gider raporlarını onaylamasına izin vermek için bu seçeneği işaretleyin.                                                                       |

### <a name="per-diem"></a>Harcırah

| **Alan**                             | **Açıklama**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Harcırah başına minimum saat sayısı**           | Bir personelin seyahatle ilişkili giderler için harcırah almaya hak kazanması için bir günde çalışması gereken saatlerin minimum sayısını girin.                                                                                      |
|**Yemek yüzdesi**                          | **Yiyecek indirimini şuna göre hesapla** alanı **Gün başına öğün türü** veya **Günlük öğünlerin sayısı** olarak ayarlandığında seyahate ilişkili giderin ilk ve son gününde kullanılacak yiyecek harcırahı için varsayılan yüzdeyi girin. İlk ve son günlerdeki çalışma günü, standart iş gününden daha kısa olabilir. Bu nedenle, bu günlerdeki harcırahın tutarı standart tutardan farklı olabilir. Yüzde 0 olarak ayarlanmışsa, ilk ve son gün kesintileri 0,00 olacaktır. |
|**Otel yüzdesi**                        | Oteller için seyahate ilişkin giderin ilk ve son gününde kullanılacak varsayılan harcırahın yüzdesini girin. İlk ve son günlerdeki çalışma günü, standart iş gününden daha kısa olabilir. Bu nedenle, bu günlerdeki harcırahın tutarı standart tutardan farklı olabilir. Yüzde 0 olarak ayarlanmışsa, ilk ve son gün kesintileri 0,00 olacaktır.                                              |
|**Diğer yüzde**                        | Muhtelif giderler için seyahate ilişkin giderin ilk ve son gününde kullanılacak varsayılan harcırahın yüzdesini girin. İlk ve son günlerdeki çalışma günü, standart iş gününden daha kısa olabilir. Bu nedenle, bu günlerdeki harcırahın tutarı standart tutardan farklı olabilir. Yüzde 0 olarak ayarlanmışsa, ilk ve son gün kesintileri 0,00 olacaktır.                                                                                                     |
|**Kahvaltı için indirim yüzdesi** | Kahvaltı için azaltılacak harcırah tutarını girin. Örneğin, bir çalışan indirimli kahvaltı alıyorsa, harcırahın tutarını yüzde 10 oranında azaltmak isteyebilirsiniz.                               |
|**Öğle yemeği için indirim yüzdesi**    | Öğle yemeği için azaltılacak harcırah tutarını girin. Örneğin, bir çalışan indirimli öğle yemeği alıyorsa, harcırahın tutarını yüzde 15 oranında azaltmak isteyebilirsiniz.                                       |
|**Akşam yemeği için indirim yüzdesi**   | Akşam yemeği için azaltılacak harcırah tutarını girin. Örneğin, bir çalışan indirimli akşam yemeği alıyorsa, harcırahın tutarını yüzde 25 oranında azaltmak isteyebilirsiniz.                                     |
|**Yemek indirimi hesaplama ölçütü**         | Kesintinin seyahat başına öğün türüne mi gün başına mı yoksa gün başına izin verilen öğün sayısına mı dayanacağını seçerek sistemin harcırah yiyecek kesintisini nasıl hesaplayacağını seçin.|
|**Harcırah yuvarlama**                  | Harcırah giderleri için yuvarlama türünü seçin. Normal yuvarlama seçerseniz, 0,50 tutarına sahip tüm harcırah giderleri 1,00'e yuvarlanır ve 0,50'ten düşük tutara sahip harcırah giderleri 0,00'a aşağı yuvarlanır.                                                                                              |
|**Harcırah hesaplamasında şunu esas al:**         | Harcırah tutarının takvim gününe mi 24 saatlik döneme mi dayanacağını seçin.       |

### <a name="fax-cover-pages"></a>Faks kapak sayfası

| **Alan**                      | **Açıklama**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Talimatlar**                   | Gider raporuyla ilişkili makbuzları göndermek için kullanılan faksın kapak sayfasını oluştururken personellerin izlemesi gereken yönergeleri girin. Kullanıcının diline dayalı olarak dile özel bir metni görüntülemek için **Çeviriler** düğmesini tıklatın. |
|**Kullanıcı kodu (Barkod bilgileri)** | Faks kapak sayfasında kullanılan bir personelin benzersiz tanımlayıcısını barkodda depolamak için bu seçeneği seçin.                 |
|**Barkod**                      | Faksın kapak sayfasında kullanılan barkodu seçin. Bar kodlar 39 ve 128 Gider yönetimi ile desteklenir.               |

### <a name="anti-corruption"></a>Yolsuzlukla mücadele

| **Alan**                             | **Açıklama**      |
|---------------------------------------|------------------------------------------------------------------------|
|**Yolsuzlukla mücadele onayını görüntüle**   | Yeni bir gider raporu oluştururken yolsuzlukla mücadele metnini görüntülemek için bu seçeneği işaretleyin. Belirli gider kategorileri daha sonra gider raporunda yolsuzlukla mücadele kanıtı gerektirmek üzere etkinleştirilebilir. Örneğin, bir hükümet yetkilisi gideri ile ilişkili hediye kategorisi, bir personelin giderin şirket ilkesine uygun olduğuna dair doğrulamasını gerektirebilir. |
|**Gönderene yönelik yolsuzlukla mücadele iletisi** | Yeni bir gider raporu oluşturulurken personele gösterilecek metni girin. Kullanıcının diline dayalı olarak dile özel bir metni görüntülemek için **Çeviriler** düğmesini tıklatın.         |
|**Onaylayana yönelik yolsuzlukla mücadele iletisi**  | Yeni bir gider raporu oluşturulurken onaylayıcıya gösterilecek metni girin. Kullanıcının diline dayalı olarak dile özel bir metni görüntülemek için **Çeviriler** düğmesini tıklatın.        |

