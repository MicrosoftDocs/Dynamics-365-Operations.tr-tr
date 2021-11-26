---
title: Cihazlar için iş kartını konfigüre et
description: Bu konu, iş kartı aygıtını konfigüre etmek için çeşitli seçenekleri açıklamaktadır.
author: johanhoffmann
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 0382e34664f20389c43e8dec4437f0078fa1f60a
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777752"
---
# <a name="configure-job-card-for-devices"></a>Cihazlar için iş kartını konfigüre et

[!include [banner](../includes/banner.md)]

İş kartı aygıtı, atölye çalışanları tarafından, işlerin başlatılması, işlere ilişkin geribildirim bildirmek, dolaylı faaliyetleri kaydetmek ve devamsızlığı bildirmek gibi günlük çalışmalarını kaydetmek için kullanılır. Bu kayıtlar, ilerlemeyi izlemenin ve üretim emirleriyle ilgili maliyetin temelini oluşturur ve çalışanların ödemesine yönelik temel hesaplama içindir. Bu konu, iş kartı aygıtını konfigüre etmek için çeşitli seçenekleri açıklamaktadır.

## <a name="enable-new-features-in-feature-management"></a>Özellik yönetiminde yeni özellikleri etkinleştir

Bu konuda açıklanan ayarlardan birkaçı sisteminizde kullanılabilmesi için etkin olmalıdır. Aşağıdaki özelliklerin herhangi birini veya tümünü gerekli şekilde etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanın.

### <a name="generate-license-plate"></a>Plaka oluştur

