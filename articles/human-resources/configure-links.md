---
title: Human Resources uygulamasından başka bir ortama bağlantılar oluşturma
description: Bu makalede, Microsoft Dynamics 365 Human Resources'tan başka bir Dynamics 365 ortamına nasıl bağlantı oluşturulacağı açıklanmaktadır.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9640f460ed7b0b1a0cfdffb7c318bf833f8627fc
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065322"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Human Resources uygulamasından başka bir Finance ortamına bağlantılar oluşturma

Bir müşterinin, üzerinde çalıştığı iki Dynamics 365 ortamı olabilir. Örneğin, müşterinin Finance altyapısında bir Dynamics 365 Human Resources ortamı olabilir ve başka bir Dynamics 365 Finance ortamına bağlanması gerekir. 

Bu özellik, Human Resources sayfasından başka bir Finance ortamındaki belirli bir sayfaya giden bağlantılara izin verir. Bağlantılar yapılandırıldığında, bağlantının Human Resources'ta nerede kullanılabileceğini ve diğer ortamda açılacak hedef sayfayı belirleyebilirsiniz.

> [!Note] 
> Bu özelliği almak için **Özellik yönetimi**'ndeki **İnsan kaynakları kullanıcı deneyimi geliştirmeleri** özelliğini açmanız gerekir.

## <a name="configure-target-systems"></a>Hedef sistemleri yapılandır

Human Resources'ta sistem yöneticileri, **Human Resources** sayfalarında görülecek bağlantıları tanımlayabilir. Yapılandırmanın bazı bölümleri, bağlantının hedefi olarak gitmek istediğiniz Finance ortamlarıdır. 

Hedef sistemi yapılandırmak için:
1. **Bağlantıları yapılandır** sayfasında **Hedef sistemi yapılandır**'ı seçin.  
2. Hedef sisteme ad girin ve Finance ortamının URL'sini sağlayın. Hedef sistemlerinizi yapılandırdıktan sonra bağlantıları tanımlayabilirsiniz.

## <a name="configure-links"></a>Bağlantıları yapılandır

Oluşturduğunuz her bağlantının aşağıdaki bilgileri tanımlanması gerekir:
 - **Bağlantı**: Bağlantı adı. Yalnızca tanımlama için kullanılır.
 - **Bu bağlantıyı etkinleştir**: Bağlantıyı Human Resources kullanıcılarına göstermek isterseniz **Evet** olarak ayarlayın.
 - **Görünen ad**: İkincil ortama bağlantı olarak görünecek adı girin. 
 - **Bağlantıyı formda göster**: Bağlantıyı göstermek istediğiniz sayfayı seçin. Bağlantılar yalnızca **Personel self servisi** çalışma alanı ve **İş**, **Pozisyon**, **Çalışan** ve **Kolaylaştırılmış Çalışan** sayfalarında gösterilebilir.
 - **Grup**: Bağlantılarınızı grupları kullanarak düzenleyebilirsiniz. Mevcut bir grubu seçin veya **Grup** sütununu kullanarak yeni bir grup oluşturun.
 - **Hedef sistem**: **Hedef sistemi yapılandır** seçeneği kullanılarak oluşturulmuş olan hedef sistemi seçin. Bu, bağlantıyı kullanarak ziyaret edildiğinde kullanılacak ikincil ortamdır.
 - **Kullanıcının geçerli şirketini kullan**: Finance'e giderken kullanıcının geçerli şirket içeriğini kullanmak isterseniz **Evet**'i seçin. Kullanılması gereken şirketi seçmek için **Hayır**'ı seçin.
 - **Hedef** menü öğesi: Ziyaret ederken kullanılması gereken bağlantı için Finance ortamından menü öğesini girin. Doğrudan gidilecek menü öğeleri bulunur. 

   Gerekli menü öğesini bulmak için:
   1. Finance ortamına gidin ve gezintinin hedefi olan sayfayı açın. 
   2. Menü öğesini URL'den kopyalayın. Örneğin, bağlantının sizi finans ve operasyon uygulamalarında personele götürmesini isterseniz URL'de "&mi" sonrasında görünen değeri girin. 
   3. Bu örnekte personel listesi sayfasına gitmek için menü öğesi: HcmWorkerListPage_Employees.

 - **Veri kaynağına bağlantı**: Bağlantı referansı olan veri kaynağını seçin. En sık kullanılan kaynaklar, **Çalışan** ve **Konum** gibi, kullanılabilirdir.

### <a name="access-to-links"></a>Bağlantılara erişim

Sistem yöneticileri, **Bu bağlantıyı etkinleştir** seçeneği **Hayır** olarak ayarlanmış olsa bile yeni oluşturulan bağlantıları tanımlanan sayfalarda gösterir. Bu, bağlantıları diğer çalışanlara sunmadan önce test etmek için kullanılabilir. Tüm diğer roller yapılandırılmış bağlantıları yalnızca **Bu bağlantıyı etkinleştir** seçeneği **Evet** olarak ayarlandıktan sonra görür. Bağlantıların yer aldığı sayfalara erişimi olan personeller, bağlantılara erişime sahiptir.

Ayrıca kullanıcıların, o ortamdaki sayfalara erişmek için tanımlanmış ikincil ortam içinde güvenlik hakları da olmalıdır. Yoksa, bağlantıyı kullanırken güvenlik iletişim kutusu görüntülenir.


