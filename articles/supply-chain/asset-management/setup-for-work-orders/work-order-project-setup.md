---
title: İş emri proje kurulumu
description: Bu makalede Varlık Yönetimi'nde iş emri proje türünü açıklanmaktadır.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjectSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31d8f42eb5753ea2656d502d2670a6cf7683c0f2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874144"
---
# <a name="work-order-project-setup"></a>İş emri proje kurulumu

[!include [banner](../../includes/banner.md)]

 

**Kıymet Yönetimi** modülünde, her bir iş emri işi için bir proje ilişkisi gereklidir. Bir iş emri işiyle ilişkilendirilmiş proje, dahili bakım projeleri, servis yönetim projeleri ve yatırım projeleri gibi, kıymet yönetimiyle ilgili çeşitli projelerdeki maliyetleri izlemenize olanak sağlar. 

## <a name="project-setup-for-a-work-order-job"></a>İş emri işi için proje ayarı

Bir iş emrinde iş emri işi oluşturduğunuzda **Proje yönetimi ve muhasebe** modülündeki proje kurulumu ve **Kıymet yönetimi** modülündeki iş siparişi proje kurulumu, projelerin maliyet için nasıl kullanılabileceğini belirler Bu iş emri işinde seçilen kıymet üzerinde kontrol sağlar. Bu bölüm, bir iş emri için kullanılan proje kurulumunun aşağıdaki kısımlarını açıklamaktadır: Ana proje (proje kodu), proje türü, proje faaliyetleri ve mali boyutlar:

- Bir iş emrinde iş emri işi oluşturduğunuzda, bunun için benzersiz bir proje kodu ve bir ilgili proje faaliyeti otomatik olarak oluşturulur. Ancak, bir iş emrindeki birkaç iş siparişi işi aynı kıymeti içeriyorsa, bunlar için aynı proje kodu kullanılır. Başka bir deyişle, bir iş emrindeki her kıymet için bir proje kodu oluşturulur.

    - İş emri işi için ana proje (proje kodu) üst proje kurulumunda bulunur. (Üst proje kurulumu hakkında daha fazla bilgi için sonraki bölüme bakın.) Örneğin, bir müşteriyi veya işlem yapılacak yerleşimi belirli bir ana projeyle ilişkilendirirseniz, o müşteri veya söz konusu işlem yapılacak yerleşim için her iş siparişi oluşturduğunuzda ana proje kullanılır. Örneğin, bir işlem yapılacak yerleşim gibi belirli bir proje kodunu ilişkilendirmezseniz, iş emri proje kurulumundaki bir sonraki ilgili üst proje kullanılır.
    - Her proje kodu için bir proje türü gereklidir. Proje türü, proje grubu kurulumu kurulumunda bulunur. (Proje grubu kurulumu hakkında daha fazla bilgi için sonraki bölüme bakın.) Proje grubu kurulumunda bir eşleşme bulunamazsa, ana projedeki proje grubu kurulumu kullanılır.
    - Tahminler ve günlüklerde proje faaliyetleri gerektiren kurulum, ana projeden iş emri projesine kopyalanır. Bir ana projeolarak kullanılan proje için **Saat**, **Gider** ve **Madde** seçenekleri **Evet** olarak ayarlanmışsa, proje faaliyeti tahminler ve günlüklerde zorunludur. (Bu seçeneklere erişmek için,**Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler**'i seçin ve ana proje olarak kullanılacak projeyi seçin. Seçenekler, **Kurulum** hızlı sekmesindeki **Günlüklerde faaliyet iste** bölümünde bulunur.)

- Finansal boyutlar kıymetten kopyalanır ve ana projeyle birleştirilir.

Sonraki bölüm, Ana projelerin ve proje gruplarının nasıl ayarlanacağını açıklar. Ana proje ve üst gruplar iş emirlerini denetlemek için kullanılır. Bunlar aynı zamanda iş emirleri hakkında raporlamalar için kullanılırlar.

## <a name="set-up-work-order-projects"></a>İş emri projeleri ayarı

İş emirleri oluşturmaya başlamadan önce iş emri projelerini ayarlamanız gerekir. **İş emri proje yönetimi** sayfası (**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Proje kurulumu**) iki sekme içerir: **Ana proje** ve **Proje grubu**.

**Üst proje** sekmesinde, iş emri işinde seçili kıymet üzerinde ayarlanmış bir proje yoksa, kullanılabilecek proje ilişkileri ayarlayabilirsiniz. Şirketiniz kıymet projeleri kullanıyorsa, bir üst proje kurulumu gerekmez. Yalnızca, kıymet projeleri yerine iş emri projelerini kullanmak istiyorsanız ilgilidir. Bu durumda, en az bir ana proje ayarlamanız gerekir.

**Proje grubu** sekmesinde, iş emri türleri, kıymet türleri ve kıymetlerle ilişkilendirilebilecek proje grupları ayarlayabilirsiniz.

Proje grupları, maliyet kontrolü için kullanılan belirli kategorileri (gruplar) oluşturmak için kullanılabilir. Örneğin, belirli kıymet türleri veya iş emri türleri için proje grupları oluşturarak, bakım maliyetlerinin ayrıntılı olarak bu türe göre izlenmesini sağlayabilirsiniz.

Proje grupları zorunlu değildir. Proje grupları ayarlamadıysanız, ana proje, proje grubunu belirlemek için kullanılır ve bir alt proje üst projenin proje grubundan oluşturulur.

Kurulum, **Oroje yönetimi ve muhasebe** modülüyle tam tümleştirmeye olanak tanır. Bu nedenle, ilgili projelerdeki iş emirleriyle ilgili maliyetleri izleyebilirsiniz. Aşağıdaki yordamda iş emri projeleri için kurulum açıklanmaktadır.

1. **Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Proje kurulumu**'nu seçin.
2. **Ana Proje** sekmesinde **Ekle**'yi seçin.
3. **Çalışma emri türü**, **İşlem yapılacak yerleşim**, **Kıymet türü** ve **Kıymet** alanlarında, gereksinim duyduğunuz şekilde değerleri seçin. Eklediğiniz her satır için yalnızca bir veya birden çok alan ayarlayabilirsiniz. Ayarladığınız alan sayısı, kıymet yönetiminde bir proje kodu seçildiğinde kullanılacak birleşimi belirler. 

    İşlem yapılacak yerleşim seçerseniz, ilgili alt yerleşimler otomatik olarak eklenir. Bir kıymet seçerseniz, aynı kıymet için daha fazla iş siparişi proje kurulum satırı oluşturabilirsiniz, ancak bu kıymet için farklı projeler seçebilirsiniz.

4. **Proje kodu** alanında, adım 3'te oluşturduğunuz kurulumla ilişkili olması gereken projeyi seçin.
5. Proje kurulumu yalnızca sınırlı bir dönem için geçerli ise, **Bitiş tarihi** alanında bir bitiş tarihi seçin. Aksi durumda **Hiçbiri** seçeneğini belirleyin.

    Varsayılan olarak, başlangıç tarihi iş emri projesini sayfaya eklediğiniz tarihtir. Varsayılan olarak gizli olan, **Geçerlilik başlangıcı** alanı tarafından denetlenir. **Geçerlilik tarihi** alanında **Görüntüle** \> **Tümü**'nü seçin. Daha sonra iş siparişi projesi için sınırlı bir dönem dönemi ayarlamak için **Geçerlilik tarihi** alanını **Bitiş tarihi** alanıyla birlikte kullanabilirsiniz.

    ![İş emri proje kurulumu sayfası.](media/17-setup-for-work-orders.png)

6. **Proje grubu** sekmesinde **Ekle**'yi seçin.
7. **İş emri türü** alanında bir iş emri türü seçin.
8. Proje grubu ilişkisinin daha belirli bir şekilde olmasını istiyorsanız, kıymet alanında **Kıymet türü** alanına veya bir **Kıymet**'e bir varlık türü seçin.
9. **Proje grubu** alanında, iş emri tipiyle ilişkili olması gereken proje grubunu seçin. Örneğin, **Önleyici bakım** olarak adlandırılan bir iş emri türü, önceki servis **Prev Maint** veya **Dahili** olarak adlandırılan bir proje grubuyla ilişkilendirilmiş olabilir. Alternatif olarak, **Yatırımlar** ve sabit kıymetlerle ilgili iş emirleri için kullanılan bir yatırım iş emri türü, **Yatırım** veya **Yatırım** adlı bir proje grubuyla ilişkilendirilebilir.
10. **Kaydet**'i seçin.

![İş emri proje kurulumu sayfası, İş emri ekleme.](media/18-setup-for-work-orders.png)

> [!NOTE]
> Bir iş emri satırı her oluşturulduğunda, kıymet yönetimi iş emri iş projesiyle ilişkili olması gereken bir proje grubu arar. Arama, bu makalede açıklanan kuruluma dayanır. Her proje grubunun ilgili bir proje türü vardır. **Zaman ve malzeme** veya **Sabit fiyatlı** proje türüne sahip proje grupları, yalnızca bir müşteri hesabıyla ilişkili kıymetler için geçerlidir.
>
> Ana projeler ve proje grupları için, sistem kullanılabilir iş emri projesini veya proje grubunu seçtiğinde, bu seçim önceki yordamı kullanarak oluşturduğunuz kayıtlara dayanır. Kıymet yönetimi, olası bir eşleşmeyi denetlemek için iş emri projesiyle ilişkili kayıtlara geçer. Her zaman ilk önce en belirgin birleşimi denetler. Başka bir deyişle, iş emri ana projesi için Kıymet Yönetimi **Kıymet** alanı için olası bir eşleşme arar. Eşleşme bulamazsa **Kıymet** alanı için eşleşmeleri denetler. Eşleşme bulamazsa **İşlem yapılacak yerleşim** alanı için eşleşmeleri denetler ve bu şekilde devam eder. **İş emri proje ayarı** sayfasının düzeninde gördüğünüz gibi bu davranış en belirgin birleşimi bulmak için Varlık Yönetimi'nin eşleşme için sağdan sola her kaydı denetleyeceği anlamına gelir. Eşleşme bulunmazsa yalnızca proje kodunun seçildiği varsayılan kaydı kullanılır. İlgili proje grubunu bulma işlemi benzerdir. Kıymet yönetimi önce **Kıymet** alanıyla ilgili olası eşleşmeyi denetleyip **Kıymet türü** alanını ve **İş emri türü** alanını denetler. Eşleşme bulunmazsa yalnızca proje grubunun seçildiği varsayılan kaydı kullanılır.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]