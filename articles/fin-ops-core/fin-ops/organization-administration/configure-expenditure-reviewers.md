---
title: Harcama gözden geçirenlerini yapılandırma
description: Bu konu, iş akışı görevinin, onayın veya el ile kararın atandığı kullanıcıyı dinamik olarak seçmek için harcama gözden geçiricilerin nasıl kullanılacağını açıklar.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: b0de3d9280c43fc7e2bb2568d4a57250da4dfebf
ms.sourcegitcommit: 9f3b6c00f82694b5f8eb1bda75411801c0fccf4a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2021
ms.locfileid: "6315691"
---
# <a name="configure-expenditure-reviewers"></a>Harcama gözden geçiricilerini yapılandırma
[!include[banner](../includes/banner.md)]

Proje rolüne atanan kullanıcıya veya harcamanın borçlandırıldığı mali boyuta göre harcamaları gözden geçirilmesi için yönlendirmek üzere dinamik harcama gözden geçiriciler ayarlayabilirsiniz. İş akışı süreci, harcamanın kime yönlendirilmesi gerektiğini belirlemek için belirli bir proje rolünü veya mali boyut sahibini kullanır.

Bir veya daha fazla harcama gözden geçiren yapılandırması tanımlayabilir ve ardından bir iş akışı oluşturduğunuzda bir yapılandırmayı seçebilirsiniz. Kuruluşunuzdaki her bir tüzel kişilik için harcama gözden geçiren değerlerini yapılandırabilirsiniz. Harcama gözden geçiren yapılandırmalarını tanımladıktan sonra yapılandırmayı atarsınız. Harcamaları gözden geçirenler iş akışı görevlerine, onaylara ve el ile kararlara atanabilir.

> [!NOTE]
> Harcamaları gözden geçirenler zorunlu olmasa da, iş akışınızın yapılandırmasını basitleştirmeye yardımcı olabilirler. Örneğin, her maliyet merkezi boyutunu denetlemek için bir koşullu karar oluşturmanız ve sonra onayı veya görevi belirli bir kullanıcıya veya Kullanıcı gruplarına atamak için başka bir öğe oluşturmanız gerekmez. Bunun yerine, maliyet merkezi boyutunun sahibini yapılandırabilir ve doğru kullanıcıyı dinamik olarak seçmek için bir harcama gözden geçireni kullanabilirsiniz. Bu şekilde, maliyet merkezlerinin sahipliği veya ataması değiştiğinde, mali boyu için yalnızca **Sahip** alanını güncelleştirmeniz gerekir.

## <a name="types-of-expenditure-reviewers"></a>Harcama gözden geçirenlerin türleri

Tüm iş akışları harcama gözden geçiriciler kavramını desteklemez. Varsayılan olarak satınalma talepleri, satınalma siparişleri, satıcı faturaları ve gider raporları için harcama gözden geçirenleri yapılandırabilirsiniz. Bu iş akışı türlerinin her biri, harcama gözden geçirenlerini özellik ve modüle özel ayrı bir sayfada yapılandırmanızı gerektirir. Desteklenen her belge için, harcama gözden geçirenler başlık düzeyi iş akışlarıyla veya satır düzeyi iş akışlarıyla kullanılabilir.

Aşağıdaki tabloda, her desteklenen belge için bir harcama gözden geçireni yapılandırmak üzere gittiğiniz yer gösterilmektedir.

| Belge | Gezinti yolu |
|----------|-----------------|
| Gider raporları | Gider yönetimi \> Kurulum \> İlkeler \> Harcama gözden geçirenler |
| Satın alma siparişleri | Tedarik ve kaynak atama \> Kurulum \> İlkeler \> Satınalma siparişi harcama gözden geçirenleri |
| Satın alma talepleri | Tedarik ve kaynak atama \> Kurulum \> İlkeler \> Satınalma talebi harcama gözden geçirenleri |
| Satıcı faturaları | Borç hesapları \> İlke ayarı \> Satıcı fatura harcama gözden geçirenleri |

## <a name="expenditure-reviewer-assignments"></a>Harcama gözden geçirici atamaları

Her bir harcama gözden geçirici için iki tür atama vardır: *proje dağıtımları* ve *kuruluş dağıtımları*. Proje dağıtımı için proje yetkilileri ve mali boyutlar arasından seçim yapabilirsiniz. Kuruluş dağıtımı için mali boyutları seçebilirsiniz.

Proje yetkilileri proje yöneticisini, proje denetleyicisini ve proje satış yöneticisini içerir. İlgili alanlarda bir çalışan seçerek bu yetkilileri doğrudan projenizde tanımlayabilirsiniz.