Bu özelliği kullanılabilir hale getirmek için, [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin (sırasıyla):

1. İş Kartı Cihazına eklenme işi tamamlandı bildirimi için plaka (Supply Chain Management sürüm 10.0.21'den itibaren bu özellik varsayılan olarak etkindir.)
1. İş kartı cihazında tamamlandı olarak bildirme sırasında otomatik plaka numarası oluşturmayı etkinleştirin

### <a name="print-label"></a>Etiket yazdır

Bu özelliği kullanılabilir hale getirmek için, [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin (sırasıyla):

1. İş Kartı Cihazına eklenme işi tamamlandı bildirimi için plaka (Supply Chain Management sürüm 10.0.21'den itibaren bu özellik varsayılan olarak etkindir.)
1. İş Kartı Cihazından etiket yazdır

### <a name="allow-locking-of-touch-screen"></a>Dokunmatik ekranın kilitlenmesini sağla

Supply Chain Management sürüm 10.0.21 itibariyle, bu özellik varsayılan olarak açıktır. Bu özelliği kullanmak istiyorsanız [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) bulunan şu özelliği açın:

- Temizlenebilmeleri için iş kartı cihazını ve iş kartı terminalini kilitleme özelliği

## <a name="manage-your-device-configurations"></a>Cihaz yapılandırmalarınızı yönetin

Cihaz yapılandırmalarınızı yapmak için **Üretim denetimi > Ayarlar > Üretim yürütme > Cihazlar için iş kartını konfigüre et**'e gidin. Mevcut konfigürasyonların listesini gösteren cihazlar için **proje kartını konfigüre et** sayfası açılır. Buradan Aşağıdaki seçenekler arasından seçim yapabilirsiniz: 

- Görüntülemek ve düzenlemek için sol sütunda listelenmiş aygıt yapılandırmalarını seçin.
- Listeye yeni bir aygıt konfigürasyonu eklemek Için eylem bölmesinde **yeni** 'yi seçin. Yeni Yapılandırmayı tanımlamanıza yardımcı olacak bir **yapılandırma** alanına bir adı girin. Buraya girdiğiniz değer tüm aygıt yapılandırmaları arasında benzersiz olmalıdır ve daha sonra düzenleyemeyeceksiniz.

İş kartı aygıtlarını konfigüre etme ayarlarının her biri hakkında ayrıntılı bilgi için aşağıdaki bölümlere bakın.

## <a name="general-settings"></a>Genel ayarlar

**Genel** Hızlı sekmesi, seçili aygıt konfigürasyonu için kullanılabilen çeşitli seçeneklerin her birini konfigüre etmenize olanak tanır. Aşağıdaki ayarlar kullanılabilir:

- **Çıkış saatindeki rapor miktarı**: Çalışanların çıkış yaparken sürmekte olan işler hakkında geribildirim raporlamalarını istemek için bunu **Evet** olarak ayarlayın. **Hayır** olarak ayarlandığında, çalışanlar uyarılmayacaktır.
- **Çalışanı kilitle**: Bu seçenek **Hayır** olarak ayarlandığında , her çalışan bir kayıt yapıldıktan (yeni bir iş gibi) hemen sonra kapatılır ve sonra aygıt oturum açma sayfasına geri dönecektir. Bu seçenek **Evet** olarak ayarlandığında , her çalışan iş kartı aygıtında oturum açmış durumda kalır. Ancak, iş kartı aygıtı aynı sistem kullanıcı hesabı altında kaldığı sürece başka bir çalışanın oturum açmasına izin vermek için, çalışan el ile de oturum açabilir. Bu hesap türleri hakkında daha fazla bilgi için, [atanan kullanıcılar](#assigned-users)'a bakın.
- **Barkod tarayıcısı**: Bir Barkod tarayarak çalışanların yeni bir işin başlangıcını kaydetmesini sağlayan bir iş kartı aygıtında seçenek sağlamak için bunu **Evet** olarak ayarlayın.
- **Kaydın gerçek zamanını kullan**: Her yeni kaydın bir çalışan tarafından gönderildiği tam zamana eşit olması için kaydın gerçek zamanını **Evet** olarak ayarlayın. Bunun yerine oturum açma süresini kullanmak için **Hayır** olarak ayarlayın. Genellikle , **çalışanı kilitle** ve/veya **Tekli çalışan** seçeneklerini kilitlerseniz çalışanların daha uzun süreler boyunca oturum açmış durumda kaldığı durumlarda bunu **Evet** olarak ayarlamak isteyeceksiniz.
- **Tek çalışan**: Bu yapılandırmanın etkin olduğu her iş kartı aygıtını yalnızca bir alt kullanıyorsa, bu seçeneği **Evet** olarak ayarlayın. Bu seçenek belirlendiğinde, **çalışanı kilitle** seçeneği otomatik olarak **Evet** 'e ayarlanır. Ek olarak, bu seçenek işçi için bir rozet KIMLIĞI (veya benzeri) kullanarak oturum açabilme gereksinimi (ve yeteneğini) kaldırır. Bunun yerine çalışan, *çalışan bir saate bağlanmış* bir sistem kullanıcı hesabı kullanarak sağlamak için Supply Chain Management'ta oturum açar (*çalışanlar* tablosu) ve iş kartı aygıtında aynı anda çalışan olarak oturum açanlar.  Bu hesap türleri hakkında daha fazla bilgi için, [atanan kullanıcılar](#assigned-users)'a bakın.
- **Çalışanların kişisel filtreleri düzenlemesine izin ver** - çalışanların cihazda gösterilen işleri süzmelerine izin vermek için bu seçeneği **Evet** olarak ayarlayın. Çalışan, üç filtre ölçütlerinden herhangi birinin değerlerini değiştirebilir: **Üretim birimi**, **kaynak grubu** ve **kaynağı**. Yalnızca seçili filtre ölçütleriyle eşleşen kaynaklar üzerinde zamanlanan işler cihazda gösterilir. Bu ölçütlerin herhangi biri veya tümü için varsayılan değerler de atayabilirsiniz; bu seçenekle bile bunlar seçili olmaz.
- **Dokunmatik ekranda kilitlemeye izin ver** - çalışanların iş kartı aygıtı dokunmatik ekran seçeneklerini bu şekilde kilitlemesine izin vermek için bu seçeneği **Evet** olarak ayarlayın. Etkinleştirildiğinde, **Dezenfekte etmek için ekranı kilitle** düğmesi için bir kilit ekranı eklenir. Bir çalışan bu düğmeyi seçtiğinde, dokunmatik ekran, istenmeyen giriş yapılmasını önlemek için geçici olarak kilitler ve geri sayım süreölçeri görüntülenir. Çalışan şimdi aygıtı ve ekranı güvenle temizleyebilecek. Geri sayım tamamlandığında, dokunmatik ekran otomatik olarak yeniden kilidi açar.
- **Ekran kilitleme süresi** - **dokunmatik ekranı kilitlemeye izin ver** seçeneği etkinleştirildiğinde, bu seçeneği kullanın ve dokunmatik ekranın temizleme amacıyla kilitlenmesi gereken saniye sayısını belirtin. Süre 5 ile 120 saniye arasında olmalıdır.
- **Üretim birimi** - Her bir çalışana gösterilen iş listesi için varsayılan filtre ölçütü olarak uygulanacak bir üretim birimi seçin. Yalnızca seçili üretim birimi altında gruplandırılan kaynaklara zamanlanan işler başlangıçta görüntülenir. **Çalışanların kişisel filtreleri düzenlemesine izin ver** etkinse, çalışanlar bu değeri düzenleyebilir, aksi durumda bu cihaz konfigürasyonu etkin olduğunda bu filtre her zaman uygulanır.
- **Kaynak grubu** - Her bir çalışana gösterilen iş listesi için varsayılan filtre ölçütü olarak uygulanacak bir kaynak grubu seçin. Yalnızca seçili kaynak grubu altında gruplandırılan kaynaklara zamanlanan işler başlangıçta görüntülenir. **Çalışanların kişisel filtreleri düzenlemesine izin ver** etkinse, çalışanlar bu değeri düzenleyebilir, aksi durumda bu cihaz konfigürasyonu etkin olduğunda bu filtre her zaman uygulanır.
- **Kaynak** - Her bir çalışana gösterilen iş listesi için varsayılan filtre ölçütü olarak uygulanacak bir kaynak seçin. Yalnızca seçili kaynakta zamanlanan işler başlangıçta görüntülenir. **Çalışanların kişisel filtreleri düzenlemesine izin ver** etkinse, çalışanlar bu değeri düzenleyebilir, aksi durumda bu cihaz konfigürasyonu etkin olduğunda bu filtre her zaman uygulanır.
- **Lisans levhasını oluştur** - bir çalışanın bir iş kartı aygıtını her kullandığında tamamlandı bildirimi oluşturmak için bu seçeneği **Evet** olarak ayarlayın. Lisans levhası numarası, **Ambar yönetimi parametreleri** sayfasında ayarlanmış bir numara serisinden oluşturulur. **Hayır** olarak ayarlandığında , çalışanlar tamamlandı bildirimine göre, varolan bir lisans levhası belirtmelidir.
- **Etiket Yazdır** - bir çalışan bir çalışma tamamlandı bildirimi yapmak için iş kartı aygıtını kullandığında, bu seçeneği **Evet** olarak ayarlayın. Etiketin konfigürasyonu belge yönlendirmesinde, [Lisans plak etiketlerinin belge yönlendirme](../warehousing/document-routing-layout-for-license-plates.md) düzeninde açıklandığı gibi ayarlanır.

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Atanan kullanıcılar

Bir veya daha fazla sistem kullanıcıyı geçerli aygıt konfigürasyonuyla ilişkilendirmek için **atanan kullanıcılar** hızlı sekmesini kullanın. Her sistem kullanıcısına yalnızca bir iş aygıtı konfigürasyonu atanabilir.

Bir aygıtı kurarken BT çalışanı normalde bir sistem kullanıcı hesabı kullanarak Supply Chain Management'ta oturum açtığında. Bundan sonra, sistem kullanıcısı ile ilişkilendirilmiş iş aygıtı yapılandırması, o Kullanıcı oturum açtığı sürece uygulanır. Bu sistem kullanıcı hesapları genellikle yalnızca iş kartı aygıtı sayfasıyla erişim izni ve Supply Chain Management başka bir parçası olmadan sınırlıdır.

Sistem kullanıcısı oturum açtıktan ve iş aygıtı konfigürasyonu yüklendikten sonra, çalışanlar yeni işleri başlatmak ve başka tür kayıtlar yapabilmesi için, iş kartı aygıtında *kayıtlı saat çalışan* hesaplarını kullanarak oturum açabilir (örneğin, rozetinin barkodunu tarayarak). Sistem kullanıcısı gün boyunca Supply Chain Management için oturum açtığı için, aynı aygıt konfigürasyonu gün içinde oturum açıp bu makinede etkin kalır.

Ancak, daha önce belirtildiği gibi **tek çalışan** seçeneğiyle bir aygıt konfigürasyonu kullandığınızda , çalışanlar genellikle, kendi *saatine kayıtlı çalışan* hesaplarına bağlı bir sistem kullanıcısı kullanarak Supply Chain Management'ta oturum açtıklarında, bu nedenle aygıt yapılandırmasını yükler ve iş kartı aygıtında aynı anda oturum açmak için

## <a name="additional-resources"></a>Ek kaynaklar

[İş kartı cihazından tamamlandı olarak bildirme](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]