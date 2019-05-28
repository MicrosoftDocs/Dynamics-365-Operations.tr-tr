---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (31 Ekim 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6942f8e4dc86f18a081b347df0567b1358a87ab
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519334"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a>Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (31 Ekim 2018)

[!include [banner](includes/banner.md)]

**Derleme 8.1.2031**

Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.

## <a name="create-links-from-talent-to-finance-and-operations"></a>Talent ile Finance and Operations arasında bağlantı oluştur
Bu yeni gezinti işlevi Talent ile Finance and Operations arasında bağlantı kurmanızı sağlayarak Finance and Operations sayfalarına doğrudan ulaşım sunar. Bağlantılar yapılandırıldığında bağlantının adını ve grubunu, Talent'ta bağlantının yerini ve Finance and Operations'ta açılacak hedef sayfayı belirtebilirsiniz.

#### <a name="coming-soon"></a>Çok yakında
Bağlam alanı daha sonra Finance and Operations'ta karşılık gelen kayıtlara doğrudan gezintiye izin verecek şekilde eklenir. Örneğin, belirli bir personel veya Finance and Operations'ta konuma doğrudan gitmek için bağlam sağlamak için **Alana bağlantı** kullanabilirsiniz.

### <a name="configure-target-systems"></a>Hedef sistemleri yapılandır

Talent'ta sistem yöneticileri, Sistem Yönetimi çalışma alanında ortaya konacak bağlantılar tanımlayabilir. Konfigürasyonun bir kısmı, bağlantının "hedefi" olarak gitmek istediğiniz Finance and Operations ortamlarıdır. Hedef sisteme ad vererek ve Finance and Operations ortamı URL'sini sağlayarak bunu yaparsınız. İşte belirttiğiniz bir Finance and Operations URL'si örneği: https://devax00124aos.cloud.test.dynamics.com/. Hedef sistemlerinizi yapılandırdıktan sonra bağlantıları tanımlayabilirsiniz.

### <a name="configure-links"></a>Bağlantıları yapılandır

Oluşturulan her bağlantının aşağıdaki bilgileri tanımlanması gerekir.

- Bağlantı - Bağlantı adı, yalnızca kimlik saptama için kullanılır.

- Bu bağlantıyı etkinleştir - Bağlantıyı Talent kullanıcılara görüntülemek isterseniz **Evet** ayarlayın.

- Görünen ad - Finance and Operations bağlantısı olarak görünecek adı belirtin. Bu veri şu anda çevrilmemiş.

- Formda yüzey bağlantı - Bağlantıyı görüntülemek istediğiniz sayfayı seçin.

- Grup - Gruplar gerekli değildir, ancak bağlantılarınızı grupları kullanarak düzenlemek istiyorsanız, varolan bir grup seçin veya **Grup** alanını kullanarak yeni bir grup oluşturun.

- Hedef sistem - **Hedef sistemi yapılandır** seçeneği kullanılarak oluşturulmuş olan hedef sistemi seçin. Bağlantıyı kullanarak ziyaret edildiğinde kullanılacak Finance and Operations ortamı olacak.

- Kullanıcının geçerli şirketini kullanın - Finance and Operations'a giderken kullanıcının geçerli şirket içeriğini kullanmak isterseniz **Evet**'i seçin. **Hayır** seçilirse kullanılması gereken şirket seçebilirsiniz.

- Hedef menü öğesi - Ziyaret ederken kullanılması gereken bağlantı için Finance and Operations'tan menü öğesini girin. Doğrudan gidilecek menü öğeleri bulunur. Gereken menü öğesini bulmak için Finance and Operations'ı açın ve gezintinin hedefi olan sayfayı açın. Menü öğesini URL'den kopyalayın. Örneğin, bağlantının sizi Finance and Operations'ta personele götürmesini isterseniz URL'de "&mi" sonrasında görünen değeri girin. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Bu örnekte personel listesi sayfasına gitmek için menü öğesi: HcmWorkerListPage_Employees.

- Veri kaynağına bağlantı - Bağlantı referansı olan veri kaynağını seçin. En sık kullanılan kaynaklar, **Çalışan** ve **Konum** gibi, kullanılabilirdir.

- Alan bağlantısı - (Çok yakında) Bu alan seçimi, Talent'ta tek bir kayıttan Finance and Operations'a tek bir kayıt için doğrudan gezintiye izin verir.

### <a name="access-to-links"></a>Bağlantılara erişim

Sistem yöneticileri, **Bu bağlantıyı etkinleştir** seçeneği **Hayır** olarak ayarlanmış olsa bile yeni oluşturulan bağlantıları tanımlanan sayfalarda gösterir. Bu, bağlantıları diğer çalışanlara sunmadan önce test etmek için kullanılabilir. Tüm diğer roller yalnızca **Bu bağlantıyı etkinleştir** seçeneği **Evet** olarak ayarlandıktan sonra yapılandırılmış bağlantıları görür. Bağlantıların yer aldığı sayfalara erişimi olan personeller, bağlantılara erişime sahiptir.

Kullanıcılar, Finance and Operations'taki sayfalara erişmek için Finance and Operations'ta tanımlanmış güvenlik haklarına sahip olabilir. Yoksa, bağlantıyı kullanırken güvenlik iletişim kutusu görüntülenir.


## <a name="other-changesfixes"></a>Diğer değişimler/düzeltmeler

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>İleride bir başlangıç tarihine sahip olan pozisyonlar yeni bir personele atanamaz

Gelecek tarihli pozisyonlara personel atamasına izin vermek için değişiklikler yapıldı. Başlangıç tarihi gelecekte olan pozisyonlar seçilebilir ve personel ataması, kaydetmeden ya da iş akışının (iş akışı etkinse) tamamlanmasından sonra yapılır.

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Yeni çalışan varolan konuma atanamaz

Yeni personel ataması artık varolan konumlara atanabilsin diye değişiklikler yapıldı.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Kıdem tarihi/Ofis konumu, çalışma başlangıç tarihi geçmişte olduğunda ve kayıt kaydedildiğinde kaybolur

Eski personeller için değişiklikleri kaydederken **Kıdem tarihi** ve **Ofis konumu** görünürlüğünü doğrulamak için değişiklikler yapıldı.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Çalışan sayfasına gelecek tarihli istihdamlar için veri girilemiyor

Gelecek tarihli istihdamlar için çalışma verileri ana çalışan sayfasında devre dışı bırakıldı. İstihdam verileri, **Tarih Yöneticisi** sayfalarıyla girilebilir. Gelecekteki sürümlerde, iş akışı süreci sırasında doğrudan istihdam verilerini girebilmek için ilave değişiklikler yapılacak.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>HcmPersonalContactPersonEntity'ye ValidFrom ve ValidTo ekleyin

Veri Yönetimi Çerçevesi (DMF) varlığı HcmPersonalContactPersonEntity, belirli kazanç entegrasyon senaryolarını etkinleştirmek için "geçerli başlangıç" ve "geçerli bitiş" tarihlerini içerecek şekilde güncelleştirildi. 

## <a name="known-issue"></a>Bilinen sorun
- **Sorun**: Bir çalışan için yeni bir eki eklerken **Yeni** ve **Düzenle** düğmeleri gridir. 
- **Çözüm:** Ek sayfasını açmadan önce **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun. **Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır. (Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)