Mali Boyutlar, her tüzel kişilikteki hesap yapılarına göre kontrol edilir. Her tüzel kişilik için, harcama gözden geçirici ile hangi finansal boyutların kullanılacağını seçebilirsiniz. Boyutlar ya projeden (bu durumda, **Proje dağıtımları** sekmesinde boyutları seçersiniz) ya da belgeden (bu durumda, **Kuruluş dağıtımları** sekmesindeki boyutları seçersiniz) gelir. **Finansal boyut değerleri** sayfasındaki **Sahip** alanında her mali boyut için çalışanı seçebilirsiniz.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>Örnek 1: Kuruluş dağıtımlarına göre harcama gözden geçiriciler

Contoso Appliances için çalışıyorsunuz ve kuruluşunuzda altı departman ve 10 maliyet merkezi var. Yeni bir satınalma talebi gönderildiğinde, onay ilk olarak departman yöneticisinden ve sonra da maliyet merkezi yöneticisinden gelmelidir.

Bu örnekte, iki *Satınalma talebi harcamaları gözden geçireni* yapılandırırsınız:

- İlk gözden geçiren kişi için, departmanı belirtin ve ardından **Kuruluş dağıtımları** sekmesinde **Departman** mali boyutunu seçin. 
- İkinci gözden geçiren kişi için, maliyet merkezini belirtin ve ardından **Kuruluş dağıtımları** sekmesinde **Maliyet Merkezi** mali boyutunu seçin.

İş akışını yapılandırdığınızda, iki onay adımı oluşturursunuz. Birincisi departman içindir, ikincisi ise maliyet merkezi içindir. Her bir onay öğesi için, **Rol tabanlı** sekmesindeki **Atama türü** alanında **Katılımcı**'yı seçin, **Katılımcı türü** alanında **Harcama katılımcıları**'nı ve ardından **Katılımcı** alanında uygun katılımcıyı seçin.

Satınalma talebi oluşturulduğunda, departman ve maliyet merkezi finansal boyutları satınalma talebinin satırlarına atanır. İş akışı gönderildiğinde, sistem önce satınalma talebindeki departmanı değerlendirir ve departman için seçtiğiniz çalışanla ilgili kullanıcıya onay öğesini atar. İlk onay adımı tamamlandıktan sonra, sistem ikinci onay adımını değerlendirir ve departman için seçtiğiniz çalışanla ilgili kullanıcıya ikinci onay öğesini atar.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>Örnek 2: Proje dağıtımlarına göre harcama gözden geçiriciler

Contoso Appliances servis bölümünde çalışıyorsunuz. Kuruluş, proje yöneticisinin her satınalma siparişi için gideri onaylamasını gerekli kılıyor. Ayrıca, projenin maliyet merkezi yöneticisinin de bunu onaylaması gerekiyor. Onaylar aynı zamanda yapılabilir. Her durumda, iş akışının devam edebilmesi için, her iki kullanıcının da satınalma siparişini onaylaması gerekir.

Bu örnekte, *PM ve Maliyet Merkezi* adında bir **satınalma siparişi harcamaları gözden geçireni** oluşturursunuz. **Proje Yöneticisi** onay kutusunu seçip **Satınalma siparişi harcamaları gözden geçireni** sayfasının **Proje dağıtımları** sekmesinde **Maliyet merkezi boyutu** seçeneğini **Evet** olarak ayarlarsınız. Yapılandırmanın bir parçası olarak, **Proje Yöneticisi** alanının tüm projeler için ayarlandığından ve **Mali boyut değerleri** sayfasındaki tüm maliyet merkezleri için bir sahip belirtildiğinden emin olmanız gerekir.

İş akışını yapılandırırken, bir onay öğesi gerekir. **Atama türü** alanında **Katılımcı**'yı seçersiniz. Ardından, **Rol tabanlı** sekmesinde **Katılımcı türü** alanında **Harcama katılımcıları**'nı seçin ve **Katılımcı** alanında proje yöneticisini ve maliyet merkezini seçin. Hem proje yöneticisi, hem de maliyet merkezi sahibi iş akışını onaylayana kadar iş akışının devam edememesini sağlamak için, **Tamamlanma ilkesi** alanını **Tüm onaylayanlar** olarak ayarlarsınız.

Satınalma siparişi oluşturulduğunda, **Proje** alanı belirtilmelidir. Tüm satınalma siparişleriniz için projeyi gerekli yapmadıysanız, onay adımı çalıştırılmadan önce bir proje için iş akışınızın kontrol etmesi gereken bir koşullu karar eklemeniz gerekir. Daha sonra sistem, satınalma siparişi için belirtilen projeyi değerlendirir ve **Proje Yöneticisi** alanında çalışan ile ilgili kullanıcıya onay öğesini atar. Ek olarak, sistem bir görev oluşturur ve bunu projedeki maliyet merkezinin **Sahip** alanında seçtiğiniz çalışanla ilgili kullanıcıya atar. Bu örneğin satınalma siparişinin maliyet merkezini değil, projenin maliyet merkezini kullandığını unutmayın.

## <a name="set-up-expenditure-reviewers"></a>Harcama gözden geçirenleri ayarlama

Bu örnekte, bir satınalma talebi harcamaları gözden geçireninin nasıl yapılandırılacağı gösterilmektedir. Diğer türdeki harcama gözden geçirenleri yapılandırmak için adım 1'deki gezinti yolunu, bu konunun önceki bölümlerinde yer alan [Harcama gözden geçirenleri türleri](configure-expenditure-reviewers.md#types-of-expenditure-reviewers) bölümünde bulunan tablodaki uygun yolla değiştirin.

1. **Tedarik ve kaynak atama \> Kurulum \> İlkeler \> Satınalma talebi harcama gözden geçirenleri**'ne gidin.
2. **Satınalma talebi harcamaları gözden geçirenleri** sayfasında, **Yeni**'yi seçin.
3. **Ad** alanına, harcama gözden geçireni yapılandırması için **maliyet merkezi** gibi bir ad girin.
4. **Tüzel kişiliğe göre harcama gözden geçirenleri** hızlı sekmesinde, yapılandırılacak tüzel kişiliği seçin.
5. Proje dağıtımında, her proje yetkilisi için onay kutusunu seçin ve etkinleştirmek istediğiniz her mali boyut için **Evet**'i seçin. 
6. Kuruluş dağıtımında, **Kuruluş dağıtımları** sekmesinde, etkinleştirmek istediğiniz her mali boyut için **Evet**'i seçin.
7. Her ek tüzel kişilik için 4 ile 6 arasındaki adımları yineleyin.

## <a name="assign-owners-to-financial-dimensions"></a>Mali boyutlara sahip atama

Bir mali boyuta sahip atamak için aşağıdaki adımları izleyin.

1. **Genel muhasebe \> Hesap planı \> Boyutlar \> Mali boyutlar**'a gidin.
2. Listede, sahiplerin atanacağı mali boyutu seçin.
3. **Boyut değerleri**'ni seçin.
4. Boyut değerlerinde değişiklik yapmak için **Düzenle**'yi seçin.
5. Listede, bir sahip atanacak mali boyut değerini seçin.
6. **Sahip** alanında, mali boyutu atamak için bir çalışan seçin.

## <a name="configure-project-distributions"></a>Proje dağıtımlarını yapılandırma

Bir projeye proje yetkilileri atamak için şu adımları izleyin.

1. **Proje yönetimi ve muhasebe \> Projeler \> Tüm projeler**'e gidin.
2. Yetkililer atanacak projeyi seçin.
3. Projede değişiklik yapmak için **Düzenle**'yi seçin.
4. **Genel** hızlı sekmesinde, **Sorumlu** bölümünde, **Satış yöneticisi**, **Proje yöneticisi** ve **Proje denetleyicisi** alanları için gereken şekilde bir çalışan seçin.
5. **Mali boyutlar** hızlı sekmesinde, projeniz için gerekli mali boyutları seçin.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Harcama gözden geçirenlerini bir iş akışı görevine atama

Bu örnekte, satınalma talebi harcamaları gözden geçireni kullanmasını sağlamak üzere bir satın alma talebi iş akışının nasıl yapılandırılacağı gösterilir. Diğer iş akışı türlerini yapılandırmak için adım 1'de açmanız gereken iş akışı sayfası **Tedarik ve kaynak atama** modülü yerine **Gider yönetimi** veya **Borç hesapları** modülünde olabilir.

Bir iş akışı görevine satınalma talebi harcamaları gözden geçirenleri atamak için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak atama \> Kurulum \> Tedarik ve kaynak atama iş akışları**'na gidin.
2. Mevcut bir iş akışına çift dokunun (veya çift tıklayın) veya yeni bir iş akışı oluşturun.
3. İş akışı düzenleyicisinde, **İş akışı** bölmesinde, harcama gözden geçireni yapılandırmasının atanacağı görevi seçin. Sonra, **Eylem Bölmesinde**, **Göster** grubunda, **Özellikler**'i seçin.
4. **Özellikler** sayfasının sol bölmesinde **Atama**'yı seçin.
5. **Atama türü** sekmesinde **Katılımcı**'yı seçin.
6. **Rol tabanlı** sekmesinde, **Katılımcı türü** alanında, **Harcama katılımcıları**'nı seçin. Daha sonra **Katılımcı** alanında, iş akışı görevi için kullanılacak harcama gözden geçireni yapılandırmasını seçin.
